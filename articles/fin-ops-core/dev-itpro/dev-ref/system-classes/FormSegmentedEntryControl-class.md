---
title: FormSegmentedEntryControl クラス
description: このトピックでは、FormSegmentedEntryControl クラスについて説明します。
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
ms.openlocfilehash: 063d20875b10f7936c27412df8aa1cf3c76e7133
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502617"
---
# <a name="class-formsegmentedentrycontrol"></a><span data-ttu-id="48d0b-103">クラス FormSegmentedEntryControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-103">Class FormSegmentedEntryControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormSegmentedEntryControl extends FormReferenceControl
```

## <a name="remarks"></a><span data-ttu-id="48d0b-104">備考</span><span class="sxs-lookup"><span data-stu-id="48d0b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="48d0b-105">例</span><span class="sxs-lookup"><span data-stu-id="48d0b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="48d0b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="48d0b-106">Methods</span></span>

| <span data-ttu-id="48d0b-107">方法</span><span class="sxs-lookup"><span data-stu-id="48d0b-107">Method</span></span>                                                                                                      | <span data-ttu-id="48d0b-108">説明</span><span class="sxs-lookup"><span data-stu-id="48d0b-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d0b-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="48d0b-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="48d0b-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="48d0b-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="48d0b-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="48d0b-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="48d0b-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="48d0b-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="48d0b-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="48d0b-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="48d0b-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-118">Gets or sets the background color of the control.</span></span>                                                                                                                       
| <span data-ttu-id="48d0b-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="48d0b-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-120">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="48d0b-121">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48d0b-121">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="48d0b-122">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-122">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="48d0b-123">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-123">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="48d0b-124">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-124">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="48d0b-125">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="48d0b-125">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="48d0b-126">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-126">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="48d0b-127">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-127">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="48d0b-128">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-128">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="48d0b-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="48d0b-130">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-130">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="48d0b-131">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="48d0b-131">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="48d0b-132">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-132">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="48d0b-133">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-133">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="48d0b-134">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-134">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="48d0b-135">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-135">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-136">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-136">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="48d0b-137">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-137">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="48d0b-138">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-138">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="48d0b-139">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-139">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="48d0b-140">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-140">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="48d0b-141">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-141">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="48d0b-142">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-142">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="48d0b-143">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-143">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="48d0b-144">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48d0b-144">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="48d0b-145">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-145">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="48d0b-146">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48d0b-146">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="48d0b-147">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-147">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="48d0b-148">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="48d0b-148">public str dragText()</span></span>                                                                                       | <span data-ttu-id="48d0b-149">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-149">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="48d0b-150">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-150">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="48d0b-151">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-151">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="48d0b-152">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-152">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-153">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-153">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="48d0b-154">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-154">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="48d0b-155">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-155">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="48d0b-156">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-156">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="48d0b-157">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="48d0b-157">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="48d0b-158">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-158">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="48d0b-159">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-159">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="48d0b-160">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-160">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="48d0b-161">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-161">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="48d0b-162">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-162">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="48d0b-163">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-163">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="48d0b-164">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-164">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="48d0b-165">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="48d0b-165">public str helpField()</span></span>                                                                                      | <span data-ttu-id="48d0b-166">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-166">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="48d0b-167">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-167">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="48d0b-168">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-168">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="48d0b-169">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-169">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="48d0b-170">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-170">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="48d0b-171">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="48d0b-171">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="48d0b-172">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-172">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="48d0b-173">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="48d0b-173">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-174">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="48d0b-174">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="48d0b-175">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-175">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="48d0b-176">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="48d0b-176">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="48d0b-177">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-177">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="48d0b-178">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="48d0b-178">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="48d0b-179">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-179">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="48d0b-180">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="48d0b-180">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-181">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-181">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="48d0b-182">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-182">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="48d0b-183">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-183">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-184">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-184">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-185">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-185">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-186">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-186">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-187">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-187">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-188">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-188">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-189">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-189">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-190">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-190">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-191">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-191">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-192">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-192">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-193">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-193">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-194">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-194">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-195">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-195">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-196">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-196">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-197">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-197">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-198">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-198">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-199">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-199">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-200">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-200">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-201">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-201">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-202">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="48d0b-202">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-203">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-203">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="48d0b-204">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-204">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="48d0b-205">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-205">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="48d0b-206">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-206">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="48d0b-207">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-207">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="48d0b-208">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-208">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="48d0b-209">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-209">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-210">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-210">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="48d0b-211">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-211">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="48d0b-212">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="48d0b-212">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-213">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-213">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="48d0b-214">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-214">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="48d0b-215">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-215">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="48d0b-216">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-216">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="48d0b-217">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-217">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="48d0b-218">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-218">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="48d0b-219">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-219">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="48d0b-220">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-220">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="48d0b-221">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-221">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="48d0b-222">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-222">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="48d0b-223">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-223">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-224">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="48d0b-224">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-225">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="48d0b-225">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="48d0b-226">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-226">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="48d0b-227">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-227">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-228">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-228">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-229">public FieldId referenceField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-229">public FieldId referenceField(\[FieldId value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-230">public str replacementFieldGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-230">public str replacementFieldGroup(\[str value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-231">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-231">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="48d0b-232">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-232">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="48d0b-233">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="48d0b-233">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="48d0b-234">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-234">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="48d0b-235">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-235">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-236">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-236">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="48d0b-237">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-237">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="48d0b-238">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-238">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-239">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="48d0b-239">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="48d0b-240">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-240">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="48d0b-241">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-241">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="48d0b-242">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-242">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="48d0b-243">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-243">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="48d0b-244">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-244">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="48d0b-245">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-245">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="48d0b-246">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-246">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="48d0b-247">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-247">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-248">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="48d0b-248">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-249">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-249">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="48d0b-250">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-250">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="48d0b-251">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-251">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="48d0b-252">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-252">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="48d0b-253">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-253">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="48d0b-254">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-254">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="48d0b-255">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-255">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="48d0b-256">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-256">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="48d0b-257">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-257">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="48d0b-258">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-258">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="48d0b-259">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-259">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="48d0b-260">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-260">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="48d0b-261">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-261">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="48d0b-262">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-262">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="48d0b-263">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-263">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="48d0b-264">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-264">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="48d0b-265">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-265">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="48d0b-266">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-266">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="48d0b-267">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-267">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="48d0b-268">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-268">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="48d0b-269">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-269">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="48d0b-270">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-270">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="48d0b-271">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-271">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="48d0b-272">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-272">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="48d0b-273">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="48d0b-273">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-274">public Int64 value(\[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-274">public Int64 value(\[Int64 value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-275">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-275">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="48d0b-276">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-276">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="48d0b-277">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-277">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="48d0b-278">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-278">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="48d0b-279">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-279">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="48d0b-280">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-280">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="48d0b-281">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-281">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-282">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-282">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="48d0b-283">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-283">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="48d0b-284">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-284">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="48d0b-285">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-285">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="48d0b-286">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-286">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="48d0b-287">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-287">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="48d0b-288">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-288">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="48d0b-289">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-289">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="48d0b-290">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-290">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-291">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="48d0b-291">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="48d0b-292">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-292">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="48d0b-293">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-293">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-294">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="48d0b-294">public void displayControl()</span></span>                                                                                | <span data-ttu-id="48d0b-295">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-295">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="48d0b-296">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="48d0b-296">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="48d0b-297">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-297">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="48d0b-298">public void undo()</span><span class="sxs-lookup"><span data-stu-id="48d0b-298">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-299">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-299">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-300">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-300">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-301">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="48d0b-301">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-302">public void enter()</span><span class="sxs-lookup"><span data-stu-id="48d0b-302">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-303">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="48d0b-303">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="48d0b-304">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-304">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="48d0b-305">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48d0b-305">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="48d0b-306">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-306">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="48d0b-307">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="48d0b-307">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="48d0b-308">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-308">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="48d0b-309">public void cut()</span><span class="sxs-lookup"><span data-stu-id="48d0b-309">public void cut()</span></span>                                                                                           | <span data-ttu-id="48d0b-310">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-310">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="48d0b-311">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="48d0b-311">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-312">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-312">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-313">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="48d0b-313">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="48d0b-314">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-314">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="48d0b-315">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="48d0b-315">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="48d0b-316">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-316">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="48d0b-317">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-317">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-318">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-318">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-319">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="48d0b-319">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="48d0b-320">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-320">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="48d0b-321">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-321">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-322">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="48d0b-322">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="48d0b-323">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-323">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="48d0b-324">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="48d0b-324">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="48d0b-325">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-325">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="48d0b-326">public void copy()</span><span class="sxs-lookup"><span data-stu-id="48d0b-326">public void copy()</span></span>                                                                                          | <span data-ttu-id="48d0b-327">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-327">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="48d0b-328">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="48d0b-328">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="48d0b-329">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-329">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="48d0b-330">public void context()</span><span class="sxs-lookup"><span data-stu-id="48d0b-330">public void context()</span></span>                                                                                       | <span data-ttu-id="48d0b-331">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-331">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="48d0b-332">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-332">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="48d0b-333">public void paste()</span><span class="sxs-lookup"><span data-stu-id="48d0b-333">public void paste()</span></span>                                                                                         | <span data-ttu-id="48d0b-334">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-334">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="48d0b-335">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="48d0b-335">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="48d0b-336">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-336">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="48d0b-337">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="48d0b-337">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="48d0b-338">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-338">Method alignControl</span></span>

<span data-ttu-id="48d0b-339">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-339">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="48d0b-340">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-340">Parameters - alignControl</span></span>

<span data-ttu-id="48d0b-341">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-341">value</span></span>  
<span data-ttu-id="48d0b-342">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-342">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="48d0b-343">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-343">Return Value - alignControl</span></span>

<span data-ttu-id="48d0b-344">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-344">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="48d0b-345">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-345">Remarks - alignControl</span></span>

<span data-ttu-id="48d0b-346">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-346">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="48d0b-347">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="48d0b-347">Method allowEdit</span></span>

<span data-ttu-id="48d0b-348">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-348">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="48d0b-349">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="48d0b-349">Parameters - allowEdit</span></span>

<span data-ttu-id="48d0b-350">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-350">value</span></span>  
<span data-ttu-id="48d0b-351">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-351">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="48d0b-352">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="48d0b-352">Return Value - allowEdit</span></span>

<span data-ttu-id="48d0b-353">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-353">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="48d0b-354">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="48d0b-354">Remarks - allowEdit</span></span>

<span data-ttu-id="48d0b-355">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-355">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="48d0b-356">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="48d0b-356">Method allowSysSetup</span></span>

<span data-ttu-id="48d0b-357">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-357">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="48d0b-358">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="48d0b-358">Return Value - allowSysSetup</span></span>

<span data-ttu-id="48d0b-359">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-359">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="48d0b-360">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48d0b-360">Method autoDeclaration</span></span>

<span data-ttu-id="48d0b-361">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-361">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="48d0b-362">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48d0b-362">Parameters - autoDeclaration</span></span>

<span data-ttu-id="48d0b-363">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-363">value</span></span>  
<span data-ttu-id="48d0b-364">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-364">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="48d0b-365">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48d0b-365">Return Value - autoDeclaration</span></span>

<span data-ttu-id="48d0b-366">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-366">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="48d0b-367">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="48d0b-367">Remarks - autoDeclaration</span></span>

<span data-ttu-id="48d0b-368">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-368">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="48d0b-369">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-369">Method backgroundColor</span></span>

<span data-ttu-id="48d0b-370">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-370">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="48d0b-371">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-371">Parameters - backgroundColor</span></span>

<span data-ttu-id="48d0b-372">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-372">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="48d0b-373">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-373">Return Value - backgroundColor</span></span>

<span data-ttu-id="48d0b-374">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="48d0b-374">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="48d0b-375">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-375">Remarks - backgroundColor</span></span>

<span data-ttu-id="48d0b-376">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-376">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="48d0b-377">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-377">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="48d0b-378">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-378">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="48d0b-379">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-379">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="48d0b-380">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-380">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="48d0b-381">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-381">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="48d0b-382">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="48d0b-382">Method backStyle</span></span>

<span data-ttu-id="48d0b-383">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-383">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="48d0b-384">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="48d0b-384">Parameters - backStyle</span></span>

<span data-ttu-id="48d0b-385">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-385">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="48d0b-386">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="48d0b-386">Return Value - backStyle</span></span>

<span data-ttu-id="48d0b-387">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-387">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="48d0b-388">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="48d0b-388">Method beginDrag</span></span>

<span data-ttu-id="48d0b-389">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-389">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="48d0b-390">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="48d0b-390">Parameters - beginDrag</span></span>

<span data-ttu-id="48d0b-391">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-391">x</span></span>  
<span data-ttu-id="48d0b-392">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-392">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="48d0b-393">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-393">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="48d0b-394">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-394">y</span></span>  
<span data-ttu-id="48d0b-395">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-395">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="48d0b-396">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-396">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="48d0b-397">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="48d0b-397">Return Value - beginDrag</span></span>

<span data-ttu-id="48d0b-398">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-398">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="48d0b-399">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="48d0b-399">Remarks - beginDrag</span></span>

<span data-ttu-id="48d0b-400">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-400">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="48d0b-401">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-401">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-border"></a><span data-ttu-id="48d0b-402">メソッド border</span><span class="sxs-lookup"><span data-stu-id="48d0b-402">Method border</span></span>

<span data-ttu-id="48d0b-403">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-403">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="48d0b-404">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="48d0b-404">Parameters - border</span></span>

<span data-ttu-id="48d0b-405">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-405">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="48d0b-406">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="48d0b-406">Return Value - border</span></span>

<span data-ttu-id="48d0b-407">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="48d0b-407">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="48d0b-408">備考 - border</span><span class="sxs-lookup"><span data-stu-id="48d0b-408">Remarks - border</span></span>

<span data-ttu-id="48d0b-409">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-409">The integer that is returned contains the style of the borderline of the control as follows.</span></span>

| <span data-ttu-id="48d0b-410">先頭値</span><span class="sxs-lookup"><span data-stu-id="48d0b-410">Value</span></span> | <span data-ttu-id="48d0b-411">説明</span><span class="sxs-lookup"><span data-stu-id="48d0b-411">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="48d0b-412">0</span><span class="sxs-lookup"><span data-stu-id="48d0b-412">0</span></span>     | <span data-ttu-id="48d0b-413">自動</span><span class="sxs-lookup"><span data-stu-id="48d0b-413">Auto</span></span>        |
| <span data-ttu-id="48d0b-414">1</span><span class="sxs-lookup"><span data-stu-id="48d0b-414">1</span></span>     | <span data-ttu-id="48d0b-415">3D</span><span class="sxs-lookup"><span data-stu-id="48d0b-415">3D</span></span>          |
| <span data-ttu-id="48d0b-416">2</span><span class="sxs-lookup"><span data-stu-id="48d0b-416">2</span></span>     | <span data-ttu-id="48d0b-417">単一明細行</span><span class="sxs-lookup"><span data-stu-id="48d0b-417">Single line</span></span> |
| <span data-ttu-id="48d0b-418">3</span><span class="sxs-lookup"><span data-stu-id="48d0b-418">3</span></span>     | <span data-ttu-id="48d0b-419">均一</span><span class="sxs-lookup"><span data-stu-id="48d0b-419">Flat</span></span>        |
| <span data-ttu-id="48d0b-420">4</span><span class="sxs-lookup"><span data-stu-id="48d0b-420">4</span></span>     | <span data-ttu-id="48d0b-421">None</span><span class="sxs-lookup"><span data-stu-id="48d0b-421">None</span></span>        |

## <a name="method-calccontrolsize"></a><span data-ttu-id="48d0b-422">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-422">Method calcControlSize</span></span>

<span data-ttu-id="48d0b-423">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-423">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="48d0b-424">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-424">Parameters - calcControlSize</span></span>

<span data-ttu-id="48d0b-425">chars</span><span class="sxs-lookup"><span data-stu-id="48d0b-425">chars</span></span>  
<span data-ttu-id="48d0b-426">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="48d0b-426">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="48d0b-427">明細行</span><span class="sxs-lookup"><span data-stu-id="48d0b-427">lines</span></span>  
<span data-ttu-id="48d0b-428">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="48d0b-428">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="48d0b-429">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-429">Return Value - calcControlSize</span></span>

<span data-ttu-id="48d0b-430">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="48d0b-430">The container that holds the width and height.</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="48d0b-431">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="48d0b-431">Method colorScheme</span></span>

<span data-ttu-id="48d0b-432">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-432">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="48d0b-433">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="48d0b-433">Parameters - colorScheme</span></span>

<span data-ttu-id="48d0b-434">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-434">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="48d0b-435">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="48d0b-435">Return Value - colorScheme</span></span>

<span data-ttu-id="48d0b-436">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="48d0b-436">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="48d0b-437">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="48d0b-437">Remarks - colorScheme</span></span>

<span data-ttu-id="48d0b-438">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-438">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="48d0b-439">金額</span><span class="sxs-lookup"><span data-stu-id="48d0b-439">Value</span></span> | <span data-ttu-id="48d0b-440">スタイル</span><span class="sxs-lookup"><span data-stu-id="48d0b-440">Style</span></span>                        |
|-------|------------------------------|
| <span data-ttu-id="48d0b-441">0</span><span class="sxs-lookup"><span data-stu-id="48d0b-441">0</span></span>     | <span data-ttu-id="48d0b-442">既定</span><span class="sxs-lookup"><span data-stu-id="48d0b-442">Default</span></span>                      |
| <span data-ttu-id="48d0b-443">1</span><span class="sxs-lookup"><span data-stu-id="48d0b-443">1</span></span>     | <span data-ttu-id="48d0b-444">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="48d0b-444">The Microsoft Windows palette</span></span> |
| <span data-ttu-id="48d0b-445">2</span><span class="sxs-lookup"><span data-stu-id="48d0b-445">2</span></span>     | <span data-ttu-id="48d0b-446">真の配色</span><span class="sxs-lookup"><span data-stu-id="48d0b-446">The true-color scheme</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="48d0b-447">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="48d0b-447">Method configurationKey</span></span>

<span data-ttu-id="48d0b-448">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-448">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="48d0b-449">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="48d0b-449">Parameters - configurationKey</span></span>

<span data-ttu-id="48d0b-450">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-450">value</span></span>  
<span data-ttu-id="48d0b-451">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-451">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="48d0b-452">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="48d0b-452">Return Value - configurationKey</span></span>

<span data-ttu-id="48d0b-453">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="48d0b-453">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="48d0b-454">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="48d0b-454">Remarks - configurationKey</span></span>

<span data-ttu-id="48d0b-455">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-455">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="48d0b-456">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-456">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="48d0b-457">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-457">Method configurationKeyEx</span></span>

<span data-ttu-id="48d0b-458">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-458">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="48d0b-459">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-459">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="48d0b-460">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="48d0b-460">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="48d0b-461">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-461">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="48d0b-462">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-462">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="48d0b-463">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-463">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="48d0b-464">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-464">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="48d0b-465">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="48d0b-465">Method countryRegionCodes</span></span>

<span data-ttu-id="48d0b-466">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-466">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="48d0b-467">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="48d0b-467">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="48d0b-468">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-468">value</span></span>  
<span data-ttu-id="48d0b-469">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-469">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="48d0b-470">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="48d0b-470">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="48d0b-471">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="48d0b-471">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="48d0b-472">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="48d0b-472">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="48d0b-473">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="48d0b-473">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="48d0b-474">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-474">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="48d0b-475">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="48d0b-475">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="48d0b-476">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48d0b-476">Method dataRelationPath</span></span>

<span data-ttu-id="48d0b-477">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-477">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="48d0b-478">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48d0b-478">Parameters - dataRelationPath</span></span>

<span data-ttu-id="48d0b-479">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-479">value</span></span>  
<span data-ttu-id="48d0b-480">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-480">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="48d0b-481">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48d0b-481">Return Value - dataRelationPath</span></span>

<span data-ttu-id="48d0b-482">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="48d0b-482">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="48d0b-483">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="48d0b-483">Remarks - dataRelationPath</span></span>

<span data-ttu-id="48d0b-484">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-484">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="48d0b-485">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="48d0b-485">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="48d0b-486">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="48d0b-486">Method dataSource</span></span>

<span data-ttu-id="48d0b-487">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-487">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="48d0b-488">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="48d0b-488">Parameters - dataSource</span></span>

<span data-ttu-id="48d0b-489">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-489">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="48d0b-490">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="48d0b-490">Return Value - dataSource</span></span>

<span data-ttu-id="48d0b-491">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="48d0b-491">The identifier of the data source to use.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="48d0b-492">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="48d0b-492">Method displayTarget</span></span>

<span data-ttu-id="48d0b-493">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-493">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="48d0b-494">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="48d0b-494">Parameters - displayTarget</span></span>

<span data-ttu-id="48d0b-495">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-495">value</span></span>  
<span data-ttu-id="48d0b-496">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-496">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="48d0b-497">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="48d0b-497">Return Value - displayTarget</span></span>

<span data-ttu-id="48d0b-498">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-498">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="48d0b-499">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="48d0b-499">Method dragDrop</span></span>

<span data-ttu-id="48d0b-500">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-500">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="48d0b-501">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="48d0b-501">Parameters - dragDrop</span></span>

<span data-ttu-id="48d0b-502">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-502">value</span></span>  
<span data-ttu-id="48d0b-503">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-503">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="48d0b-504">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="48d0b-504">Return Value - dragDrop</span></span>

<span data-ttu-id="48d0b-505">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-505">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="48d0b-506">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="48d0b-506">Remarks - dragDrop</span></span>

<span data-ttu-id="48d0b-507">dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-507">Use the dragLeave Method, the dragOver Method, and the dragOverEx Method to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="48d0b-508">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="48d0b-508">Method dragOver</span></span>

<span data-ttu-id="48d0b-509">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-509">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="48d0b-510">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="48d0b-510">Parameters - dragOver</span></span>

<span data-ttu-id="48d0b-511">dragSource</span><span class="sxs-lookup"><span data-stu-id="48d0b-511">dragSource</span></span>  
<span data-ttu-id="48d0b-512">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-512">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-513">dragMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-513">dragMode</span></span>  
<span data-ttu-id="48d0b-514">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-514">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-515">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-515">x</span></span>  
<span data-ttu-id="48d0b-516">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-516">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-517">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-517">y</span></span>  
<span data-ttu-id="48d0b-518">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-518">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="48d0b-519">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="48d0b-519">Return Value - dragOver</span></span>

<span data-ttu-id="48d0b-520">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-520">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="48d0b-521">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-521">Method dragOverEx</span></span>

<span data-ttu-id="48d0b-522">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-522">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="48d0b-523">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-523">Parameters - dragOverEx</span></span>

<span data-ttu-id="48d0b-524">dragSource</span><span class="sxs-lookup"><span data-stu-id="48d0b-524">dragSource</span></span>  
<span data-ttu-id="48d0b-525">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-525">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-526">dragMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-526">dragMode</span></span>  
<span data-ttu-id="48d0b-527">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-527">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-528">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-528">x</span></span>  
<span data-ttu-id="48d0b-529">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-529">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-530">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-530">y</span></span>  
<span data-ttu-id="48d0b-531">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-531">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="48d0b-532">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-532">Return Value - dragOverEx</span></span>

<span data-ttu-id="48d0b-533">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-533">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="48d0b-534">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="48d0b-534">Method dragText</span></span>

<span data-ttu-id="48d0b-535">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-535">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="48d0b-536">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="48d0b-536">Return Value - dragText</span></span>

<span data-ttu-id="48d0b-537">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="48d0b-537">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="48d0b-538">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-538">Method enabled</span></span>

<span data-ttu-id="48d0b-539">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-539">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="48d0b-540">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-540">Parameters - enabled</span></span>

<span data-ttu-id="48d0b-541">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-541">value</span></span>  
<span data-ttu-id="48d0b-542">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-542">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="48d0b-543">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-543">Return Value - enabled</span></span>

<span data-ttu-id="48d0b-544">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-544">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="48d0b-545">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-545">Remarks - enabled</span></span>

<span data-ttu-id="48d0b-546">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-546">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="48d0b-547">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-547">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="48d0b-548">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-548">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="48d0b-549">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="48d0b-549">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="48d0b-550">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="48d0b-550">Parameters - extendedDataType</span></span>

<span data-ttu-id="48d0b-551">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-551">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="48d0b-552">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="48d0b-552">Return Value - extendedDataType</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="48d0b-553">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-553">Method foregroundColor</span></span>

<span data-ttu-id="48d0b-554">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-554">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="48d0b-555">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-555">Parameters - foregroundColor</span></span>

<span data-ttu-id="48d0b-556">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-556">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="48d0b-557">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-557">Return Value - foregroundColor</span></span>

<span data-ttu-id="48d0b-558">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="48d0b-558">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="48d0b-559">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-559">Remarks - foregroundColor</span></span>

<span data-ttu-id="48d0b-560">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-560">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="48d0b-561">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-561">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="48d0b-562">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-562">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="48d0b-563">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="48d0b-563">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="48d0b-564">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-564">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="48d0b-565">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-565">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="48d0b-566">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="48d0b-566">Method hasChanged</span></span>

<span data-ttu-id="48d0b-567">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-567">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="48d0b-568">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="48d0b-568">Parameters - hasChanged</span></span>

<span data-ttu-id="48d0b-569">val</span><span class="sxs-lookup"><span data-stu-id="48d0b-569">val</span></span>  
<span data-ttu-id="48d0b-570">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-570">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="48d0b-571">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="48d0b-571">Return Value - hasChanged</span></span>

<span data-ttu-id="48d0b-572">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-572">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="48d0b-573">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="48d0b-573">Method hasUserSetting</span></span>

<span data-ttu-id="48d0b-574">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-574">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="48d0b-575">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="48d0b-575">Return Value - hasUserSetting</span></span>

<span data-ttu-id="48d0b-576">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-576">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="48d0b-577">メソッド height</span><span class="sxs-lookup"><span data-stu-id="48d0b-577">Method height</span></span>

<span data-ttu-id="48d0b-578">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-578">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="48d0b-579">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="48d0b-579">Parameters - height</span></span>

<span data-ttu-id="48d0b-580">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-580">value</span></span>  
<span data-ttu-id="48d0b-581">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-581">An integer value that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="48d0b-582">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-582">mode</span></span>  
<span data-ttu-id="48d0b-583">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-583">An integer value that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="48d0b-584">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="48d0b-584">Return Value - height</span></span>

<span data-ttu-id="48d0b-585">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="48d0b-585">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="48d0b-586">備考 - height</span><span class="sxs-lookup"><span data-stu-id="48d0b-586">Remarks - height</span></span>

<span data-ttu-id="48d0b-587">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-587">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="48d0b-588">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-588">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="48d0b-589">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-589">Mode</span></span>            | <span data-ttu-id="48d0b-590">高さの計算</span><span class="sxs-lookup"><span data-stu-id="48d0b-590">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d0b-591">-1 正確</span><span class="sxs-lookup"><span data-stu-id="48d0b-591">-1 Exact</span></span>        | <span data-ttu-id="48d0b-592">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-592">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48d0b-593">0 自動</span><span class="sxs-lookup"><span data-stu-id="48d0b-593">0 Auto</span></span>          | <span data-ttu-id="48d0b-594">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-594">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48d0b-595">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="48d0b-595">1 Column height</span></span> | <span data-ttu-id="48d0b-596">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-596">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="48d0b-597">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-597">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="48d0b-598">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-598">Method heightMode</span></span>

<span data-ttu-id="48d0b-599">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-599">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="48d0b-600">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-600">Parameters - heightMode</span></span>

<span data-ttu-id="48d0b-601">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-601">value</span></span>  
<span data-ttu-id="48d0b-602">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-602">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="48d0b-603">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-603">Return Value - heightMode</span></span>

<span data-ttu-id="48d0b-604">計算モード。</span><span class="sxs-lookup"><span data-stu-id="48d0b-604">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="48d0b-605">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-605">Remarks - heightMode</span></span>

<span data-ttu-id="48d0b-606">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-606">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="48d0b-607">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-607">Mode</span></span>          | <span data-ttu-id="48d0b-608">高さの計算</span><span class="sxs-lookup"><span data-stu-id="48d0b-608">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d0b-609">正確</span><span class="sxs-lookup"><span data-stu-id="48d0b-609">Exact</span></span>         | <span data-ttu-id="48d0b-610">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-610">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48d0b-611">自動</span><span class="sxs-lookup"><span data-stu-id="48d0b-611">Auto</span></span>          | <span data-ttu-id="48d0b-612">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-612">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48d0b-613">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="48d0b-613">Column height</span></span> | <span data-ttu-id="48d0b-614">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-614">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="48d0b-615">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-615">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="48d0b-616">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-616">Method heightValue</span></span>

<span data-ttu-id="48d0b-617">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-617">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="48d0b-618">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-618">Parameters - heightValue</span></span>

<span data-ttu-id="48d0b-619">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-619">value</span></span>  
<span data-ttu-id="48d0b-620">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-620">An integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="48d0b-621">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-621">Return Value - heightValue</span></span>

<span data-ttu-id="48d0b-622">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="48d0b-622">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="48d0b-623">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-623">Remarks - heightValue</span></span>

<span data-ttu-id="48d0b-624">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-624">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="48d0b-625">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="48d0b-625">Method helpField</span></span>

<span data-ttu-id="48d0b-626">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-626">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="48d0b-627">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="48d0b-627">Return Value - helpField</span></span>

<span data-ttu-id="48d0b-628">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="48d0b-628">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="48d0b-629">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="48d0b-629">Remarks - helpField</span></span>

<span data-ttu-id="48d0b-630">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-630">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="48d0b-631">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-631">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="48d0b-632">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="48d0b-632">Method helpText</span></span>

<span data-ttu-id="48d0b-633">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-633">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="48d0b-634">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="48d0b-634">Parameters - helpText</span></span>

<span data-ttu-id="48d0b-635">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-635">value</span></span>  
<span data-ttu-id="48d0b-636">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-636">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="48d0b-637">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="48d0b-637">Return Value - helpText</span></span>

<span data-ttu-id="48d0b-638">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="48d0b-638">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="48d0b-639">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="48d0b-639">Remarks - helpText</span></span>

<span data-ttu-id="48d0b-640">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-640">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="48d0b-641">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-641">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="48d0b-642">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="48d0b-642">Method hierarchyParent</span></span>

<span data-ttu-id="48d0b-643">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-643">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="48d0b-644">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="48d0b-644">Parameters - hierarchyParent</span></span>

<span data-ttu-id="48d0b-645">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-645">value</span></span>  
<span data-ttu-id="48d0b-646">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-646">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="48d0b-647">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="48d0b-647">Return Value - hierarchyParent</span></span>

<span data-ttu-id="48d0b-648">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-648">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="48d0b-649">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="48d0b-649">Method hWnd</span></span>

<span data-ttu-id="48d0b-650">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-650">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="48d0b-651">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="48d0b-651">Return Value - hWnd</span></span>

<span data-ttu-id="48d0b-652">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="48d0b-652">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="48d0b-653">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="48d0b-653">Remarks - hWnd</span></span>

<span data-ttu-id="48d0b-654">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-654">This handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="48d0b-655">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="48d0b-655">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="48d0b-656">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="48d0b-656">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="48d0b-657">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="48d0b-657">Method isDisplayed</span></span>

<span data-ttu-id="48d0b-658">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-658">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="48d0b-659">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="48d0b-659">Return Value - isDisplayed</span></span>

<span data-ttu-id="48d0b-660">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-660">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="48d0b-661">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="48d0b-661">Remarks - isDisplayed</span></span>

<span data-ttu-id="48d0b-662">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-662">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="48d0b-663">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="48d0b-663">Method isRestricted</span></span>

<span data-ttu-id="48d0b-664">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-664">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="48d0b-665">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="48d0b-665">Return Value - isRestricted</span></span>

<span data-ttu-id="48d0b-666">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-666">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="48d0b-667">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-667">Method isUserSetupEnabled</span></span>

<span data-ttu-id="48d0b-668">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-668">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="48d0b-669">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-669">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="48d0b-670">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="48d0b-670">neededSetupRights</span></span>  
<span data-ttu-id="48d0b-671">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-671">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="48d0b-672">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-672">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="48d0b-673">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-673">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="48d0b-674">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="48d0b-674">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="48d0b-675">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-675">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d0b-676">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="48d0b-676">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="48d0b-677">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-677">No changes can be made to the control.</span></span> <span data-ttu-id="48d0b-678">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-678">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="48d0b-679">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="48d0b-679">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="48d0b-680">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-680">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="48d0b-681">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-681">The user cannot move the control.</span></span>   |
| <span data-ttu-id="48d0b-682">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="48d0b-682">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="48d0b-683">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-683">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="48d0b-684">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-684">The user can also move the control.</span></span> |

<span data-ttu-id="48d0b-685">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-685">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="48d0b-686">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="48d0b-686">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="48d0b-687">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="48d0b-687">Return Value - isValid</span></span>

## <a name="method-label"></a><span data-ttu-id="48d0b-688">メソッド label</span><span class="sxs-lookup"><span data-stu-id="48d0b-688">Method label</span></span>

<span data-ttu-id="48d0b-689">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-689">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="48d0b-690">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="48d0b-690">Parameters - label</span></span>

<span data-ttu-id="48d0b-691">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-691">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="48d0b-692">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="48d0b-692">Return Value - label</span></span>

<span data-ttu-id="48d0b-693">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-693">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="48d0b-694">備考 - label</span><span class="sxs-lookup"><span data-stu-id="48d0b-694">Remarks - label</span></span>

<span data-ttu-id="48d0b-695">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-695">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="48d0b-696">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-696">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="48d0b-697">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="48d0b-697">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="48d0b-698">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="48d0b-698">Parameters - labelAlignment</span></span>

<span data-ttu-id="48d0b-699">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-699">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="48d0b-700">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="48d0b-700">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="48d0b-701">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="48d0b-701">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="48d0b-702">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="48d0b-702">Parameters - labelBold</span></span>

<span data-ttu-id="48d0b-703">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-703">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="48d0b-704">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="48d0b-704">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="48d0b-705">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="48d0b-705">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="48d0b-706">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="48d0b-706">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="48d0b-707">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-707">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="48d0b-708">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="48d0b-708">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="48d0b-709">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="48d0b-709">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="48d0b-710">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="48d0b-710">Parameters - labelFont</span></span>

<span data-ttu-id="48d0b-711">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-711">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="48d0b-712">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="48d0b-712">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="48d0b-713">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-713">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="48d0b-714">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-714">Parameters - labelFontSize</span></span>

<span data-ttu-id="48d0b-715">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-715">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="48d0b-716">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-716">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="48d0b-717">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-717">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="48d0b-718">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-718">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="48d0b-719">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-719">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="48d0b-720">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="48d0b-720">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="48d0b-721">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="48d0b-721">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="48d0b-722">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="48d0b-722">Parameters - labelGuide</span></span>

<span data-ttu-id="48d0b-723">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-723">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="48d0b-724">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="48d0b-724">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="48d0b-725">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="48d0b-725">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="48d0b-726">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="48d0b-726">Parameters - labelHeight</span></span>

<span data-ttu-id="48d0b-727">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-727">value</span></span>  

<!-- -->

<span data-ttu-id="48d0b-728">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-728">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="48d0b-729">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="48d0b-729">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="48d0b-730">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-730">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="48d0b-731">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-731">Parameters - labelHeightMode</span></span>

<span data-ttu-id="48d0b-732">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-732">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="48d0b-733">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-733">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="48d0b-734">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-734">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="48d0b-735">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-735">Parameters - labelHeightValue</span></span>

<span data-ttu-id="48d0b-736">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-736">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="48d0b-737">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-737">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="48d0b-738">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="48d0b-738">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="48d0b-739">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="48d0b-739">Parameters - labelItalic</span></span>

<span data-ttu-id="48d0b-740">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-740">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="48d0b-741">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="48d0b-741">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="48d0b-742">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48d0b-742">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="48d0b-743">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48d0b-743">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="48d0b-744">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-744">x</span></span>  

<!-- -->

<span data-ttu-id="48d0b-745">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-745">y</span></span>  

<!-- -->

<span data-ttu-id="48d0b-746">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-746">button</span></span>  

<!-- -->

<span data-ttu-id="48d0b-747">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-747">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="48d0b-748">Shift</span><span class="sxs-lookup"><span data-stu-id="48d0b-748">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="48d0b-749">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48d0b-749">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="48d0b-750">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="48d0b-750">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="48d0b-751">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="48d0b-751">Parameters - labelMouseDown</span></span>

<span data-ttu-id="48d0b-752">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-752">x</span></span>  

<!-- -->

<span data-ttu-id="48d0b-753">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-753">y</span></span>  

<!-- -->

<span data-ttu-id="48d0b-754">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-754">button</span></span>  

<!-- -->

<span data-ttu-id="48d0b-755">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-755">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="48d0b-756">Shift</span><span class="sxs-lookup"><span data-stu-id="48d0b-756">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="48d0b-757">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="48d0b-757">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="48d0b-758">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="48d0b-758">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="48d0b-759">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="48d0b-759">Parameters - labelMouseUp</span></span>

<span data-ttu-id="48d0b-760">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-760">x</span></span>  

<!-- -->

<span data-ttu-id="48d0b-761">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-761">y</span></span>  

<!-- -->

<span data-ttu-id="48d0b-762">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-762">button</span></span>  

<!-- -->

<span data-ttu-id="48d0b-763">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-763">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="48d0b-764">Shift</span><span class="sxs-lookup"><span data-stu-id="48d0b-764">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="48d0b-765">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="48d0b-765">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="48d0b-766">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="48d0b-766">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="48d0b-767">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="48d0b-767">Parameters - labelPosition</span></span>

<span data-ttu-id="48d0b-768">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-768">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="48d0b-769">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="48d0b-769">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="48d0b-770">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="48d0b-770">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="48d0b-771">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="48d0b-771">Parameters - labelUnderline</span></span>

<span data-ttu-id="48d0b-772">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-772">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="48d0b-773">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="48d0b-773">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="48d0b-774">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="48d0b-774">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="48d0b-775">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="48d0b-775">Parameters - labelWidth</span></span>

<span data-ttu-id="48d0b-776">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-776">value</span></span>  

<!-- -->

<span data-ttu-id="48d0b-777">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-777">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="48d0b-778">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="48d0b-778">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="48d0b-779">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-779">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="48d0b-780">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-780">Parameters - labelWidthMode</span></span>

<span data-ttu-id="48d0b-781">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-781">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="48d0b-782">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-782">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="48d0b-783">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-783">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="48d0b-784">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-784">Parameters - labelWidthValue</span></span>

<span data-ttu-id="48d0b-785">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-785">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="48d0b-786">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-786">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="48d0b-787">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="48d0b-787">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="48d0b-788">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="48d0b-788">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="48d0b-789">メソッド left</span><span class="sxs-lookup"><span data-stu-id="48d0b-789">Method left</span></span>

<span data-ttu-id="48d0b-790">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-790">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="48d0b-791">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="48d0b-791">Parameters - left</span></span>

<span data-ttu-id="48d0b-792">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-792">value</span></span>  
<span data-ttu-id="48d0b-793">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-793">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="48d0b-794">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-794">mode</span></span>  
<span data-ttu-id="48d0b-795">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-795">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="48d0b-796">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="48d0b-796">Return Value - left</span></span>

<span data-ttu-id="48d0b-797">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="48d0b-797">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="48d0b-798">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-798">Method leftMode</span></span>

<span data-ttu-id="48d0b-799">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-799">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="48d0b-800">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-800">Parameters - leftMode</span></span>

<span data-ttu-id="48d0b-801">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-801">value</span></span>  
<span data-ttu-id="48d0b-802">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-802">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="48d0b-803">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-803">Return Value - leftMode</span></span>

<span data-ttu-id="48d0b-804">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="48d0b-804">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="48d0b-805">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-805">Method leftValue</span></span>

<span data-ttu-id="48d0b-806">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-806">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="48d0b-807">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-807">Parameters - leftValue</span></span>

<span data-ttu-id="48d0b-808">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-808">value</span></span>  
<span data-ttu-id="48d0b-809">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-809">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="48d0b-810">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-810">Return Value - leftValue</span></span>

<span data-ttu-id="48d0b-811">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="48d0b-811">The horizontal position of the control in the form.</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="48d0b-812">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="48d0b-812">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="48d0b-813">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="48d0b-813">Parameters - mandatory</span></span>

<span data-ttu-id="48d0b-814">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-814">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="48d0b-815">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="48d0b-815">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="48d0b-816">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="48d0b-816">Method markAsUserAdd</span></span>

<span data-ttu-id="48d0b-817">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-817">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="48d0b-818">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="48d0b-818">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="48d0b-819">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-819">value</span></span>  
<span data-ttu-id="48d0b-820">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-820">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="48d0b-821">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="48d0b-821">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="48d0b-822">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-822">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="48d0b-823">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="48d0b-823">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="48d0b-824">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="48d0b-824">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="48d0b-825">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48d0b-825">Method mouseDblClick</span></span>

<span data-ttu-id="48d0b-826">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-826">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="48d0b-827">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48d0b-827">Parameters - mouseDblClick</span></span>

<span data-ttu-id="48d0b-828">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-828">x</span></span>  
<span data-ttu-id="48d0b-829">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-829">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-830">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-830">y</span></span>  
<span data-ttu-id="48d0b-831">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-831">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-832">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-832">button</span></span>  
<span data-ttu-id="48d0b-833">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-833">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-834">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-834">Ctrl</span></span>  
<span data-ttu-id="48d0b-835">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-835">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-836">シフト</span><span class="sxs-lookup"><span data-stu-id="48d0b-836">Shift</span></span>  
<span data-ttu-id="48d0b-837">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-837">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="48d0b-838">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48d0b-838">Return Value - mouseDblClick</span></span>

<span data-ttu-id="48d0b-839">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-839">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="48d0b-840">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="48d0b-840">Remarks - mouseDblClick</span></span>

<span data-ttu-id="48d0b-841">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-841">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="48d0b-842">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="48d0b-842">Method mouseDown</span></span>

<span data-ttu-id="48d0b-843">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-843">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="48d0b-844">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="48d0b-844">Parameters - mouseDown</span></span>

<span data-ttu-id="48d0b-845">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-845">x</span></span>  
<span data-ttu-id="48d0b-846">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-846">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-847">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-847">y</span></span>  
<span data-ttu-id="48d0b-848">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-848">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-849">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-849">button</span></span>  
<span data-ttu-id="48d0b-850">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-850">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-851">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-851">Ctrl</span></span>  
<span data-ttu-id="48d0b-852">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-852">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-853">シフト</span><span class="sxs-lookup"><span data-stu-id="48d0b-853">Shift</span></span>  
<span data-ttu-id="48d0b-854">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-854">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="48d0b-855">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="48d0b-855">Return Value - mouseDown</span></span>

<span data-ttu-id="48d0b-856">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-856">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="48d0b-857">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="48d0b-857">Remarks - mouseDown</span></span>

<span data-ttu-id="48d0b-858">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-858">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="48d0b-859">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-859">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="48d0b-860">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="48d0b-860">Method mouseMove</span></span>

<span data-ttu-id="48d0b-861">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-861">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="48d0b-862">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="48d0b-862">Parameters - mouseMove</span></span>

<span data-ttu-id="48d0b-863">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-863">x</span></span>  
<span data-ttu-id="48d0b-864">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-864">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-865">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-865">y</span></span>  
<span data-ttu-id="48d0b-866">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-866">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-867">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-867">button</span></span>  
<span data-ttu-id="48d0b-868">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-868">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-869">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-869">Ctrl</span></span>  
<span data-ttu-id="48d0b-870">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-870">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-871">シフト</span><span class="sxs-lookup"><span data-stu-id="48d0b-871">Shift</span></span>  
<span data-ttu-id="48d0b-872">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-872">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="48d0b-873">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="48d0b-873">Return Value - mouseMove</span></span>

<span data-ttu-id="48d0b-874">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-874">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="48d0b-875">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="48d0b-875">Remarks - mouseMove</span></span>

<span data-ttu-id="48d0b-876">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-876">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="48d0b-877">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="48d0b-877">Method mouseUp</span></span>

<span data-ttu-id="48d0b-878">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-878">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="48d0b-879">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="48d0b-879">Parameters - mouseUp</span></span>

<span data-ttu-id="48d0b-880">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-880">x</span></span>  
<span data-ttu-id="48d0b-881">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-881">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-882">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-882">y</span></span>  
<span data-ttu-id="48d0b-883">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-883">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-884">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-884">button</span></span>  
<span data-ttu-id="48d0b-885">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-885">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-886">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-886">Ctrl</span></span>  
<span data-ttu-id="48d0b-887">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-887">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-888">シフト</span><span class="sxs-lookup"><span data-stu-id="48d0b-888">Shift</span></span>  
<span data-ttu-id="48d0b-889">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-889">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="48d0b-890">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="48d0b-890">Return Value - mouseUp</span></span>

<span data-ttu-id="48d0b-891">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-891">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="48d0b-892">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="48d0b-892">Remarks - mouseUp</span></span>

<span data-ttu-id="48d0b-893">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-893">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="48d0b-894">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-894">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="48d0b-895">メソッド名</span><span class="sxs-lookup"><span data-stu-id="48d0b-895">Method name</span></span>

<span data-ttu-id="48d0b-896">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-896">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="48d0b-897">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="48d0b-897">Parameters - name</span></span>

<span data-ttu-id="48d0b-898">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-898">value</span></span>  
<span data-ttu-id="48d0b-899">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="48d0b-899">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="48d0b-900">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="48d0b-900">Return Value - name</span></span>

<span data-ttu-id="48d0b-901">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="48d0b-901">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="48d0b-902">備考 - name</span><span class="sxs-lookup"><span data-stu-id="48d0b-902">Remarks - name</span></span>

<span data-ttu-id="48d0b-903">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-903">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="48d0b-904">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-904">It must start with a letter.</span></span>
-   <span data-ttu-id="48d0b-905">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-905">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="48d0b-906">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-906">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="48d0b-907">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-907">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="48d0b-908">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-908">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="48d0b-909">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="48d0b-909">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="48d0b-910">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="48d0b-910">Parameters - neededPermission</span></span>

<span data-ttu-id="48d0b-911">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-911">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="48d0b-912">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="48d0b-912">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="48d0b-913">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48d0b-913">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="48d0b-914">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48d0b-914">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="48d0b-915">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-915">Method parentControl</span></span>

<span data-ttu-id="48d0b-916">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-916">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="48d0b-917">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-917">Return Value - parentControl</span></span>

<span data-ttu-id="48d0b-918">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="48d0b-918">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="48d0b-919">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="48d0b-919">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="48d0b-920">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="48d0b-920">Parameters - previewPartRef</span></span>

<span data-ttu-id="48d0b-921">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-921">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="48d0b-922">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="48d0b-922">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="48d0b-923">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="48d0b-923">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="48d0b-924">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="48d0b-924">Parameters - promptrect</span></span>

<span data-ttu-id="48d0b-925">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-925">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="48d0b-926">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="48d0b-926">Return Value - promptrect</span></span>

## <a name="method-referencefield"></a><span data-ttu-id="48d0b-927">メソッド referenceField</span><span class="sxs-lookup"><span data-stu-id="48d0b-927">Method referenceField</span></span>

```xpp
public FieldId referenceField([FieldId value])
```

### <a name="parameters---referencefield"></a><span data-ttu-id="48d0b-928">パラメーター - referenceField</span><span class="sxs-lookup"><span data-stu-id="48d0b-928">Parameters - referenceField</span></span>

<span data-ttu-id="48d0b-929">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-929">value</span></span>  

### <a name="return-value---referencefield"></a><span data-ttu-id="48d0b-930">戻り値 - referenceField</span><span class="sxs-lookup"><span data-stu-id="48d0b-930">Return Value - referenceField</span></span>

## <a name="method-replacementfieldgroup"></a><span data-ttu-id="48d0b-931">メソッド replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="48d0b-931">Method replacementFieldGroup</span></span>

```xpp
public str replacementFieldGroup([str value])
```

### <a name="parameters---replacementfieldgroup"></a><span data-ttu-id="48d0b-932">パラメーター - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="48d0b-932">Parameters - replacementFieldGroup</span></span>

<span data-ttu-id="48d0b-933">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-933">value</span></span>  

### <a name="return-value---replacementfieldgroup"></a><span data-ttu-id="48d0b-934">戻り値 - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="48d0b-934">Return Value - replacementFieldGroup</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="48d0b-935">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="48d0b-935">Method securityKey</span></span>

<span data-ttu-id="48d0b-936">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-936">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="48d0b-937">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="48d0b-937">Parameters - securityKey</span></span>

<span data-ttu-id="48d0b-938">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-938">value</span></span>  
<span data-ttu-id="48d0b-939">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-939">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="48d0b-940">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="48d0b-940">Return Value - securityKey</span></span>

<span data-ttu-id="48d0b-941">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-941">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="48d0b-942">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="48d0b-942">Method showContextMenu</span></span>

<span data-ttu-id="48d0b-943">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-943">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="48d0b-944">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="48d0b-944">Parameters - showContextMenu</span></span>

<span data-ttu-id="48d0b-945">menuHandle</span><span class="sxs-lookup"><span data-stu-id="48d0b-945">menuHandle</span></span>  
<span data-ttu-id="48d0b-946">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="48d0b-946">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="48d0b-947">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="48d0b-947">Return Value - showContextMenu</span></span>

<span data-ttu-id="48d0b-948">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-948">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="48d0b-949">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="48d0b-949">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="48d0b-950">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="48d0b-950">Parameters - showLabel</span></span>

<span data-ttu-id="48d0b-951">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-951">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="48d0b-952">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="48d0b-952">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="48d0b-953">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="48d0b-953">Method skip</span></span>

<span data-ttu-id="48d0b-954">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-954">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="48d0b-955">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="48d0b-955">Parameters - skip</span></span>

<span data-ttu-id="48d0b-956">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-956">value</span></span>  
<span data-ttu-id="48d0b-957">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-957">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="48d0b-958">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="48d0b-958">Return Value - skip</span></span>

<span data-ttu-id="48d0b-959">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-959">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="48d0b-960">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="48d0b-960">Remarks - skip</span></span>

<span data-ttu-id="48d0b-961">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-961">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="48d0b-962">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="48d0b-962">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="48d0b-963">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="48d0b-963">Parameters - sort</span></span>

<span data-ttu-id="48d0b-964">sortDirection</span><span class="sxs-lookup"><span data-stu-id="48d0b-964">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="48d0b-965">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="48d0b-965">Return Value - sort</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="48d0b-966">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="48d0b-966">Method toolTip</span></span>

<span data-ttu-id="48d0b-967">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-967">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="48d0b-968">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="48d0b-968">Return Value - toolTip</span></span>

<span data-ttu-id="48d0b-969">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="48d0b-969">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="48d0b-970">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="48d0b-970">Remarks - toolTip</span></span>

<span data-ttu-id="48d0b-971">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-971">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="48d0b-972">メソッド top</span><span class="sxs-lookup"><span data-stu-id="48d0b-972">Method top</span></span>

<span data-ttu-id="48d0b-973">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-973">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="48d0b-974">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="48d0b-974">Parameters - top</span></span>

<span data-ttu-id="48d0b-975">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-975">value</span></span>  
<span data-ttu-id="48d0b-976">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-976">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="48d0b-977">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-977">mode</span></span>  
<span data-ttu-id="48d0b-978">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-978">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="48d0b-979">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="48d0b-979">Return Value - top</span></span>

<span data-ttu-id="48d0b-980">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="48d0b-980">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="48d0b-981">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-981">Method topMode</span></span>

<span data-ttu-id="48d0b-982">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-982">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="48d0b-983">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-983">Parameters - topMode</span></span>

<span data-ttu-id="48d0b-984">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-984">value</span></span>  
<span data-ttu-id="48d0b-985">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-985">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="48d0b-986">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-986">Return Value - topMode</span></span>

<span data-ttu-id="48d0b-987">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="48d0b-987">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="48d0b-988">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-988">Method topValue</span></span>

<span data-ttu-id="48d0b-989">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-989">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="48d0b-990">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-990">Parameters - topValue</span></span>

<span data-ttu-id="48d0b-991">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-991">value</span></span>  
<span data-ttu-id="48d0b-992">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-992">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="48d0b-993">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-993">Return Value - topValue</span></span>

<span data-ttu-id="48d0b-994">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="48d0b-994">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="48d0b-995">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="48d0b-995">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="48d0b-996">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="48d0b-996">Parameters - type</span></span>

<span data-ttu-id="48d0b-997">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-997">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="48d0b-998">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="48d0b-998">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="48d0b-999">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48d0b-999">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="48d0b-1000">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48d0b-1000">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="48d0b-1001">データ</span><span class="sxs-lookup"><span data-stu-id="48d0b-1001">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="48d0b-1002">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="48d0b-1002">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="48d0b-1003">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="48d0b-1003">Method userData</span></span>

<span data-ttu-id="48d0b-1004">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1004">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="48d0b-1005">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="48d0b-1005">Parameters - userData</span></span>

<span data-ttu-id="48d0b-1006">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1006">value</span></span>  
<span data-ttu-id="48d0b-1007">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1007">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="48d0b-1008">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="48d0b-1008">Return Value - userData</span></span>

<span data-ttu-id="48d0b-1009">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1009">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="48d0b-1010">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="48d0b-1010">Method userDataItem</span></span>

<span data-ttu-id="48d0b-1011">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1011">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="48d0b-1012">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="48d0b-1012">Parameters - userDataItem</span></span>

<span data-ttu-id="48d0b-1013">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1013">value</span></span>  
<span data-ttu-id="48d0b-1014">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1014">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="48d0b-1015">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="48d0b-1015">Return Value - userDataItem</span></span>

<span data-ttu-id="48d0b-1016">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1016">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="48d0b-1017">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="48d0b-1017">Method userDataItems</span></span>

<span data-ttu-id="48d0b-1018">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1018">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="48d0b-1019">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="48d0b-1019">Parameters - userDataItems</span></span>

<span data-ttu-id="48d0b-1020">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1020">value</span></span>  
<span data-ttu-id="48d0b-1021">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1021">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="48d0b-1022">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="48d0b-1022">Return Value - userDataItems</span></span>

<span data-ttu-id="48d0b-1023">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1023">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="48d0b-1024">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="48d0b-1024">Method userDisable</span></span>

<span data-ttu-id="48d0b-1025">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1025">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="48d0b-1026">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="48d0b-1026">Parameters - userDisable</span></span>

<span data-ttu-id="48d0b-1027">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1027">value</span></span>  
<span data-ttu-id="48d0b-1028">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1028">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="48d0b-1029">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="48d0b-1029">Return Value - userDisable</span></span>

<span data-ttu-id="48d0b-1030">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1030">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="48d0b-1031">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="48d0b-1031">Method userHeight</span></span>

<span data-ttu-id="48d0b-1032">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1032">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="48d0b-1033">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="48d0b-1033">Parameters - userHeight</span></span>

<span data-ttu-id="48d0b-1034">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1034">value</span></span>  
<span data-ttu-id="48d0b-1035">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1035">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="48d0b-1036">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="48d0b-1036">Return Value - userHeight</span></span>

<span data-ttu-id="48d0b-1037">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1037">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="48d0b-1038">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="48d0b-1038">Method userHide</span></span>

<span data-ttu-id="48d0b-1039">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1039">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="48d0b-1040">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="48d0b-1040">Parameters - userHide</span></span>

<span data-ttu-id="48d0b-1041">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1041">value</span></span>  
<span data-ttu-id="48d0b-1042">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1042">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="48d0b-1043">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="48d0b-1043">Return Value - userHide</span></span>

<span data-ttu-id="48d0b-1044">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1044">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="48d0b-1045">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="48d0b-1045">Remarks - userHide</span></span>

<span data-ttu-id="48d0b-1046">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1046">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="48d0b-1047">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1047">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="48d0b-1048">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1048">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="48d0b-1049">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="48d0b-1049">Method userOrgContainer</span></span>

<span data-ttu-id="48d0b-1050">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1050">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="48d0b-1051">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="48d0b-1051">Parameters - userOrgContainer</span></span>

<span data-ttu-id="48d0b-1052">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1052">value</span></span>  
<span data-ttu-id="48d0b-1053">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1053">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="48d0b-1054">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="48d0b-1054">Return Value - userOrgContainer</span></span>

<span data-ttu-id="48d0b-1055">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1055">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="48d0b-1056">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="48d0b-1056">Method userOrgSibling</span></span>

<span data-ttu-id="48d0b-1057">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1057">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="48d0b-1058">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="48d0b-1058">Parameters - userOrgSibling</span></span>

<span data-ttu-id="48d0b-1059">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1059">value</span></span>  
<span data-ttu-id="48d0b-1060">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1060">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="48d0b-1061">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="48d0b-1061">Return Value - userOrgSibling</span></span>

<span data-ttu-id="48d0b-1062">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1062">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="48d0b-1063">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="48d0b-1063">Method userPromptText</span></span>

<span data-ttu-id="48d0b-1064">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1064">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="48d0b-1065">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="48d0b-1065">Parameters - userPromptText</span></span>

<span data-ttu-id="48d0b-1066">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1066">value</span></span>  
<span data-ttu-id="48d0b-1067">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1067">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="48d0b-1068">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="48d0b-1068">Return Value - userPromptText</span></span>

<span data-ttu-id="48d0b-1069">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1069">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="48d0b-1070">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="48d0b-1070">Method userSecurityLevel</span></span>

<span data-ttu-id="48d0b-1071">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1071">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="48d0b-1072">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="48d0b-1072">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="48d0b-1073">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1073">value</span></span>  
<span data-ttu-id="48d0b-1074">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1074">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="48d0b-1075">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="48d0b-1075">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="48d0b-1076">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1076">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="48d0b-1077">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="48d0b-1077">Method userSkip</span></span>

<span data-ttu-id="48d0b-1078">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1078">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="48d0b-1079">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="48d0b-1079">Parameters - userSkip</span></span>

<span data-ttu-id="48d0b-1080">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1080">value</span></span>  
<span data-ttu-id="48d0b-1081">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1081">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="48d0b-1082">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1082">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="48d0b-1083">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="48d0b-1083">Return Value - userSkip</span></span>

<span data-ttu-id="48d0b-1084">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1084">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="48d0b-1085">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="48d0b-1085">Method userWidth</span></span>

<span data-ttu-id="48d0b-1086">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1086">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="48d0b-1087">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="48d0b-1087">Parameters - userWidth</span></span>

<span data-ttu-id="48d0b-1088">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1088">value</span></span>  
<span data-ttu-id="48d0b-1089">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1089">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="48d0b-1090">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="48d0b-1090">Return Value - userWidth</span></span>

<span data-ttu-id="48d0b-1091">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1091">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="48d0b-1092">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="48d0b-1092">Remarks - userWidth</span></span>

<span data-ttu-id="48d0b-1093">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1093">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="48d0b-1094">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1094">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="48d0b-1095">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1095">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="48d0b-1096">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="48d0b-1096">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="48d0b-1097">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="48d0b-1097">Return Value - validate</span></span>

## <a name="method-value"></a><span data-ttu-id="48d0b-1098">メソッド value</span><span class="sxs-lookup"><span data-stu-id="48d0b-1098">Method value</span></span>

```xpp
public Int64 value([Int64 value])
```

### <a name="parameters---value"></a><span data-ttu-id="48d0b-1099">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="48d0b-1099">Parameters - value</span></span>

<span data-ttu-id="48d0b-1100">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1100">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="48d0b-1101">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="48d0b-1101">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="48d0b-1102">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="48d0b-1102">Method verticalSpacing</span></span>

<span data-ttu-id="48d0b-1103">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1103">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="48d0b-1104">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="48d0b-1104">Parameters - verticalSpacing</span></span>

<span data-ttu-id="48d0b-1105">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1105">value</span></span>  
<span data-ttu-id="48d0b-1106">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1106">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1107">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-1107">mode</span></span>  
<span data-ttu-id="48d0b-1108">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1108">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="48d0b-1109">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="48d0b-1109">Return Value - verticalSpacing</span></span>

<span data-ttu-id="48d0b-1110">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1110">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="48d0b-1111">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1111">Method verticalSpacingMode</span></span>

<span data-ttu-id="48d0b-1112">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1112">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="48d0b-1113">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1113">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="48d0b-1114">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-1114">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="48d0b-1115">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1115">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="48d0b-1116">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1116">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="48d0b-1117">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-1117">Method verticalSpacingValue</span></span>

<span data-ttu-id="48d0b-1118">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1118">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="48d0b-1119">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-1119">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="48d0b-1120">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1120">value</span></span>  
<span data-ttu-id="48d0b-1121">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1121">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="48d0b-1122">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-1122">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="48d0b-1123">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1123">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="48d0b-1124">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1124">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="48d0b-1125">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1125">Parameters - viewEditMode</span></span>

<span data-ttu-id="48d0b-1126">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1126">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="48d0b-1127">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1127">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="48d0b-1128">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="48d0b-1128">Method visible</span></span>

<span data-ttu-id="48d0b-1129">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1129">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="48d0b-1130">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="48d0b-1130">Parameters - visible</span></span>

<span data-ttu-id="48d0b-1131">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1131">value</span></span>  
<span data-ttu-id="48d0b-1132">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1132">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="48d0b-1133">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="48d0b-1133">Return Value - visible</span></span>

<span data-ttu-id="48d0b-1134">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1134">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="48d0b-1135">メソッド width</span><span class="sxs-lookup"><span data-stu-id="48d0b-1135">Method width</span></span>

<span data-ttu-id="48d0b-1136">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1136">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="48d0b-1137">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="48d0b-1137">Parameters - width</span></span>

<span data-ttu-id="48d0b-1138">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1138">value</span></span>  
<span data-ttu-id="48d0b-1139">幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1139">An integer value that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1140">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-1140">mode</span></span>  
<span data-ttu-id="48d0b-1141">幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1141">An integer value that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="48d0b-1142">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="48d0b-1142">Return Value - width</span></span>

<span data-ttu-id="48d0b-1143">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1143">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="48d0b-1144">備考 - width</span><span class="sxs-lookup"><span data-stu-id="48d0b-1144">Remarks - width</span></span>

<span data-ttu-id="48d0b-1145">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1145">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="48d0b-1146">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1146">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="48d0b-1147">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-1147">Mode</span></span>           | <span data-ttu-id="48d0b-1148">幅計算</span><span class="sxs-lookup"><span data-stu-id="48d0b-1148">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d0b-1149">-1 正確</span><span class="sxs-lookup"><span data-stu-id="48d0b-1149">-1 Exact</span></span>       | <span data-ttu-id="48d0b-1150">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1150">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48d0b-1151">0 自動</span><span class="sxs-lookup"><span data-stu-id="48d0b-1151">0 Auto</span></span>         | <span data-ttu-id="48d0b-1152">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1152">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48d0b-1153">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="48d0b-1153">1 Column width</span></span> | <span data-ttu-id="48d0b-1154">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1154">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="48d0b-1155">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1155">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="48d0b-1156">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1156">Method widthMode</span></span>

<span data-ttu-id="48d0b-1157">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1157">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="48d0b-1158">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1158">Parameters - widthMode</span></span>

<span data-ttu-id="48d0b-1159">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1159">value</span></span>  
<span data-ttu-id="48d0b-1160">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1160">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="48d0b-1161">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1161">Return Value - widthMode</span></span>

<span data-ttu-id="48d0b-1162">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1162">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="48d0b-1163">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1163">Remarks - widthMode</span></span>

<span data-ttu-id="48d0b-1164">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1164">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="48d0b-1165">モード</span><span class="sxs-lookup"><span data-stu-id="48d0b-1165">Mode</span></span>         | <span data-ttu-id="48d0b-1166">幅計算</span><span class="sxs-lookup"><span data-stu-id="48d0b-1166">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d0b-1167">正確</span><span class="sxs-lookup"><span data-stu-id="48d0b-1167">Exact</span></span>        | <span data-ttu-id="48d0b-1168">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1168">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="48d0b-1169">自動</span><span class="sxs-lookup"><span data-stu-id="48d0b-1169">Auto</span></span>         | <span data-ttu-id="48d0b-1170">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1170">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="48d0b-1171">列の幅</span><span class="sxs-lookup"><span data-stu-id="48d0b-1171">Column width</span></span> | <span data-ttu-id="48d0b-1172">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1172">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="48d0b-1173">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1173">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="48d0b-1174">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-1174">Method widthValue</span></span>

<span data-ttu-id="48d0b-1175">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1175">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="48d0b-1176">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-1176">Parameters - widthValue</span></span>

<span data-ttu-id="48d0b-1177">値</span><span class="sxs-lookup"><span data-stu-id="48d0b-1177">value</span></span>  
<span data-ttu-id="48d0b-1178">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1178">An integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="48d0b-1179">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-1179">Return Value - widthValue</span></span>

<span data-ttu-id="48d0b-1180">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1180">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="48d0b-1181">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="48d0b-1181">Remarks - widthValue</span></span>

<span data-ttu-id="48d0b-1182">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1182">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-ongotfocus"></a><span data-ttu-id="48d0b-1183">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="48d0b-1183">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="48d0b-1184">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="48d0b-1184">Parameters - OnGotFocus</span></span>

<span data-ttu-id="48d0b-1185">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1185">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1186">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1186">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="48d0b-1187">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="48d0b-1187">Method lostFocus</span></span>

<span data-ttu-id="48d0b-1188">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1188">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-onenter"></a><span data-ttu-id="48d0b-1189">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="48d0b-1189">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="48d0b-1190">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="48d0b-1190">Parameters - OnEnter</span></span>

<span data-ttu-id="48d0b-1191">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1191">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1192">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1192">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="48d0b-1193">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="48d0b-1193">Method displayControl</span></span>

<span data-ttu-id="48d0b-1194">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1194">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-gotfocus"></a><span data-ttu-id="48d0b-1195">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="48d0b-1195">Method gotFocus</span></span>

<span data-ttu-id="48d0b-1196">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1196">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-undo"></a><span data-ttu-id="48d0b-1197">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="48d0b-1197">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="48d0b-1198">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="48d0b-1198">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="48d0b-1199">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="48d0b-1199">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="48d0b-1200">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="48d0b-1200">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1201">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="48d0b-1201">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1202">overrideObject</span><span class="sxs-lookup"><span data-stu-id="48d0b-1202">overrideObject</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="48d0b-1203">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="48d0b-1203">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="48d0b-1204">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="48d0b-1204">Parameters - OnValidated</span></span>

<span data-ttu-id="48d0b-1205">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1205">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1206">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1206">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="48d0b-1207">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="48d0b-1207">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-enter"></a><span data-ttu-id="48d0b-1208">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="48d0b-1208">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-setfocus"></a><span data-ttu-id="48d0b-1209">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="48d0b-1209">Method setFocus</span></span>

<span data-ttu-id="48d0b-1210">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1210">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-drop"></a><span data-ttu-id="48d0b-1211">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="48d0b-1211">Method drop</span></span>

<span data-ttu-id="48d0b-1212">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1212">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="48d0b-1213">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="48d0b-1213">Parameters - drop</span></span>

<span data-ttu-id="48d0b-1214">dragSource</span><span class="sxs-lookup"><span data-stu-id="48d0b-1214">dragSource</span></span>  
<span data-ttu-id="48d0b-1215">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1215">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1216">dragMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1216">dragMode</span></span>  
<span data-ttu-id="48d0b-1217">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1217">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1218">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-1218">x</span></span>  
<span data-ttu-id="48d0b-1219">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1219">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1220">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-1220">y</span></span>  
<span data-ttu-id="48d0b-1221">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1221">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="48d0b-1222">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="48d0b-1222">Method dragLeave</span></span>

<span data-ttu-id="48d0b-1223">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1223">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-cut"></a><span data-ttu-id="48d0b-1224">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="48d0b-1224">Method cut</span></span>

<span data-ttu-id="48d0b-1225">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1225">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-lookup"></a><span data-ttu-id="48d0b-1226">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="48d0b-1226">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-onmodified"></a><span data-ttu-id="48d0b-1227">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="48d0b-1227">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="48d0b-1228">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="48d0b-1228">Parameters - OnModified</span></span>

<span data-ttu-id="48d0b-1229">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1229">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1230">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1230">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="48d0b-1231">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-1231">Method prefColumnSize</span></span>

<span data-ttu-id="48d0b-1232">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1232">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="48d0b-1233">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="48d0b-1233">Parameters - prefColumnSize</span></span>

<span data-ttu-id="48d0b-1234">width</span><span class="sxs-lookup"><span data-stu-id="48d0b-1234">width</span></span>  
<span data-ttu-id="48d0b-1235">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1235">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1236">height</span><span class="sxs-lookup"><span data-stu-id="48d0b-1236">height</span></span>  
<span data-ttu-id="48d0b-1237">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1237">The preferred height of the control.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="48d0b-1238">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="48d0b-1238">Method resetUserSetting</span></span>

<span data-ttu-id="48d0b-1239">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1239">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-filter"></a><span data-ttu-id="48d0b-1240">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="48d0b-1240">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="48d0b-1241">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="48d0b-1241">Parameters - filter</span></span>

<span data-ttu-id="48d0b-1242">filterStr</span><span class="sxs-lookup"><span data-stu-id="48d0b-1242">filterStr</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="48d0b-1243">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="48d0b-1243">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="48d0b-1244">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="48d0b-1244">Parameters - OnLeaving</span></span>

<span data-ttu-id="48d0b-1245">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1245">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1246">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1246">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="48d0b-1247">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-1247">Method dropEx</span></span>

<span data-ttu-id="48d0b-1248">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1248">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="48d0b-1249">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="48d0b-1249">Parameters - dropEx</span></span>

<span data-ttu-id="48d0b-1250">dragSource</span><span class="sxs-lookup"><span data-stu-id="48d0b-1250">dragSource</span></span>  
<span data-ttu-id="48d0b-1251">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1251">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1252">dragMode</span><span class="sxs-lookup"><span data-stu-id="48d0b-1252">dragMode</span></span>  
<span data-ttu-id="48d0b-1253">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1253">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1254">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-1254">x</span></span>  
<span data-ttu-id="48d0b-1255">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1255">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1256">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-1256">y</span></span>  
<span data-ttu-id="48d0b-1257">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1257">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onvalidating"></a><span data-ttu-id="48d0b-1258">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="48d0b-1258">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="48d0b-1259">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="48d0b-1259">Parameters - OnValidating</span></span>

<span data-ttu-id="48d0b-1260">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1260">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1261">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1261">e</span></span>  

## <a name="method-mouseenter"></a><span data-ttu-id="48d0b-1262">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="48d0b-1262">Method mouseEnter</span></span>

<span data-ttu-id="48d0b-1263">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1263">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="48d0b-1264">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="48d0b-1264">Parameters - mouseEnter</span></span>

<span data-ttu-id="48d0b-1265">x</span><span class="sxs-lookup"><span data-stu-id="48d0b-1265">x</span></span>  
<span data-ttu-id="48d0b-1266">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1266">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1267">y</span><span class="sxs-lookup"><span data-stu-id="48d0b-1267">y</span></span>  
<span data-ttu-id="48d0b-1268">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1268">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1269">ボタン</span><span class="sxs-lookup"><span data-stu-id="48d0b-1269">button</span></span>  
<span data-ttu-id="48d0b-1270">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1270">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1271">Ctrl</span><span class="sxs-lookup"><span data-stu-id="48d0b-1271">Ctrl</span></span>  
<span data-ttu-id="48d0b-1272">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1272">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="48d0b-1273">シフト</span><span class="sxs-lookup"><span data-stu-id="48d0b-1273">Shift</span></span>  
<span data-ttu-id="48d0b-1274">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1274">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="48d0b-1275">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="48d0b-1275">Method endDrag</span></span>

<span data-ttu-id="48d0b-1276">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1276">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="48d0b-1277">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="48d0b-1277">Remarks - endDrag</span></span>

<span data-ttu-id="48d0b-1278">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1278">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="48d0b-1279">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1279">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-copy"></a><span data-ttu-id="48d0b-1280">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="48d0b-1280">Method copy</span></span>

<span data-ttu-id="48d0b-1281">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1281">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-mouseleave"></a><span data-ttu-id="48d0b-1282">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="48d0b-1282">Method mouseLeave</span></span>

<span data-ttu-id="48d0b-1283">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1283">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-context"></a><span data-ttu-id="48d0b-1284">メソッド context</span><span class="sxs-lookup"><span data-stu-id="48d0b-1284">Method context</span></span>

<span data-ttu-id="48d0b-1285">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1285">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="48d0b-1286">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="48d0b-1286">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="48d0b-1287">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="48d0b-1287">Parameters - OnLostFocus</span></span>

<span data-ttu-id="48d0b-1288">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1288">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1289">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1289">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="48d0b-1290">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="48d0b-1290">Method paste</span></span>

<span data-ttu-id="48d0b-1291">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1291">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-inputsearch"></a><span data-ttu-id="48d0b-1292">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="48d0b-1292">Method inputSearch</span></span>

<span data-ttu-id="48d0b-1293">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1293">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="48d0b-1294">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="48d0b-1294">Parameters - inputSearch</span></span>

<span data-ttu-id="48d0b-1295">searchStr</span><span class="sxs-lookup"><span data-stu-id="48d0b-1295">searchStr</span></span>  
<span data-ttu-id="48d0b-1296">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="48d0b-1296">The string value to use to filter data; optional.</span></span>

## <a name="method-onlookup"></a><span data-ttu-id="48d0b-1297">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="48d0b-1297">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="48d0b-1298">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="48d0b-1298">Parameters - OnLookup</span></span>

<span data-ttu-id="48d0b-1299">sender</span><span class="sxs-lookup"><span data-stu-id="48d0b-1299">sender</span></span>  

<!-- -->

<span data-ttu-id="48d0b-1300">e</span><span class="sxs-lookup"><span data-stu-id="48d0b-1300">e</span></span>  

