---
title: FormComboBoxControl クラス
description: このトピックでは、FormComboBoxControl クラスについて説明します。
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
ms.openlocfilehash: 6326f4b91792c0232349ed443bf13913db319e1c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502952"
---
# <a name="class-formcomboboxcontrol"></a><span data-ttu-id="31131-103">クラス FormComboBoxControl</span><span class="sxs-lookup"><span data-stu-id="31131-103">Class FormComboBoxControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormComboBoxControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="31131-104">備考</span><span class="sxs-lookup"><span data-stu-id="31131-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="31131-105">例</span><span class="sxs-lookup"><span data-stu-id="31131-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="31131-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="31131-106">Methods</span></span>

| <span data-ttu-id="31131-107">方法</span><span class="sxs-lookup"><span data-stu-id="31131-107">Method</span></span>                                                                                                      | <span data-ttu-id="31131-108">説明</span><span class="sxs-lookup"><span data-stu-id="31131-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31131-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="31131-110">コントロールを他のコントロールと揃える必要があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-110">Determines whether the control should be aligned with other controls.</span></span>                                                                                                   |
| <span data-ttu-id="31131-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="31131-112">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-112">Determines whether the user can modify the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="31131-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="31131-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="31131-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="31131-115">public boolean appendNew(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-115">public boolean appendNew(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="31131-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="31131-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="31131-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="31131-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="31131-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="31131-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="31131-122">コントロール� のバックグラウンドを透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-122">Determines whether the control�s background can be transparent.</span></span>                                                                                                         |
| <span data-ttu-id="31131-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31131-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="31131-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="31131-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="31131-126">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-126">Gets or sets the weight of font that is used to display text in the control.</span></span>                                                                                            |
| <span data-ttu-id="31131-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="31131-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-128">Gets or sets the style of the border line for the control.</span></span>                                                                                                              |
| <span data-ttu-id="31131-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="31131-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="31131-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="31131-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="31131-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="31131-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-133">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="31131-134">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-134">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="31131-135">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-135">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="31131-136">public int comboType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-136">public int comboType(\[int value\])</span></span>                                                                         | <span data-ttu-id="31131-137">コントロールのコンボ ボックスのタイプを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-137">Sets or returns the type of combo box for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="31131-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="31131-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="31131-139">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-139">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="31131-140">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="31131-140">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="31131-141">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-141">Returns a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                          |
| <span data-ttu-id="31131-142">public int count()</span><span class="sxs-lookup"><span data-stu-id="31131-142">public int count()</span></span>                                                                                          | <span data-ttu-id="31131-143">コンボ ボックス コントロール内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-143">Returns the number of items in the combo box control.</span></span>                                                                                                                   |
| <span data-ttu-id="31131-144">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-144">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="31131-145">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-145">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="31131-146">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="31131-146">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="31131-147">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="31131-147">public FieldId dataField(\[FieldId value\])</span></span>                                                                 | <span data-ttu-id="31131-148">コンボ ボックス コントロールのデータ フィールドを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-148">Sets or returns the data field for the combo box control.</span></span>                                                                                                               |
| <span data-ttu-id="31131-149">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-149">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="31131-150">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-150">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="31131-151">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-151">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="31131-152">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="31131-152">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="31131-153">コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-153">Gets or sets a data source that should be used by the control or the form.</span></span>                                                                                              |
| <span data-ttu-id="31131-154">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-154">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="31131-155">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-155">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="31131-156">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-156">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="31131-157">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-157">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="31131-158">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-158">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="31131-159">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-159">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="31131-160">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-160">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>                                                                                    |
| <span data-ttu-id="31131-161">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31131-161">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="31131-162">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-162">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="31131-163">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31131-163">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="31131-164">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-164">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="31131-165">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="31131-165">public str dragText()</span></span>                                                                                       | <span data-ttu-id="31131-166">フォーム コンボ ボックス コントロールをドラッグしたときに表示されるテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-166">Returns the text that is displayed when the form combo box control is dragged.</span></span>                                                                                          |
| <span data-ttu-id="31131-167">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-167">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="31131-168">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-168">Determines whether the object is enabled or disabled.</span></span>                                                                                                                   |
| <span data-ttu-id="31131-169">public EnumId enumType(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="31131-169">public EnumId enumType(\[EnumId value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-170">public EnumId enumTypeValue()</span><span class="sxs-lookup"><span data-stu-id="31131-170">public EnumId enumTypeValue()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="31131-171">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="31131-171">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="31131-172">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-172">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-173">public int find(str string)</span><span class="sxs-lookup"><span data-stu-id="31131-173">public int find(str string)</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="31131-174">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-174">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="31131-175">コントロールに使用するフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-175">Gets or sets the name of the font that should be used for the control.</span></span>                                                                                                  |
| <span data-ttu-id="31131-176">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-176">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="31131-177">コントロールに使用するフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-177">Gets or sets the size of the font that should be used for the control.</span></span>                                                                                                  |
| <span data-ttu-id="31131-178">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-178">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="31131-179">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-179">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="31131-180">public str getEditText()</span><span class="sxs-lookup"><span data-stu-id="31131-180">public str getEditText()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-181">public str getText(int index)</span><span class="sxs-lookup"><span data-stu-id="31131-181">public str getText(int index)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="31131-182">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="31131-182">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="31131-183">フォーム コンボ ボックス コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-183">Sets or returns a value that indicates whether the contents of the form combo box control have changed.</span></span>                                                                 |
| <span data-ttu-id="31131-184">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="31131-184">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="31131-185">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-185">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="31131-186">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-186">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="31131-187">ピクセル単位でコントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-187">Gets or sets the height of the control in pixels.</span></span>                                                                                                                       |
| <span data-ttu-id="31131-188">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-188">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="31131-189">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-189">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="31131-190">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-190">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="31131-191">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-191">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="31131-192">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="31131-192">public str helpField()</span></span>                                                                                      | <span data-ttu-id="31131-193">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-193">Returns the Help text for the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="31131-194">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-194">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="31131-195">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-195">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>                                                         |
| <span data-ttu-id="31131-196">public boolean hideFirstEntry(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-196">public boolean hideFirstEntry(\[boolean value\])</span></span>                                                            | <span data-ttu-id="31131-197">コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-197">Sets or returns a value that indicates whether the first entry in the combo box control is hidden.</span></span>                                                                      |
| <span data-ttu-id="31131-198">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-198">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="31131-199">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-199">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="31131-200">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="31131-200">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="31131-201">コントロールの Windows ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-201">Returns the Windows handle for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="31131-202">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="31131-202">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="31131-203">コントロールがコンテナーかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-203">Returns a value that indicates whether the control is a container.</span></span>                                                                                                      |
| <span data-ttu-id="31131-204">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="31131-204">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="31131-205">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-205">Returns a value that indicates whether the control is displayed.</span></span>                                                                                                        |
| <span data-ttu-id="31131-206">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="31131-206">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="31131-207">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-207">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="31131-208">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="31131-208">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="31131-209">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-209">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="31131-210">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="31131-210">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-211">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-211">public boolean italic(\[boolean value\])</span></span>                                                                    | <span data-ttu-id="31131-212">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-212">Sets or returns a value that indicates whether the text in the control is italic.</span></span>                                                                                       |
| <span data-ttu-id="31131-213">public int item(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-213">public int item(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="31131-214">public int items(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-214">public int items(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="31131-215">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-215">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="31131-216">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-216">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="31131-217">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-217">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-218">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-218">public int labelBold(\[int value\])</span></span>                                                                         | <span data-ttu-id="31131-219">コントロールのラベルの太字設定を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-219">Sets or returns a value that indicates the bold setting for the label in the control.</span></span>                                                                                   |
| <span data-ttu-id="31131-220">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-220">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="31131-221">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-221">public str labelFont(\[str value\])</span></span>                                                                         | <span data-ttu-id="31131-222">フォーム コンボ ボックス コントロールのラベル テキストのフォントを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-222">Sets or returns a font for the label text in a form combo box control.</span></span>                                                                                                  |
| <span data-ttu-id="31131-223">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-223">public int labelFontSize(\[int value\])</span></span>                                                                     | <span data-ttu-id="31131-224">フォーム コンボ ボックス コントロールのラベル テキストのフォント サイズをポイント単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-224">Sets or returns the font size in points for the label text in a form combo box control.</span></span>                                                                                 |
| <span data-ttu-id="31131-225">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-225">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="31131-226">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-226">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="31131-227">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-227">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="31131-228">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-228">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="31131-229">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-229">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="31131-230">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-230">public boolean labelItalic(\[boolean value\])</span></span>                                                               | <span data-ttu-id="31131-231">コントロールのラベルのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-231">Sets or returns a value that indicates whether the text in the label of the control is italic.</span></span>                                                                          |
| <span data-ttu-id="31131-232">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-232">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        | <span data-ttu-id="31131-233">コントロールのラベルがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-233">Is called when the label for the control is double-clicked by the user.</span></span>                                                                                                 |
| <span data-ttu-id="31131-234">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-234">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            | <span data-ttu-id="31131-235">ユーザーがコントロールのラベル上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-235">Is called when the user clicks the mouse button over the label for the control.</span></span>                                                                                         |
| <span data-ttu-id="31131-236">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-236">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              | <span data-ttu-id="31131-237">ユーザーがコントロールのラベル上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-237">Is called when the user releases the mouse button over the label for the control.</span></span>                                                                                       |
| <span data-ttu-id="31131-238">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-238">public int labelPosition(\[int value\])</span></span>                                                                     | <span data-ttu-id="31131-239">コントロールのラベルの位置を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-239">Sets or returns the position of the label for the control.</span></span>                                                                                                              |
| <span data-ttu-id="31131-240">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-240">public boolean labelUnderline(\[boolean value\])</span></span>                                                            | <span data-ttu-id="31131-241">コントロールのラベルのテキストが下線付きで表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-241">Sets or returns a value that indicates whether the text in the label of the control is underlined.</span></span>                                                                      |
| <span data-ttu-id="31131-242">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-242">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="31131-243">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-243">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-244">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-244">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="31131-245">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="31131-245">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="31131-246">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-246">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="31131-247">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-247">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="31131-248">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-248">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="31131-249">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-249">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="31131-250">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-250">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="31131-251">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-251">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="31131-252">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-252">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="31131-253">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="31131-253">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="31131-254">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="31131-254">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="31131-255">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-255">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="31131-256">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-256">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="31131-257">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-257">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="31131-258">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-258">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="31131-259">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-259">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="31131-260">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-260">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="31131-261">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-261">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="31131-262">ユーザーがコントロール上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-262">Is called when the user releases the mouse button over the control.</span></span>                                                                                                     |
| <span data-ttu-id="31131-263">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-263">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="31131-264">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-264">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="31131-265">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-265">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="31131-266">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="31131-266">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="31131-267">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="31131-267">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="31131-268">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-268">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="31131-269">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-269">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-270">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-270">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="31131-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="31131-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="31131-272">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-272">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="31131-273">public int selection(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-273">public int selection(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="31131-274">public int selectionChange()</span><span class="sxs-lookup"><span data-stu-id="31131-274">public int selectionChange()</span></span>                                                                                | <span data-ttu-id="31131-275">ユーザーがコンボ ボックス コントロールで選択した項目を変更したことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-275">Indicates that the user has changed the selected item in the combo box control.</span></span>                                                                                         |
| <span data-ttu-id="31131-276">public int selectText(str string)</span><span class="sxs-lookup"><span data-stu-id="31131-276">public int selectText(str string)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="31131-277">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="31131-277">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="31131-278">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-278">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="31131-279">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-279">public boolean showLabel(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="31131-280">コントロールのラベルがフォームに表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-280">Sets or returns a value that indicates whether the label for the control is displayed in the form.</span></span>                                                                      |
| <span data-ttu-id="31131-281">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-281">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="31131-282">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-282">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="31131-283">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="31131-283">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="31131-284">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-284">public str text(\[str value\])</span></span>                                                                              | <span data-ttu-id="31131-285">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-285">Sets or returns the text for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="31131-286">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="31131-286">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="31131-287">コントロールのツールヒント テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-287">Returns the tooltip text for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="31131-288">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-288">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="31131-289">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-289">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="31131-290">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-290">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="31131-291">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-291">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="31131-292">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-292">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="31131-293">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-293">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="31131-294">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-294">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="31131-295">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-295">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="31131-296">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-296">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="31131-297">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="31131-297">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="31131-298">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-298">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="31131-299">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-299">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="31131-300">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-300">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="31131-301">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-301">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="31131-302">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-302">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="31131-303">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-303">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="31131-304">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-304">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="31131-305">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-305">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="31131-306">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-306">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="31131-307">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-307">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="31131-308">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-308">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="31131-309">フォーム コンボ ボックス コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-309">Returns or sets the value that indicates whether the form combo box control is hidden from the user.</span></span>                                                                    |
| <span data-ttu-id="31131-310">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-310">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="31131-311">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-311">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="31131-312">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-312">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="31131-313">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-313">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="31131-314">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31131-314">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="31131-315">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-315">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="31131-316">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-316">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="31131-317">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-317">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="31131-318">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-318">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="31131-319">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コンボ ボックス コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-319">Sets or returns the value that indicates whether the form combo box control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>          |
| <span data-ttu-id="31131-320">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-320">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="31131-321">ピクセル単位でフォーム コンボ ボックス コントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-321">Sets or returns the width of the form combo box control in pixels.</span></span>                                                                                                      |
| <span data-ttu-id="31131-322">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="31131-322">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="31131-323">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-323">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="31131-324">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-324">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="31131-325">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-325">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="31131-326">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-326">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="31131-327">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-327">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="31131-328">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-328">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="31131-329">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-329">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="31131-330">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31131-330">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="31131-331">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-331">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="31131-332">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="31131-332">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="31131-333">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-333">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="31131-334">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-334">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="31131-335">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-335">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="31131-336">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31131-336">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="31131-337">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-337">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="31131-338">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="31131-338">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="31131-339">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="31131-339">public void displayControl()</span></span>                                                                                | <span data-ttu-id="31131-340">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-340">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="31131-341">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-341">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="31131-342">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="31131-342">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="31131-343">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-343">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="31131-344">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="31131-344">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="31131-345">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="31131-345">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="31131-346">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-346">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="31131-347">public void context()</span><span class="sxs-lookup"><span data-stu-id="31131-347">public void context()</span></span>                                                                                       | <span data-ttu-id="31131-348">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-348">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="31131-349">public void beginUpdate()</span><span class="sxs-lookup"><span data-stu-id="31131-349">public void beginUpdate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="31131-350">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-350">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="31131-351">public void setEditText(str string)</span><span class="sxs-lookup"><span data-stu-id="31131-351">public void setEditText(str string)</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="31131-352">public void enter()</span><span class="sxs-lookup"><span data-stu-id="31131-352">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="31131-353">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="31131-353">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="31131-354">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="31131-354">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="31131-355">public void paste()</span><span class="sxs-lookup"><span data-stu-id="31131-355">public void paste()</span></span>                                                                                         | <span data-ttu-id="31131-356">フォーム コンボ ボックス コントロールをフォームに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="31131-356">Pastes the form combo box control into the form.</span></span>                                                                                                                        |
| <span data-ttu-id="31131-357">public void clear()</span><span class="sxs-lookup"><span data-stu-id="31131-357">public void clear()</span></span>                                                                                         | <span data-ttu-id="31131-358">コンボ ボックス リストのエントリをクリアします。</span><span class="sxs-lookup"><span data-stu-id="31131-358">Clears the entries in the combo box list.</span></span>                                                                                                                               |
| <span data-ttu-id="31131-359">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="31131-359">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="31131-360">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-360">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="31131-361">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-361">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="31131-362">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31131-362">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="31131-363">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-363">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="31131-364">public void copy()</span><span class="sxs-lookup"><span data-stu-id="31131-364">public void copy()</span></span>                                                                                          | <span data-ttu-id="31131-365">フォームのコンボ ボックス コントロールをコピーします。</span><span class="sxs-lookup"><span data-stu-id="31131-365">Copies the form combo box control.</span></span>                                                                                                                                      |
| <span data-ttu-id="31131-366">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-366">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="31131-367">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="31131-367">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="31131-368">ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-368">Is called when the user has finished dragging a form combo box control.</span></span>                                                                                                 |
| <span data-ttu-id="31131-369">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="31131-369">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="31131-370">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="31131-370">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="31131-371">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-371">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="31131-372">public void insert(str string, int index)</span><span class="sxs-lookup"><span data-stu-id="31131-372">public void insert(str string, int index)</span></span>                                                                   | <span data-ttu-id="31131-373">指定した位置にあるコンボ ボックスに文字列の値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="31131-373">Inserts a string value into the combo box list at the specified position.</span></span>                                                                                               |
| <span data-ttu-id="31131-374">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="31131-374">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="31131-375">ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-375">Is called when the user moves the mouse pointer into the control.</span></span>                                                                                                       |
| <span data-ttu-id="31131-376">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-376">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="31131-377">public void delete(str string)</span><span class="sxs-lookup"><span data-stu-id="31131-377">public void delete(str string)</span></span>                                                                              | <span data-ttu-id="31131-378">コンボ ボックスのリストから文字列値を削除します。</span><span class="sxs-lookup"><span data-stu-id="31131-378">Removes a string value from the combo box list.</span></span>                                                                                                                         |
| <span data-ttu-id="31131-379">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="31131-379">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="31131-380">public void add(str string)</span><span class="sxs-lookup"><span data-stu-id="31131-380">public void add(str string)</span></span>                                                                                 | <span data-ttu-id="31131-381">コンボ ボックス リストに文字列値を追加します。</span><span class="sxs-lookup"><span data-stu-id="31131-381">Adds a string value to the combo box list.</span></span>                                                                                                                              |
| <span data-ttu-id="31131-382">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="31131-382">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="31131-383">フォーム コンボ ボックス コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="31131-383">Specifies the preferred column width and height for the form combo box control.</span></span>                                                                                         |
| <span data-ttu-id="31131-384">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-384">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="31131-385">public void undo()</span><span class="sxs-lookup"><span data-stu-id="31131-385">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="31131-386">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="31131-386">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="31131-387">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-387">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                         |                                                                                                                                                                         |
| <span data-ttu-id="31131-388">public void endUpdate()</span><span class="sxs-lookup"><span data-stu-id="31131-388">public void endUpdate()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="31131-389">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="31131-389">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="31131-390">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-390">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="31131-391">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="31131-391">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="31131-392">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-392">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="31131-393">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-393">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="31131-394">public void cut()</span><span class="sxs-lookup"><span data-stu-id="31131-394">public void cut()</span></span>                                                                                           | <span data-ttu-id="31131-395">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="31131-395">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="31131-396">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="31131-396">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="31131-397">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-397">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="31131-398">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="31131-398">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="31131-399">public void setDropSize(\[int lines\])</span><span class="sxs-lookup"><span data-stu-id="31131-399">public void setDropSize(\[int lines\])</span></span>                                                                      |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="31131-400">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="31131-400">Method alignControl</span></span>

<span data-ttu-id="31131-401">コントロールを他のコントロールと揃える必要があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-401">Determines whether the control should be aligned with other controls.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="31131-402">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="31131-402">Parameters - alignControl</span></span>

<span data-ttu-id="31131-403">値</span><span class="sxs-lookup"><span data-stu-id="31131-403">value</span></span>  
<span data-ttu-id="31131-404">フォーム コンボ ボックス コントロールが他のコントロールと一致しているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-404">A Boolean value that indicates whether the form combo box control is aligned with other controls; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="31131-405">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="31131-405">Return Value - alignControl</span></span>

<span data-ttu-id="31131-406">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-406">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="31131-407">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="31131-407">Remarks - alignControl</span></span>

<span data-ttu-id="31131-408">コントロールの左上隅は、最も長いラベルに基づいて配置されます。</span><span class="sxs-lookup"><span data-stu-id="31131-408">The upper-left corner of the control is aligned based on the longest label.</span></span>

### <a name="examples---aligncontrol"></a><span data-ttu-id="31131-409">例 - alignControl</span><span class="sxs-lookup"><span data-stu-id="31131-409">Examples - alignControl</span></span>

<span data-ttu-id="31131-410">次の例は、最も長いラベルの長さに基づいて、フォーム コンボ ボックス コントロールを他のコントロールと揃えるための alignControl メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-410">The following example shows a call to the alignControl method to align a form combo box control with other controls, based on the length of the longest label.</span></span>

```xpp
boolean bAlign; 
// The combo variable was previously assigned 
// as a FormComboBoxControl type. 
// Retrieve the alignControl property. 
bAlign = combo.alignControl(); 
// Set the alignControl property. 
combo.alignControl(false);
```

## <a name="method-allowedit"></a><span data-ttu-id="31131-411">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="31131-411">Method allowEdit</span></span>

<span data-ttu-id="31131-412">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-412">Determines whether the user can modify the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="31131-413">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="31131-413">Parameters - allowEdit</span></span>

<span data-ttu-id="31131-414">値</span><span class="sxs-lookup"><span data-stu-id="31131-414">value</span></span>  
<span data-ttu-id="31131-415">allowEdit プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-415">The value to assign to the allowEdit property; optional.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="31131-416">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="31131-416">Return Value - allowEdit</span></span>

<span data-ttu-id="31131-417">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-417">true if the control can be modified; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="31131-418">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="31131-418">Remarks - allowEdit</span></span>

<span data-ttu-id="31131-419">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="31131-419">If this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

### <a name="examples---allowedit"></a><span data-ttu-id="31131-420">例 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="31131-420">Examples - allowEdit</span></span>

<span data-ttu-id="31131-421">次の例は、allowEdit プロパティの値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-421">The following example shows how to return and set the value of the allowEdit property.</span></span>

```xpp
// Return the value. 
info (strfmt("allowEdit: %1", this.allowEdit())); 
// Set the value. 
this.allowEdit(false);
```

## <a name="method-allowsyssetup"></a><span data-ttu-id="31131-422">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="31131-422">Method allowSysSetup</span></span>

<span data-ttu-id="31131-423">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-423">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="31131-424">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="31131-424">Return Value - allowSysSetup</span></span>

<span data-ttu-id="31131-425">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-425">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-appendnew"></a><span data-ttu-id="31131-426">メソッド appendNew</span><span class="sxs-lookup"><span data-stu-id="31131-426">Method appendNew</span></span>

```xpp
public boolean appendNew([boolean value])
```

### <a name="parameters---appendnew"></a><span data-ttu-id="31131-427">パラメーター - appendNew</span><span class="sxs-lookup"><span data-stu-id="31131-427">Parameters - appendNew</span></span>

<span data-ttu-id="31131-428">値</span><span class="sxs-lookup"><span data-stu-id="31131-428">value</span></span>  

### <a name="return-value---appendnew"></a><span data-ttu-id="31131-429">戻り値 - appendNew</span><span class="sxs-lookup"><span data-stu-id="31131-429">Return Value - appendNew</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="31131-430">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="31131-430">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="31131-431">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="31131-431">Parameters - arrayIndex</span></span>

<span data-ttu-id="31131-432">値</span><span class="sxs-lookup"><span data-stu-id="31131-432">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="31131-433">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="31131-433">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="31131-434">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="31131-434">Method autoDeclaration</span></span>

<span data-ttu-id="31131-435">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-435">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="31131-436">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="31131-436">Parameters - autoDeclaration</span></span>

<span data-ttu-id="31131-437">値</span><span class="sxs-lookup"><span data-stu-id="31131-437">value</span></span>  
<span data-ttu-id="31131-438">autoDeclaration プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-438">The value to assign to the autoDeclaration property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="31131-439">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="31131-439">Return Value - autoDeclaration</span></span>

<span data-ttu-id="31131-440">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-440">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="31131-441">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="31131-441">Remarks - autoDeclaration</span></span>

<span data-ttu-id="31131-442">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="31131-442">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="31131-443">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-443">Method backgroundColor</span></span>

<span data-ttu-id="31131-444">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-444">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="31131-445">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-445">Parameters - backgroundColor</span></span>

<span data-ttu-id="31131-446">値</span><span class="sxs-lookup"><span data-stu-id="31131-446">value</span></span>  
<span data-ttu-id="31131-447">コントロールの背景色として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-447">The value to assign as the background color of the control; optional.</span></span> <span data-ttu-id="31131-448">これは、コントロール� の配色または Winapi::RGB2int 値のいずれかの値にできます。</span><span class="sxs-lookup"><span data-stu-id="31131-448">This can be one of the values from the control�s color scheme or a Winapi::RGB2int value.</span></span>

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="31131-449">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-449">Return Value - backgroundColor</span></span>

<span data-ttu-id="31131-450">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="31131-450">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="31131-451">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-451">Remarks - backgroundColor</span></span>

<span data-ttu-id="31131-452">返される整数には、次のような RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="31131-452">The integer that is returned contains the RGB color as follows:</span></span>

-   <span data-ttu-id="31131-453">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31131-453">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="31131-454">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="31131-454">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="31131-455">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="31131-455">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="31131-456">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="31131-456">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="31131-457">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="31131-457">The maximum value for a single byte is 255.</span></span>

### <a name="examples---backgroundcolor"></a><span data-ttu-id="31131-458">例 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-458">Examples - backgroundColor</span></span>

<span data-ttu-id="31131-459">次の例は、コントロールの背景色を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-459">The following example shows how to return and set the background color for a control.</span></span>

```xpp
// Retrieve the existing background color. 
info (strfmt("Background color: %1", this.backgroundColor())); 
// Set the background color. 
this.backgroundColor(WindowsPalette::DarkShadow3D);
```

## <a name="method-backstyle"></a><span data-ttu-id="31131-460">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="31131-460">Method backStyle</span></span>

<span data-ttu-id="31131-461">コントロール� のバックグラウンドを透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-461">Determines whether the control�s background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="31131-462">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="31131-462">Parameters - backStyle</span></span>

<span data-ttu-id="31131-463">値</span><span class="sxs-lookup"><span data-stu-id="31131-463">value</span></span>  
<span data-ttu-id="31131-464">コントロールの背景スタイルとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-464">The value to assign as the background style of the control; optional.</span></span>

### <a name="return-value---backstyle"></a><span data-ttu-id="31131-465">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="31131-465">Return Value - backStyle</span></span>

<span data-ttu-id="31131-466">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="31131-466">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="examples---backstyle"></a><span data-ttu-id="31131-467">例 - backStyle</span><span class="sxs-lookup"><span data-stu-id="31131-467">Examples - backStyle</span></span>

<span data-ttu-id="31131-468">次の例は、背景スタイルを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-468">The following example shows how to return and set the background style.</span></span>

```xpp
// Return the background style. 
info (strfmt("Background style: %1", this.backStyle())); 
// Set the background style. 
this.backStyle(FormBackStyle::Transparent);
```

## <a name="method-begindrag"></a><span data-ttu-id="31131-469">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="31131-469">Method beginDrag</span></span>

<span data-ttu-id="31131-470">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-470">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="31131-471">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="31131-471">Parameters - beginDrag</span></span>

<span data-ttu-id="31131-472">x</span><span class="sxs-lookup"><span data-stu-id="31131-472">x</span></span>  
<span data-ttu-id="31131-473">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-473">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="31131-474">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="31131-474">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="31131-475">y</span><span class="sxs-lookup"><span data-stu-id="31131-475">y</span></span>  
<span data-ttu-id="31131-476">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-476">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="31131-477">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="31131-477">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="31131-478">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="31131-478">Return Value - beginDrag</span></span>

<span data-ttu-id="31131-479">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-479">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="31131-480">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="31131-480">Remarks - beginDrag</span></span>

<span data-ttu-id="31131-481">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="31131-481">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="31131-482">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="31131-482">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="examples---begindrag"></a><span data-ttu-id="31131-483">例 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="31131-483">Examples - beginDrag</span></span>

<span data-ttu-id="31131-484">次の例では、ユーザーがフォーム コンボ ボックス コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-484">The following example displays the x-coordinate and y-coordinate in the Infolog when the user starts to drag the form combo box control.</span></span>

```xpp
public int beginDrag(int _x, int _y) 
{ 
    int ret; 
    info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
    ret = super(_x, _y); 
    return ret; 
}
```

## <a name="method-bold"></a><span data-ttu-id="31131-485">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="31131-485">Method bold</span></span>

<span data-ttu-id="31131-486">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-486">Gets or sets the weight of font that is used to display text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="31131-487">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="31131-487">Parameters - bold</span></span>

<span data-ttu-id="31131-488">値</span><span class="sxs-lookup"><span data-stu-id="31131-488">value</span></span>  
<span data-ttu-id="31131-489">コントロールのボールド設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-489">The value to assign to the control's bold setting; optional.</span></span>

### <a name="return-value---bold"></a><span data-ttu-id="31131-490">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="31131-490">Return Value - bold</span></span>

<span data-ttu-id="31131-491">0 (ゼロ) から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-491">An integer value between 0 (zero) and 9, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="31131-492">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="31131-492">Remarks - bold</span></span>

<span data-ttu-id="31131-493">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="31131-493">The integer that is returned contains the font weight as follows:</span></span>

-   <span data-ttu-id="31131-494">0 � 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="31131-494">0 � Use the default font weight.</span></span>
-   <span data-ttu-id="31131-495">1 � シン。</span><span class="sxs-lookup"><span data-stu-id="31131-495">1 � Thin.</span></span>
-   <span data-ttu-id="31131-496">2 � エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="31131-496">2 � Extra-light.</span></span>
-   <span data-ttu-id="31131-497">3 � ライト。</span><span class="sxs-lookup"><span data-stu-id="31131-497">3 � Light.</span></span>
-   <span data-ttu-id="31131-498">4 � 標準。</span><span class="sxs-lookup"><span data-stu-id="31131-498">4 � Normal.</span></span>
-   <span data-ttu-id="31131-499">5 � 中。</span><span class="sxs-lookup"><span data-stu-id="31131-499">5 � Medium.</span></span>
-   <span data-ttu-id="31131-500">6 � セミボールド。</span><span class="sxs-lookup"><span data-stu-id="31131-500">6 � Semibold.</span></span>
-   <span data-ttu-id="31131-501">7 � 太字。</span><span class="sxs-lookup"><span data-stu-id="31131-501">7 � Bold.</span></span>
-   <span data-ttu-id="31131-502">8 � 極太。</span><span class="sxs-lookup"><span data-stu-id="31131-502">8 � Extra-bold.</span></span>
-   <span data-ttu-id="31131-503">9 � ヘビー。</span><span class="sxs-lookup"><span data-stu-id="31131-503">9 � Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="31131-504">メソッド border</span><span class="sxs-lookup"><span data-stu-id="31131-504">Method border</span></span>

<span data-ttu-id="31131-505">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-505">Gets or sets the style of the border line for the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="31131-506">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="31131-506">Parameters - border</span></span>

<span data-ttu-id="31131-507">値</span><span class="sxs-lookup"><span data-stu-id="31131-507">value</span></span>  
<span data-ttu-id="31131-508">コントロールの境界スタイルとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-508">The value to assign as the border style for the control; optional.</span></span>

### <a name="return-value---border"></a><span data-ttu-id="31131-509">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="31131-509">Return Value - border</span></span>

<span data-ttu-id="31131-510">0 (ゼロ) から 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="31131-510">An integer between 0 (zero) and 4, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="31131-511">備考 - border</span><span class="sxs-lookup"><span data-stu-id="31131-511">Remarks - border</span></span>

<span data-ttu-id="31131-512">返される整数には、次のような境界線のスタイル線が含まれます。</span><span class="sxs-lookup"><span data-stu-id="31131-512">The integer that is returned contains the border style line as follows.</span></span>

-   <span data-ttu-id="31131-513">0 � 自動。</span><span class="sxs-lookup"><span data-stu-id="31131-513">0 � Auto.</span></span>
-   <span data-ttu-id="31131-514">1 � 3D。</span><span class="sxs-lookup"><span data-stu-id="31131-514">1 � 3D.</span></span>
-   <span data-ttu-id="31131-515">2 � 単一明細行。</span><span class="sxs-lookup"><span data-stu-id="31131-515">2 � Single line.</span></span>
-   <span data-ttu-id="31131-516">3 � 均一。</span><span class="sxs-lookup"><span data-stu-id="31131-516">3 � Flat.</span></span>
-   <span data-ttu-id="31131-517">4 � なし。</span><span class="sxs-lookup"><span data-stu-id="31131-517">4 � None.</span></span>

### <a name="examples---border"></a><span data-ttu-id="31131-518">例 - border</span><span class="sxs-lookup"><span data-stu-id="31131-518">Examples - border</span></span>

<span data-ttu-id="31131-519">次の例は、コントロールの境界線のスタイルを取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-519">The following example shows how to retrieve and set the border style for a control.</span></span>

```xpp
// Retrieve the border style. 
info (strfmt("border: %1", this.border())); 
// Set the border style. 
this.border(2);
```

## <a name="method-cachedatamethod"></a><span data-ttu-id="31131-520">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="31131-520">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="31131-521">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="31131-521">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="31131-522">値</span><span class="sxs-lookup"><span data-stu-id="31131-522">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="31131-523">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="31131-523">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="31131-524">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="31131-524">Method calcControlSize</span></span>

<span data-ttu-id="31131-525">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-525">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="31131-526">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="31131-526">Parameters - calcControlSize</span></span>

<span data-ttu-id="31131-527">chars</span><span class="sxs-lookup"><span data-stu-id="31131-527">chars</span></span>  
<span data-ttu-id="31131-528">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="31131-528">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="31131-529">明細行</span><span class="sxs-lookup"><span data-stu-id="31131-529">lines</span></span>  
<span data-ttu-id="31131-530">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="31131-530">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="31131-531">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="31131-531">Return Value - calcControlSize</span></span>

<span data-ttu-id="31131-532">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="31131-532">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="31131-533">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="31131-533">Method characterSet</span></span>

<span data-ttu-id="31131-534">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-534">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="31131-535">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="31131-535">Parameters - characterSet</span></span>

<span data-ttu-id="31131-536">値</span><span class="sxs-lookup"><span data-stu-id="31131-536">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="31131-537">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="31131-537">Return Value - characterSet</span></span>

<span data-ttu-id="31131-538">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-538">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="31131-539">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="31131-539">Remarks - characterSet</span></span>

<span data-ttu-id="31131-540">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-540">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="31131-541">値です。</span><span class="sxs-lookup"><span data-stu-id="31131-541">Value.</span></span> | <span data-ttu-id="31131-542">説明。</span><span class="sxs-lookup"><span data-stu-id="31131-542">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="31131-543">0</span><span class="sxs-lookup"><span data-stu-id="31131-543">0</span></span>      | <span data-ttu-id="31131-544">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-544">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="31131-545">1</span><span class="sxs-lookup"><span data-stu-id="31131-545">1</span></span>      | <span data-ttu-id="31131-546">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-546">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="31131-547">2</span><span class="sxs-lookup"><span data-stu-id="31131-547">2</span></span>      | <span data-ttu-id="31131-548">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-548">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="31131-549">77</span><span class="sxs-lookup"><span data-stu-id="31131-549">77</span></span>     | <span data-ttu-id="31131-550">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-550">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="31131-551">128</span><span class="sxs-lookup"><span data-stu-id="31131-551">128</span></span>    | <span data-ttu-id="31131-552">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-552">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="31131-553">129</span><span class="sxs-lookup"><span data-stu-id="31131-553">129</span></span>    | <span data-ttu-id="31131-554">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-554">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="31131-555">134</span><span class="sxs-lookup"><span data-stu-id="31131-555">134</span></span>    | <span data-ttu-id="31131-556">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-556">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="31131-557">136</span><span class="sxs-lookup"><span data-stu-id="31131-557">136</span></span>    | <span data-ttu-id="31131-558">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-558">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="31131-559">161</span><span class="sxs-lookup"><span data-stu-id="31131-559">161</span></span>    | <span data-ttu-id="31131-560">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-560">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="31131-561">162</span><span class="sxs-lookup"><span data-stu-id="31131-561">162</span></span>    | <span data-ttu-id="31131-562">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-562">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="31131-563">163</span><span class="sxs-lookup"><span data-stu-id="31131-563">163</span></span>    | <span data-ttu-id="31131-564">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-564">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="31131-565">186</span><span class="sxs-lookup"><span data-stu-id="31131-565">186</span></span>    | <span data-ttu-id="31131-566">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-566">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="31131-567">204</span><span class="sxs-lookup"><span data-stu-id="31131-567">204</span></span>    | <span data-ttu-id="31131-568">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-568">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="31131-569">238</span><span class="sxs-lookup"><span data-stu-id="31131-569">238</span></span>    | <span data-ttu-id="31131-570">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-570">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="31131-571">255</span><span class="sxs-lookup"><span data-stu-id="31131-571">255</span></span>    | <span data-ttu-id="31131-572">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-572">OEM\_CHARSET</span></span>         |

<span data-ttu-id="31131-573">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="31131-573">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="31131-574">値です。</span><span class="sxs-lookup"><span data-stu-id="31131-574">Value.</span></span> | <span data-ttu-id="31131-575">説明。</span><span class="sxs-lookup"><span data-stu-id="31131-575">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="31131-576">130</span><span class="sxs-lookup"><span data-stu-id="31131-576">130</span></span>    | <span data-ttu-id="31131-577">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-577">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="31131-578">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="31131-578">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="31131-579">値です。</span><span class="sxs-lookup"><span data-stu-id="31131-579">Value.</span></span> | <span data-ttu-id="31131-580">説明。</span><span class="sxs-lookup"><span data-stu-id="31131-580">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="31131-581">177</span><span class="sxs-lookup"><span data-stu-id="31131-581">177</span></span>    | <span data-ttu-id="31131-582">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-582">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="31131-583">178</span><span class="sxs-lookup"><span data-stu-id="31131-583">178</span></span>    | <span data-ttu-id="31131-584">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-584">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="31131-585">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="31131-585">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="31131-586">値です。</span><span class="sxs-lookup"><span data-stu-id="31131-586">Value.</span></span> | <span data-ttu-id="31131-587">説明。</span><span class="sxs-lookup"><span data-stu-id="31131-587">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="31131-588">222</span><span class="sxs-lookup"><span data-stu-id="31131-588">222</span></span>    | <span data-ttu-id="31131-589">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="31131-589">THAI\_CHARSET</span></span> |

<span data-ttu-id="31131-590">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="31131-590">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="31131-591">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="31131-591">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="31131-592">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31131-592">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="31131-593">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="31131-593">Method colorScheme</span></span>

<span data-ttu-id="31131-594">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-594">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="31131-595">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="31131-595">Parameters - colorScheme</span></span>

<span data-ttu-id="31131-596">値</span><span class="sxs-lookup"><span data-stu-id="31131-596">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="31131-597">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="31131-597">Return Value - colorScheme</span></span>

<span data-ttu-id="31131-598">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="31131-598">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="31131-599">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="31131-599">Remarks - colorScheme</span></span>

<span data-ttu-id="31131-600">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="31131-600">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="31131-601">値です。</span><span class="sxs-lookup"><span data-stu-id="31131-601">Value.</span></span> | <span data-ttu-id="31131-602">スタイル。</span><span class="sxs-lookup"><span data-stu-id="31131-602">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="31131-603">0</span><span class="sxs-lookup"><span data-stu-id="31131-603">0</span></span>      | <span data-ttu-id="31131-604">既定。</span><span class="sxs-lookup"><span data-stu-id="31131-604">Default.</span></span>               |
| <span data-ttu-id="31131-605">1</span><span class="sxs-lookup"><span data-stu-id="31131-605">1</span></span>      | <span data-ttu-id="31131-606">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="31131-606">The Windows palette.</span></span>   |
| <span data-ttu-id="31131-607">2</span><span class="sxs-lookup"><span data-stu-id="31131-607">2</span></span>      | <span data-ttu-id="31131-608">真の配色。</span><span class="sxs-lookup"><span data-stu-id="31131-608">The true-color scheme.</span></span> |

## <a name="method-combotype"></a><span data-ttu-id="31131-609">メソッド comboType</span><span class="sxs-lookup"><span data-stu-id="31131-609">Method comboType</span></span>

<span data-ttu-id="31131-610">コントロールのコンボ ボックスのタイプを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-610">Sets or returns the type of combo box for the control.</span></span>

```xpp
public int comboType([int value])
```

### <a name="parameters---combotype"></a><span data-ttu-id="31131-611">パラメーター - comboType</span><span class="sxs-lookup"><span data-stu-id="31131-611">Parameters - comboType</span></span>

<span data-ttu-id="31131-612">値</span><span class="sxs-lookup"><span data-stu-id="31131-612">value</span></span>  
<span data-ttu-id="31131-613">コンボ ボックス コントロールのタイプとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-613">The value to assign as the type of combo box for the control; optional.</span></span>

### <a name="return-value---combotype"></a><span data-ttu-id="31131-614">戻り値 - comboType</span><span class="sxs-lookup"><span data-stu-id="31131-614">Return Value - comboType</span></span>

<span data-ttu-id="31131-615">コントロールのコンボ ボックスのタイプ。</span><span class="sxs-lookup"><span data-stu-id="31131-615">The type of combo box for the control.</span></span>

### <a name="remarks---combotype"></a><span data-ttu-id="31131-616">備考 - comboType</span><span class="sxs-lookup"><span data-stu-id="31131-616">Remarks - comboType</span></span>

<span data-ttu-id="31131-617">次のテーブルは、コンボ ボックス タイプの値を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-617">The following table shows the values for the combo box type.</span></span>

| <span data-ttu-id="31131-618">先頭値</span><span class="sxs-lookup"><span data-stu-id="31131-618">Value</span></span> | <span data-ttu-id="31131-619">説明</span><span class="sxs-lookup"><span data-stu-id="31131-619">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="31131-620">0</span><span class="sxs-lookup"><span data-stu-id="31131-620">0</span></span>     | <span data-ttu-id="31131-621">標準</span><span class="sxs-lookup"><span data-stu-id="31131-621">Standard</span></span>    |
| <span data-ttu-id="31131-622">1</span><span class="sxs-lookup"><span data-stu-id="31131-622">1</span></span>     | <span data-ttu-id="31131-623">リスト</span><span class="sxs-lookup"><span data-stu-id="31131-623">List</span></span>        |

### <a name="examples---combotype"></a><span data-ttu-id="31131-624">例 - comboType</span><span class="sxs-lookup"><span data-stu-id="31131-624">Examples - comboType</span></span>

<span data-ttu-id="31131-625">次の例は、コントロールに使用されるコンボ ボックスのタイプを取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-625">The following example shows how to retrieve and set the type of combo box that is used for the control.</span></span>

```xpp
// Retrieve the type of combo box control. 
info(strfmt("comboType: %1", this.comboType())); 
// Set the type of combo box control. 
this.comboType(1);
```

## <a name="method-configurationkey"></a><span data-ttu-id="31131-626">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="31131-626">Method configurationKey</span></span>

<span data-ttu-id="31131-627">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-627">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="31131-628">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="31131-628">Parameters - configurationKey</span></span>

<span data-ttu-id="31131-629">値</span><span class="sxs-lookup"><span data-stu-id="31131-629">value</span></span>  
<span data-ttu-id="31131-630">コントロールに割り当てるコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="31131-630">The ID of the configuration key to assign to the control.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="31131-631">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="31131-631">Return Value - configurationKey</span></span>

<span data-ttu-id="31131-632">コントロールに割り当てられるコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="31131-632">The ID of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="31131-633">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="31131-633">Remarks - configurationKey</span></span>

<span data-ttu-id="31131-634">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31131-634">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="31131-635">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="31131-635">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="examples---configurationkey"></a><span data-ttu-id="31131-636">例 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="31131-636">Examples - configurationKey</span></span>

<span data-ttu-id="31131-637">次の例は、コントロールのコンフィギュレーション キーの設定と取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-637">The following example shows the setting and retrieval of the configuration key for a control.</span></span>

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
// objCtrl previously assigned. 
// Assign a configuration key to the control. 
objCtrl.configurationKey(configurationkeynum(BankDeposit)); 
// Retrieve the configuration key ID from the control. 
cki = objCtrl.configurationKey(); 
if (cki != 0) 
{ 
    dck = new DictConfigurationKey(cki); 
    if (dck) 
    { 
    print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                  cki, 
                  dck.name()); 
    } 
}
```

## <a name="method-configurationkeyex"></a><span data-ttu-id="31131-638">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="31131-638">Method configurationKeyEx</span></span>

<span data-ttu-id="31131-639">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-639">Returns a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="31131-640">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="31131-640">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="31131-641">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="31131-641">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="31131-642">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="31131-642">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="31131-643">リストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="31131-643">The list does not contain duplicate IDs.</span></span> <span data-ttu-id="31131-644">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="31131-644">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="31131-645">さらに、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="31131-645">In addition, the returned list contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="examples---configurationkeyex"></a><span data-ttu-id="31131-646">例 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="31131-646">Examples - configurationKeyEx</span></span>

<span data-ttu-id="31131-647">次の例は、コントロールのコンフィギュレーション キー ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-647">The following example shows the retrieval of the configuration key IDs for a control.</span></span>

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
List list; 
ListEnumerator enum; 
// objCtrl previously assigned. 
list = objCtrl.configurationKeyEx(); 
if (0 != list.elements()) 
{ 
    enum = list.getEnumerator(); 
    while (enum.moveNext()) 
    { 
       dck = new DictConfigurationKey(enum.current()); 
       if (dck) 
       { 
        print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                     enum.current(), 
                     dck.name() ); 
       } 
    } 
}
```

## <a name="method-count"></a><span data-ttu-id="31131-648">メソッド count</span><span class="sxs-lookup"><span data-stu-id="31131-648">Method count</span></span>

<span data-ttu-id="31131-649">コンボ ボックス コントロール内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-649">Returns the number of items in the combo box control.</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="31131-650">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="31131-650">Return Value - count</span></span>

<span data-ttu-id="31131-651">コンボ ボックス コントロール内の項目の数。</span><span class="sxs-lookup"><span data-stu-id="31131-651">The number of items in the combo box control.</span></span>

### <a name="examples---count"></a><span data-ttu-id="31131-652">例 - count</span><span class="sxs-lookup"><span data-stu-id="31131-652">Examples - count</span></span>

<span data-ttu-id="31131-653">次の例は、count メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-653">The following example shows how to use the count method.</span></span>

```xpp
int j; 
j = this.count();
```

## <a name="method-countryregioncodes"></a><span data-ttu-id="31131-654">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="31131-654">Method countryRegionCodes</span></span>

<span data-ttu-id="31131-655">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-655">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="31131-656">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="31131-656">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="31131-657">値</span><span class="sxs-lookup"><span data-stu-id="31131-657">value</span></span>  
<span data-ttu-id="31131-658">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-658">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="31131-659">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="31131-659">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="31131-660">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="31131-660">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="31131-661">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="31131-661">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="31131-662">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="31131-662">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="31131-663">値</span><span class="sxs-lookup"><span data-stu-id="31131-663">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="31131-664">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="31131-664">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="31131-665">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="31131-665">Method dataField</span></span>

<span data-ttu-id="31131-666">コンボ ボックス コントロールのデータ フィールドを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-666">Sets or returns the data field for the combo box control.</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="31131-667">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="31131-667">Parameters - dataField</span></span>

<span data-ttu-id="31131-668">値</span><span class="sxs-lookup"><span data-stu-id="31131-668">value</span></span>  
<span data-ttu-id="31131-669">コンボ ボックス コントロールのデータ フィールド ID として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-669">The value to assign as the data field ID for the combo box control; optional.</span></span>

### <a name="return-value---datafield"></a><span data-ttu-id="31131-670">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="31131-670">Return Value - dataField</span></span>

<span data-ttu-id="31131-671">コンボ ボックス コントロールのデータ フィールド ID の値。</span><span class="sxs-lookup"><span data-stu-id="31131-671">The value of the data field ID for the combo box control.</span></span>

### <a name="examples---datafield"></a><span data-ttu-id="31131-672">例 - dataField</span><span class="sxs-lookup"><span data-stu-id="31131-672">Examples - dataField</span></span>

<span data-ttu-id="31131-673">次の例は、コンボ ボックス コントロールのデータ フィールドを設定して返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-673">The following example shows how to set and return the data field for the combo box control.</span></span>

```xpp
fieldID i; 
// The combo variable is a previously assigned  
// FormComboBoxControl value. 
// Retrieve the data Field. 
i = combo.dataField(); 
// Set the data field. 
combo.dataField(fieldnum(CustTable, IdentificationNumber));
```

## <a name="method-datamethod"></a><span data-ttu-id="31131-674">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="31131-674">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="31131-675">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="31131-675">Parameters - dataMethod</span></span>

<span data-ttu-id="31131-676">値</span><span class="sxs-lookup"><span data-stu-id="31131-676">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="31131-677">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="31131-677">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="31131-678">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="31131-678">Method dataRelationPath</span></span>

<span data-ttu-id="31131-679">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-679">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="31131-680">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="31131-680">Parameters - dataRelationPath</span></span>

<span data-ttu-id="31131-681">値</span><span class="sxs-lookup"><span data-stu-id="31131-681">value</span></span>  
<span data-ttu-id="31131-682">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-682">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="31131-683">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="31131-683">Return Value - dataRelationPath</span></span>

<span data-ttu-id="31131-684">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="31131-684">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="31131-685">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="31131-685">Remarks - dataRelationPath</span></span>

<span data-ttu-id="31131-686">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="31131-686">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="31131-687">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="31131-687">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="31131-688">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="31131-688">Method dataSource</span></span>

<span data-ttu-id="31131-689">コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-689">Gets or sets a data source that should be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="31131-690">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="31131-690">Parameters - dataSource</span></span>

<span data-ttu-id="31131-691">値</span><span class="sxs-lookup"><span data-stu-id="31131-691">value</span></span>  
<span data-ttu-id="31131-692">コンボ ボックス コントロールのデータ ソースとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-692">The value to assign as the data source for the combo box control; optional.</span></span>

### <a name="return-value---datasource"></a><span data-ttu-id="31131-693">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="31131-693">Return Value - dataSource</span></span>

<span data-ttu-id="31131-694">使用する必要のあるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="31131-694">The identifier of the data source that should be used.</span></span>

### <a name="examples---datasource"></a><span data-ttu-id="31131-695">例 - dataSource</span><span class="sxs-lookup"><span data-stu-id="31131-695">Examples - dataSource</span></span>

<span data-ttu-id="31131-696">次の例は、コンボ ボックス コントロールのデータ ソースを設定して返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-696">The following example shows how to set and return the data source for the combo box control.</span></span>

```xpp
int i; 
// The combo variable was previously assigned  
// as a FormComboBoxControl variable. 
// Retrieve the data source. 
i = combo.dataSource(); 
// Set the data source. 
combo.dataSource(tablenum(CustTable));
```

## <a name="method-displaylength"></a><span data-ttu-id="31131-697">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="31131-697">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="31131-698">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="31131-698">Parameters - displayLength</span></span>

<span data-ttu-id="31131-699">値</span><span class="sxs-lookup"><span data-stu-id="31131-699">value</span></span>  

<!-- -->

<span data-ttu-id="31131-700">モード</span><span class="sxs-lookup"><span data-stu-id="31131-700">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="31131-701">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="31131-701">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="31131-702">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="31131-702">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="31131-703">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="31131-703">Parameters - displayLengthMode</span></span>

<span data-ttu-id="31131-704">モード</span><span class="sxs-lookup"><span data-stu-id="31131-704">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="31131-705">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="31131-705">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="31131-706">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="31131-706">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="31131-707">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="31131-707">Parameters - displayLengthValue</span></span>

<span data-ttu-id="31131-708">値</span><span class="sxs-lookup"><span data-stu-id="31131-708">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="31131-709">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="31131-709">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="31131-710">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="31131-710">Method displayTarget</span></span>

<span data-ttu-id="31131-711">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-711">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="31131-712">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="31131-712">Parameters - displayTarget</span></span>

<span data-ttu-id="31131-713">値</span><span class="sxs-lookup"><span data-stu-id="31131-713">value</span></span>  
<span data-ttu-id="31131-714">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-714">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="31131-715">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="31131-715">Return Value - displayTarget</span></span>

<span data-ttu-id="31131-716">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="31131-716">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="31131-717">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="31131-717">Method dragDrop</span></span>

<span data-ttu-id="31131-718">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-718">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="31131-719">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="31131-719">Parameters - dragDrop</span></span>

<span data-ttu-id="31131-720">値</span><span class="sxs-lookup"><span data-stu-id="31131-720">value</span></span>  
<span data-ttu-id="31131-721">ドラッグ アンド ドロップの動作が有効かどうかを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-721">An integer value that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="31131-722">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="31131-722">Return Value - dragDrop</span></span>

<span data-ttu-id="31131-723">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="31131-723">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="examples---dragdrop"></a><span data-ttu-id="31131-724">例 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="31131-724">Examples - dragDrop</span></span>

<span data-ttu-id="31131-725">次の例は、ドラッグ アンド ドロップの動作が有効かどうかを示す値を返すか、設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-725">The following example shows how to return or set the value that indicates whether drag-and-drop behavior is enabled.</span></span>

```xpp
boolean bDragDrop; 
// The combo variable was previously assigned  
// as a FormComboBoxControl value. 
// Retrieve the drag-and-drop-enabled value. 
bDragDrop = combo.dragDrop(); 
// Set the drag-and-drop-enabled value. 
combo.dragDrop(true);
```

## <a name="method-dragover"></a><span data-ttu-id="31131-726">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="31131-726">Method dragOver</span></span>

<span data-ttu-id="31131-727">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-727">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="31131-728">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="31131-728">Parameters - dragOver</span></span>

<span data-ttu-id="31131-729">dragSource</span><span class="sxs-lookup"><span data-stu-id="31131-729">dragSource</span></span>  
<span data-ttu-id="31131-730">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-730">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-731">dragMode</span><span class="sxs-lookup"><span data-stu-id="31131-731">dragMode</span></span>  
<span data-ttu-id="31131-732">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-732">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-733">x</span><span class="sxs-lookup"><span data-stu-id="31131-733">x</span></span>  
<span data-ttu-id="31131-734">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-734">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-735">y</span><span class="sxs-lookup"><span data-stu-id="31131-735">y</span></span>  
<span data-ttu-id="31131-736">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-736">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="31131-737">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="31131-737">Return Value - dragOver</span></span>

<span data-ttu-id="31131-738">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="31131-738">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="31131-739">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="31131-739">Method dragOverEx</span></span>

<span data-ttu-id="31131-740">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-740">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="31131-741">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="31131-741">Parameters - dragOverEx</span></span>

<span data-ttu-id="31131-742">dragSource</span><span class="sxs-lookup"><span data-stu-id="31131-742">dragSource</span></span>  
<span data-ttu-id="31131-743">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-743">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-744">dragMode</span><span class="sxs-lookup"><span data-stu-id="31131-744">dragMode</span></span>  
<span data-ttu-id="31131-745">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-745">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-746">x</span><span class="sxs-lookup"><span data-stu-id="31131-746">x</span></span>  
<span data-ttu-id="31131-747">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-747">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-748">y</span><span class="sxs-lookup"><span data-stu-id="31131-748">y</span></span>  
<span data-ttu-id="31131-749">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-749">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="31131-750">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="31131-750">Return Value - dragOverEx</span></span>

<span data-ttu-id="31131-751">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="31131-751">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="31131-752">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="31131-752">Method dragText</span></span>

<span data-ttu-id="31131-753">フォーム コンボ ボックス コントロールをドラッグしたときに表示されるテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-753">Returns the text that is displayed when the form combo box control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="31131-754">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="31131-754">Return Value - dragText</span></span>

<span data-ttu-id="31131-755">コンボ ボックス コントロールをドラッグしたときに表示されるテキスト。コンボ ボックス コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="31131-755">The text that is displayed when the combo box control is dragged; an empty string if there is no text to display when the combo box control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="31131-756">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="31131-756">Method enabled</span></span>

<span data-ttu-id="31131-757">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="31131-757">Determines whether the object is enabled or disabled.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="31131-758">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="31131-758">Parameters - enabled</span></span>

<span data-ttu-id="31131-759">値</span><span class="sxs-lookup"><span data-stu-id="31131-759">value</span></span>  
<span data-ttu-id="31131-760">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-760">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="31131-761">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="31131-761">Return Value - enabled</span></span>

<span data-ttu-id="31131-762">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-762">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="31131-763">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="31131-763">Remarks - enabled</span></span>

<span data-ttu-id="31131-764">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="31131-764">The enabled property lets you enable or disable controls at run time.</span></span> <span data-ttu-id="31131-765">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="31131-765">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="31131-766">また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="31131-766">You can also disable a control that is used only for display purposes, such as an error message that provides read-only information.</span></span>

### <a name="examples---enabled"></a><span data-ttu-id="31131-767">例 - enabled</span><span class="sxs-lookup"><span data-stu-id="31131-767">Examples - enabled</span></span>

<span data-ttu-id="31131-768">次の例は、コントロールの有効なプロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-768">The following example shows how to return and set the enabled property for a control.</span></span>

```xpp
// Return the value of the enabled property. 
info(strfmt("enabled: %1",this.enabled())); 
// Set the enabled property. 
this.enabled(false);
```

## <a name="method-enumtype"></a><span data-ttu-id="31131-769">メソッド enumType</span><span class="sxs-lookup"><span data-stu-id="31131-769">Method enumType</span></span>

```xpp
public EnumId enumType([EnumId value])
```

### <a name="parameters---enumtype"></a><span data-ttu-id="31131-770">パラメーター - enumType</span><span class="sxs-lookup"><span data-stu-id="31131-770">Parameters - enumType</span></span>

<span data-ttu-id="31131-771">値</span><span class="sxs-lookup"><span data-stu-id="31131-771">value</span></span>  

### <a name="return-value---enumtype"></a><span data-ttu-id="31131-772">戻り値 - enumType</span><span class="sxs-lookup"><span data-stu-id="31131-772">Return Value - enumType</span></span>

## <a name="method-enumtypevalue"></a><span data-ttu-id="31131-773">メソッド enumTypeValue</span><span class="sxs-lookup"><span data-stu-id="31131-773">Method enumTypeValue</span></span>

```xpp
public EnumId enumTypeValue()
```

### <a name="return-value---enumtypevalue"></a><span data-ttu-id="31131-774">戻り値 - enumTypeValue</span><span class="sxs-lookup"><span data-stu-id="31131-774">Return Value - enumTypeValue</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="31131-775">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="31131-775">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="31131-776">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="31131-776">Parameters - extendedDataType</span></span>

<span data-ttu-id="31131-777">値</span><span class="sxs-lookup"><span data-stu-id="31131-777">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="31131-778">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="31131-778">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="31131-779">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="31131-779">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="31131-780">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="31131-780">Parameters - fastTabSummary</span></span>

<span data-ttu-id="31131-781">値</span><span class="sxs-lookup"><span data-stu-id="31131-781">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="31131-782">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="31131-782">Return Value - fastTabSummary</span></span>

## <a name="method-find"></a><span data-ttu-id="31131-783">メソッド find</span><span class="sxs-lookup"><span data-stu-id="31131-783">Method find</span></span>

```xpp
public int find(str string)
```

### <a name="parameters---find"></a><span data-ttu-id="31131-784">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="31131-784">Parameters - find</span></span>

<span data-ttu-id="31131-785">文字列</span><span class="sxs-lookup"><span data-stu-id="31131-785">string</span></span>  

### <a name="return-value---find"></a><span data-ttu-id="31131-786">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="31131-786">Return Value - find</span></span>

## <a name="method-font"></a><span data-ttu-id="31131-787">メソッド font</span><span class="sxs-lookup"><span data-stu-id="31131-787">Method font</span></span>

<span data-ttu-id="31131-788">コントロールに使用するフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-788">Gets or sets the name of the font that should be used for the control.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="31131-789">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="31131-789">Parameters - font</span></span>

<span data-ttu-id="31131-790">値</span><span class="sxs-lookup"><span data-stu-id="31131-790">value</span></span>  
<span data-ttu-id="31131-791">フォーム コンボ ボックス コントロール内のテキストに使用するフォントを示す文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-791">A String data type that indicates the font to use for text in a form combo box control; optional.</span></span>

### <a name="return-value---font"></a><span data-ttu-id="31131-792">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="31131-792">Return Value - font</span></span>

<span data-ttu-id="31131-793">Tahoma や Verdana など、使用されるべきフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="31131-793">The name of the font that should be used, such as Tahoma or Verdana.</span></span>

### <a name="examples---font"></a><span data-ttu-id="31131-794">例 - font</span><span class="sxs-lookup"><span data-stu-id="31131-794">Examples - font</span></span>

<span data-ttu-id="31131-795">次の例は、フォーム コンボ ボックス コントロールのフォントを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-795">The following example shows how to return and set the font for a form combo box control.</span></span>

```xpp
str strFont; 
; 
// The ctrl variable was previously assigned  
// as a form combo box control value. 
// Retrieve the font. 
strFont = ctrl.font(); 
// Set the font. 
ctrl.font("Times New Roman");
```

## <a name="method-fontsize"></a><span data-ttu-id="31131-796">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="31131-796">Method fontSize</span></span>

<span data-ttu-id="31131-797">コントロールに使用するフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-797">Gets or sets the size of the font that should be used for the control.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="31131-798">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="31131-798">Parameters - fontSize</span></span>

<span data-ttu-id="31131-799">値</span><span class="sxs-lookup"><span data-stu-id="31131-799">value</span></span>  
<span data-ttu-id="31131-800">フォームのコンボ ボック スコントロール内のテキストのフォント サイズをポイント単位で示す整数データ型 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-800">An Integer data type that indicates the font size in points for text in a form combo box control; optional.</span></span>

### <a name="return-value---fontsize"></a><span data-ttu-id="31131-801">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="31131-801">Return Value - fontSize</span></span>

<span data-ttu-id="31131-802">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="31131-802">The height of the font in points.</span></span>

### <a name="examples---fontsize"></a><span data-ttu-id="31131-803">例 - fontSize</span><span class="sxs-lookup"><span data-stu-id="31131-803">Examples - fontSize</span></span>

<span data-ttu-id="31131-804">次の例は、フォーム コンボ ボックス コントロールのフォント サイズを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-804">The following example shows how to return and set the font size for a form combo box control.</span></span>

```xpp
int nSize; 
// The ctrl variable was previously assigned  
// as a form combo box control. 
// Retrieve the font size. 
nSize = ctrl.fontSize(); 
// Set the font size. 
ctrl.fontSize(16);
```

## <a name="method-foregroundcolor"></a><span data-ttu-id="31131-805">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-805">Method foregroundColor</span></span>

<span data-ttu-id="31131-806">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-806">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="31131-807">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-807">Parameters - foregroundColor</span></span>

<span data-ttu-id="31131-808">値</span><span class="sxs-lookup"><span data-stu-id="31131-808">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="31131-809">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-809">Return Value - foregroundColor</span></span>

<span data-ttu-id="31131-810">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="31131-810">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="31131-811">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-811">Remarks - foregroundColor</span></span>

<span data-ttu-id="31131-812">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="31131-812">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="31131-813">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31131-813">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="31131-814">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="31131-814">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="31131-815">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="31131-815">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="31131-816">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="31131-816">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="31131-817">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="31131-817">The maximum value for a single byte is 255.</span></span>

## <a name="method-getedittext"></a><span data-ttu-id="31131-818">メソッド getEditText</span><span class="sxs-lookup"><span data-stu-id="31131-818">Method getEditText</span></span>

```xpp
public str getEditText()
```

### <a name="return-value---getedittext"></a><span data-ttu-id="31131-819">戻り値 - getEditText</span><span class="sxs-lookup"><span data-stu-id="31131-819">Return Value - getEditText</span></span>

## <a name="method-gettext"></a><span data-ttu-id="31131-820">メソッド getText</span><span class="sxs-lookup"><span data-stu-id="31131-820">Method getText</span></span>

```xpp
public str getText(int index)
```

### <a name="parameters---gettext"></a><span data-ttu-id="31131-821">パラメーター - getText</span><span class="sxs-lookup"><span data-stu-id="31131-821">Parameters - getText</span></span>

<span data-ttu-id="31131-822">指数</span><span class="sxs-lookup"><span data-stu-id="31131-822">index</span></span>  

### <a name="return-value---gettext"></a><span data-ttu-id="31131-823">戻り値 - getText</span><span class="sxs-lookup"><span data-stu-id="31131-823">Return Value - getText</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="31131-824">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="31131-824">Method hasChanged</span></span>

<span data-ttu-id="31131-825">フォーム コンボ ボックス コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-825">Sets or returns a value that indicates whether the contents of the form combo box control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="31131-826">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="31131-826">Parameters - hasChanged</span></span>

<span data-ttu-id="31131-827">val</span><span class="sxs-lookup"><span data-stu-id="31131-827">val</span></span>  
<span data-ttu-id="31131-828">コンボ ボックス コントロールの hasChanged 値として割り当てる値、オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-828">A value to assign as the hasChanged value for the combo box control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="31131-829">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="31131-829">Return Value - hasChanged</span></span>

<span data-ttu-id="31131-830">コンボ ボックス コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-830">true if the contents of the combo box control have changed; otherwise, false.</span></span>

### <a name="examples---haschanged"></a><span data-ttu-id="31131-831">例 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="31131-831">Examples - hasChanged</span></span>

<span data-ttu-id="31131-832">次の例は、コンボ ボックス コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-832">The following example shows how to return and set the value that indicates whether the contents of the combo box control have changed.</span></span>

```xpp
boolean bHasChanged; 
// The ctrl variable was previously assigned 
// as a FormComboBoxControl variable. 
// Retrieve the hasChanged value. 
bHasChanged = ctrl.hasChanged(); 
// Modify the hasChanged value. 
ctrl.hasChanged(true);
```

## <a name="method-hasusersetting"></a><span data-ttu-id="31131-833">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="31131-833">Method hasUserSetting</span></span>

<span data-ttu-id="31131-834">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-834">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="31131-835">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="31131-835">Return Value - hasUserSetting</span></span>

<span data-ttu-id="31131-836">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-836">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="31131-837">メソッド height</span><span class="sxs-lookup"><span data-stu-id="31131-837">Method height</span></span>

<span data-ttu-id="31131-838">ピクセル単位でコントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-838">Gets or sets the height of the control in pixels.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="31131-839">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="31131-839">Parameters - height</span></span>

<span data-ttu-id="31131-840">値</span><span class="sxs-lookup"><span data-stu-id="31131-840">value</span></span>  
<span data-ttu-id="31131-841">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-841">An integer value that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="31131-842">モード</span><span class="sxs-lookup"><span data-stu-id="31131-842">mode</span></span>  
<span data-ttu-id="31131-843">高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-843">An integer value that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="31131-844">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="31131-844">Return Value - height</span></span>

<span data-ttu-id="31131-845">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="31131-845">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="31131-846">備考 - height</span><span class="sxs-lookup"><span data-stu-id="31131-846">Remarks - height</span></span>

<span data-ttu-id="31131-847">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="31131-847">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="31131-848">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="31131-848">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="31131-849">モード</span><span class="sxs-lookup"><span data-stu-id="31131-849">Mode</span></span>              | <span data-ttu-id="31131-850">高さの計算</span><span class="sxs-lookup"><span data-stu-id="31131-850">Height calculation</span></span>                                                                         |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="31131-851">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="31131-851">-1 � Exact</span></span>        | <span data-ttu-id="31131-852">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="31131-852">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="31131-853">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="31131-853">0 � Auto</span></span>          | <span data-ttu-id="31131-854">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="31131-854">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="31131-855">1 � 列の高さ</span><span class="sxs-lookup"><span data-stu-id="31131-855">1 � Column height</span></span> | <span data-ttu-id="31131-856">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="31131-856">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="31131-857">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="31131-857">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="31131-858">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="31131-858">Method heightMode</span></span>

<span data-ttu-id="31131-859">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-859">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="31131-860">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="31131-860">Parameters - heightMode</span></span>

<span data-ttu-id="31131-861">値</span><span class="sxs-lookup"><span data-stu-id="31131-861">value</span></span>  
<span data-ttu-id="31131-862">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-862">An integer value that indicates how the height of the control is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="31131-863">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="31131-863">Return Value - heightMode</span></span>

<span data-ttu-id="31131-864">計算モード。</span><span class="sxs-lookup"><span data-stu-id="31131-864">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="31131-865">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="31131-865">Remarks - heightMode</span></span>

<span data-ttu-id="31131-866">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="31131-866">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="31131-867">モード</span><span class="sxs-lookup"><span data-stu-id="31131-867">Mode</span></span>          | <span data-ttu-id="31131-868">高さの計算</span><span class="sxs-lookup"><span data-stu-id="31131-868">Height calculation</span></span>                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="31131-869">正確</span><span class="sxs-lookup"><span data-stu-id="31131-869">Exact</span></span>         | <span data-ttu-id="31131-870">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="31131-870">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="31131-871">自動</span><span class="sxs-lookup"><span data-stu-id="31131-871">Auto</span></span>          | <span data-ttu-id="31131-872">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="31131-872">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="31131-873">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="31131-873">Column height</span></span> | <span data-ttu-id="31131-874">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="31131-874">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="31131-875">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="31131-875">The height of the control might change when the calculation mode is set to Auto or Column height.</span></span>

### <a name="examples---heightmode"></a><span data-ttu-id="31131-876">例 - heightMode</span><span class="sxs-lookup"><span data-stu-id="31131-876">Examples - heightMode</span></span>

<span data-ttu-id="31131-877">次の例は、フォーム コンボ ボックス コントロールの高さ計算モードを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-877">The following example shows how to return and set the height calculation mode for a form combo box control:</span></span>

```xpp
int nHeightMode; 
// The ctrl variable was previously assigned 
// as a form combo box control type. 
// Retrieve the height mode. 
nHeightMode = ctrl.HeightMode(); 
// Set the height mode. 
ctrl.heightMode(-1); 
// Set the height. 
ctrl.heightValue(16);
```

## <a name="method-heightvalue"></a><span data-ttu-id="31131-878">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="31131-878">Method heightValue</span></span>

<span data-ttu-id="31131-879">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-879">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="31131-880">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="31131-880">Parameters - heightValue</span></span>

<span data-ttu-id="31131-881">値</span><span class="sxs-lookup"><span data-stu-id="31131-881">value</span></span>  
<span data-ttu-id="31131-882">高さをピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-882">An integer value that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="31131-883">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="31131-883">Return Value - heightValue</span></span>

<span data-ttu-id="31131-884">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="31131-884">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="31131-885">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="31131-885">Remarks - heightValue</span></span>

<span data-ttu-id="31131-886">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="31131-886">The height of the control is not changed unless the Exact height calculation mode is used.</span></span>

### <a name="examples---heightvalue"></a><span data-ttu-id="31131-887">例 - heightValue</span><span class="sxs-lookup"><span data-stu-id="31131-887">Examples - heightValue</span></span>

<span data-ttu-id="31131-888">次の例は、コンボ ボックス コントロールの高さの値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-888">The following example shows how to return and set the height value of a combo box control.</span></span>

```xpp
int nHeightValue; 
// The ctrl variable was previously assigned 
// as a form combo box control type. 
// Retrieve the height value. 
nHeightValue = ctrl.heightValue(); 
// Set the height value. 
ctrl.heightMode(-1); 
ctrl.heightValue(22);
```

## <a name="method-helpfield"></a><span data-ttu-id="31131-889">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="31131-889">Method helpField</span></span>

<span data-ttu-id="31131-890">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-890">Returns the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="31131-891">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="31131-891">Return Value - helpField</span></span>

<span data-ttu-id="31131-892">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="31131-892">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="31131-893">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="31131-893">Remarks - helpField</span></span>

<span data-ttu-id="31131-894">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="31131-894">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="31131-895">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="31131-895">Use the helpText method to set the value of the Help text.</span></span>

### <a name="examples---helpfield"></a><span data-ttu-id="31131-896">例 - helpField</span><span class="sxs-lookup"><span data-stu-id="31131-896">Examples - helpField</span></span>

<span data-ttu-id="31131-897">次の例は、helpField メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-897">The following example shows how to use the helpField method.</span></span>

```xpp
str strHelp; 
strHelp = this.helpField();
```

## <a name="method-helptext"></a><span data-ttu-id="31131-898">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="31131-898">Method helpText</span></span>

<span data-ttu-id="31131-899">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-899">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="31131-900">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="31131-900">Parameters - helpText</span></span>

<span data-ttu-id="31131-901">値</span><span class="sxs-lookup"><span data-stu-id="31131-901">value</span></span>  
<span data-ttu-id="31131-902">コントロールのヘルプ テキストとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-902">The value to assign as the Help text for the control; optional.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="31131-903">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="31131-903">Return Value - helpText</span></span>

<span data-ttu-id="31131-904">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="31131-904">The string that should be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="31131-905">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="31131-905">Remarks - helpText</span></span>

<span data-ttu-id="31131-906">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-906">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="31131-907">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="31131-907">The Help text must not exceed 250 characters.</span></span>

### <a name="examples---helptext"></a><span data-ttu-id="31131-908">例 - helpText</span><span class="sxs-lookup"><span data-stu-id="31131-908">Examples - helpText</span></span>

<span data-ttu-id="31131-909">次の例は、コントロールのヘルプ テキストを設定して返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-909">The following example shows how to set and return the Help text for a control.</span></span>

```xpp
// objCtrl previously assigned to a control 
// Retrieve existing help text. 
print objCtrl.helpText(); 
// Specify new help text. 
objCtrl.helpText("My new help text");
```

## <a name="method-hidefirstentry"></a><span data-ttu-id="31131-910">メソッド hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="31131-910">Method hideFirstEntry</span></span>

<span data-ttu-id="31131-911">コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-911">Sets or returns a value that indicates whether the first entry in the combo box control is hidden.</span></span>

```xpp
public boolean hideFirstEntry([boolean value])
```

### <a name="parameters---hidefirstentry"></a><span data-ttu-id="31131-912">パラメーター - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="31131-912">Parameters - hideFirstEntry</span></span>

<span data-ttu-id="31131-913">値</span><span class="sxs-lookup"><span data-stu-id="31131-913">value</span></span>  
<span data-ttu-id="31131-914">コンボ ボックス コントロールの最初のエントリが非表示がどうかを示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-914">A value that indicates whether the first entry in the combo box control is hidden; optional.</span></span>

### <a name="return-value---hidefirstentry"></a><span data-ttu-id="31131-915">戻り値 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="31131-915">Return Value - hideFirstEntry</span></span>

<span data-ttu-id="31131-916">コンボ ボックス コントロール内の最初のエントリが非表示の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-916">true if the first entry in the combo box control is hidden; otherwise, false.</span></span>

### <a name="remarks---hidefirstentry"></a><span data-ttu-id="31131-917">備考 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="31131-917">Remarks - hideFirstEntry</span></span>

<span data-ttu-id="31131-918">コンボ ボックス コントロールの最初のエントリを非表示にすることにより、必須プロパティがはいに設定されている列挙データベース フィールドの動作をエミュレートするコントロールを有効にします。</span><span class="sxs-lookup"><span data-stu-id="31131-918">By hiding the first entry in the combo box control, you enable the control to emulate the behavior of an enum database field where the Mandatory property is set to Yes.</span></span>

### <a name="examples---hidefirstentry"></a><span data-ttu-id="31131-919">例 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="31131-919">Examples - hideFirstEntry</span></span>

<span data-ttu-id="31131-920">次の例は、コンボ ボックス コントロールの最初のエントリが非表示になっているかどうかを示す値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-920">The following example shows how to return and set the value that indicates whether the first entry in the combo box control is hidden.</span></span>

```xpp
boolean bHideFirstEntry; 
// The ctrl variable was previously assigned 
// as a form combo box control type. 
// Retrieve the hideFirstEntry value. 
bHideFirstEntry = ctrl.hideFirstEntry(); 
// Set the hideFirstEntry value. 
bHideFirstEntry = ctrl.hideFirstEntry(true);
```

## <a name="method-hierarchyparent"></a><span data-ttu-id="31131-921">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="31131-921">Method hierarchyParent</span></span>

<span data-ttu-id="31131-922">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-922">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="31131-923">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="31131-923">Parameters - hierarchyParent</span></span>

<span data-ttu-id="31131-924">値</span><span class="sxs-lookup"><span data-stu-id="31131-924">value</span></span>  
<span data-ttu-id="31131-925">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="31131-925">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="31131-926">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="31131-926">Return Value - hierarchyParent</span></span>

<span data-ttu-id="31131-927">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="31131-927">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="31131-928">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="31131-928">Method hWnd</span></span>

<span data-ttu-id="31131-929">コントロールの Windows ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-929">Returns the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="31131-930">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="31131-930">Return Value - hWnd</span></span>

<span data-ttu-id="31131-931">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="31131-931">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="31131-932">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="31131-932">Remarks - hWnd</span></span>

<span data-ttu-id="31131-933">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="31131-933">The handle can be used with the Windows API.</span></span>

### <a name="examples---hwnd"></a><span data-ttu-id="31131-934">例 - hWnd</span><span class="sxs-lookup"><span data-stu-id="31131-934">Examples - hWnd</span></span>

<span data-ttu-id="31131-935">次の例は、コントロールの Windows ハンドルを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-935">The following example shows how to retrieve the Windows handle for a control.</span></span>

```xpp
int h; 
h = this.hWnd(); 
info (strfmt("hWnd: %1", h));
```

## <a name="method-iscontainer"></a><span data-ttu-id="31131-936">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="31131-936">Method isContainer</span></span>

<span data-ttu-id="31131-937">コントロールがコンテナーかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-937">Returns a value that indicates whether the control is a container.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="31131-938">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="31131-938">Return Value - isContainer</span></span>

<span data-ttu-id="31131-939">コントロールがコンテナーである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-939">true if the control is a container; otherwise, false.</span></span>

### <a name="examples---iscontainer"></a><span data-ttu-id="31131-940">例 - isContainer</span><span class="sxs-lookup"><span data-stu-id="31131-940">Examples - isContainer</span></span>

<span data-ttu-id="31131-941">次の例は、コントロールがコンテナーであるかどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-941">The following example shows how to determine whether a control is a container.</span></span>

```xpp
info(strfmt("IsContainer: %1", this.isContainer()));
```

## <a name="method-isdisplayed"></a><span data-ttu-id="31131-942">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="31131-942">Method isDisplayed</span></span>

<span data-ttu-id="31131-943">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-943">Returns a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="31131-944">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="31131-944">Return Value - isDisplayed</span></span>

<span data-ttu-id="31131-945">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-945">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="31131-946">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="31131-946">Remarks - isDisplayed</span></span>

<span data-ttu-id="31131-947">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="31131-947">To modify the visible state of the control, call the visible method.</span></span>

### <a name="examples---isdisplayed"></a><span data-ttu-id="31131-948">例 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="31131-948">Examples - isDisplayed</span></span>

<span data-ttu-id="31131-949">次の例は、コントロールが可視かどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-949">The following example shows how to determine whether a control is visible.</span></span>

```xpp
info(strfmt("isDisplayed: %1", this.isDisplayed()));
```

## <a name="method-isrestricted"></a><span data-ttu-id="31131-950">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="31131-950">Method isRestricted</span></span>

<span data-ttu-id="31131-951">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-951">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="31131-952">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="31131-952">Return Value - isRestricted</span></span>

<span data-ttu-id="31131-953">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-953">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="31131-954">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="31131-954">Method isUserSetupEnabled</span></span>

<span data-ttu-id="31131-955">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-955">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="31131-956">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="31131-956">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="31131-957">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="31131-957">neededSetupRights</span></span>  
<span data-ttu-id="31131-958">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="31131-958">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="31131-959">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="31131-959">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="31131-960">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-960">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="31131-961">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="31131-961">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="31131-962">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="31131-962">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31131-963">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="31131-963">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="31131-964">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="31131-964">No changes can be made to the control.</span></span> <span data-ttu-id="31131-965">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-965">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="31131-966">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="31131-966">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="31131-967">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="31131-967">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="31131-968">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="31131-968">The user cannot move the control.</span></span>   |
| <span data-ttu-id="31131-969">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="31131-969">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="31131-970">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="31131-970">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="31131-971">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="31131-971">The user can also move the control.</span></span> |

<span data-ttu-id="31131-972">「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメータで指定されたレベル以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="31131-972">For this method to return true, the AllowUserSetup property for the design and all parent containers must be at least as high as the level that is specified by the neededSetupRights parameter.</span></span>

### <a name="examples---isusersetupenabled"></a><span data-ttu-id="31131-973">例 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="31131-973">Examples - isUserSetupEnabled</span></span>

<span data-ttu-id="31131-974">次の例は、コントロールのユーザー設定権限を決定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-974">The following example shows how to determine the user setup rights for a control.</span></span>

```xpp
FormAllowUserSetup formAllowUserSetup = FormAllowUserSetup::No; 
switch (true) 
{ 
    case this.isUserSetupEnabled(FormAllowUserSetup::Yes): 
        formAllowUserSetup = FormAllowUserSetup::Yes; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::Restricted): 
        formAllowUserSetup = FormAllowUserSetup::Restricted; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::No): 
       formAllowUserSetup = FormAllowUserSetup::No; 
        break; 
} 
info (strfmt("formAllowUserSetup: %1", formAllowUserSetup));
```

## <a name="method-isvalid"></a><span data-ttu-id="31131-975">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="31131-975">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="31131-976">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="31131-976">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="31131-977">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="31131-977">Method italic</span></span>

<span data-ttu-id="31131-978">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-978">Sets or returns a value that indicates whether the text in the control is italic.</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="31131-979">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="31131-979">Parameters - italic</span></span>

<span data-ttu-id="31131-980">値</span><span class="sxs-lookup"><span data-stu-id="31131-980">value</span></span>  
<span data-ttu-id="31131-981">コントロールのイタリック設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-981">The value to assign to the italic setting of the control; optional.</span></span>

### <a name="return-value---italic"></a><span data-ttu-id="31131-982">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="31131-982">Return Value - italic</span></span>

<span data-ttu-id="31131-983">コントロール内のテキストが斜体である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-983">true if the text in the control is italic; otherwise, false.</span></span>

## <a name="method-item"></a><span data-ttu-id="31131-984">メソッド item</span><span class="sxs-lookup"><span data-stu-id="31131-984">Method item</span></span>

```xpp
public int item([int value])
```

### <a name="parameters---item"></a><span data-ttu-id="31131-985">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="31131-985">Parameters - item</span></span>

<span data-ttu-id="31131-986">値</span><span class="sxs-lookup"><span data-stu-id="31131-986">value</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="31131-987">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="31131-987">Return Value - item</span></span>

## <a name="method-items"></a><span data-ttu-id="31131-988">メソッド items</span><span class="sxs-lookup"><span data-stu-id="31131-988">Method items</span></span>

```xpp
public int items([int value])
```

### <a name="parameters---items"></a><span data-ttu-id="31131-989">パラメーター - items</span><span class="sxs-lookup"><span data-stu-id="31131-989">Parameters - items</span></span>

<span data-ttu-id="31131-990">値</span><span class="sxs-lookup"><span data-stu-id="31131-990">value</span></span>  

### <a name="return-value---items"></a><span data-ttu-id="31131-991">戻り値 - items</span><span class="sxs-lookup"><span data-stu-id="31131-991">Return Value - items</span></span>

## <a name="method-label"></a><span data-ttu-id="31131-992">メソッド label</span><span class="sxs-lookup"><span data-stu-id="31131-992">Method label</span></span>

<span data-ttu-id="31131-993">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-993">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="31131-994">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="31131-994">Parameters - label</span></span>

<span data-ttu-id="31131-995">値</span><span class="sxs-lookup"><span data-stu-id="31131-995">value</span></span>  
<span data-ttu-id="31131-996">コントロールのラベルとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-996">The value to assign as the label of the control; optional.</span></span>

### <a name="return-value---label"></a><span data-ttu-id="31131-997">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="31131-997">Return Value - label</span></span>

<span data-ttu-id="31131-998">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="31131-998">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="31131-999">備考 - label</span><span class="sxs-lookup"><span data-stu-id="31131-999">Remarks - label</span></span>

<span data-ttu-id="31131-1000">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1000">The label determines the text that is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="31131-1001">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="31131-1001">The label property value cannot exceed 250 characters.</span></span>

### <a name="examples---label"></a><span data-ttu-id="31131-1002">例 - label</span><span class="sxs-lookup"><span data-stu-id="31131-1002">Examples - label</span></span>

<span data-ttu-id="31131-1003">次の例は、コントロールのラベルを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1003">The following example shows how to return and set the label of the control.</span></span>

```xpp
// Return the label value. 
info(strfmt("label: %1", this.label())); 
// Set the label value. 
this.label("New label text goes here");
```

## <a name="method-labelalignment"></a><span data-ttu-id="31131-1004">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="31131-1004">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="31131-1005">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="31131-1005">Parameters - labelAlignment</span></span>

<span data-ttu-id="31131-1006">値</span><span class="sxs-lookup"><span data-stu-id="31131-1006">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="31131-1007">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="31131-1007">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="31131-1008">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="31131-1008">Method labelBold</span></span>

<span data-ttu-id="31131-1009">コントロールのラベルの太字設定を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1009">Sets or returns a value that indicates the bold setting for the label in the control.</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="31131-1010">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="31131-1010">Parameters - labelBold</span></span>

<span data-ttu-id="31131-1011">値</span><span class="sxs-lookup"><span data-stu-id="31131-1011">value</span></span>  
<span data-ttu-id="31131-1012">ラベルのボールド設定に割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="31131-1012">The value to assign to the label bold setting.</span></span> <span data-ttu-id="31131-1013">これは、ReportControlBold 列挙型からの値の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="31131-1013">This can be one of the values from the ReportControlBold enumeration.</span></span>

### <a name="return-value---labelbold"></a><span data-ttu-id="31131-1014">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="31131-1014">Return Value - labelBold</span></span>

<span data-ttu-id="31131-1015">コントロールのラベルの太字設定を示す ReportControlBold 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="31131-1015">A value from the ReportControlBold enumeration that indicates the bold setting for the label in the control.</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="31131-1016">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="31131-1016">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="31131-1017">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="31131-1017">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="31131-1018">値</span><span class="sxs-lookup"><span data-stu-id="31131-1018">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="31131-1019">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="31131-1019">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="31131-1020">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="31131-1020">Method labelFont</span></span>

<span data-ttu-id="31131-1021">フォーム コンボ ボックス コントロールのラベル テキストのフォントを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1021">Sets or returns a font for the label text in a form combo box control.</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="31131-1022">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="31131-1022">Parameters - labelFont</span></span>

<span data-ttu-id="31131-1023">値</span><span class="sxs-lookup"><span data-stu-id="31131-1023">value</span></span>  
<span data-ttu-id="31131-1024">フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型; オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1024">A String data type that indicates the font for the label text in a form combo box control; optional.</span></span>

### <a name="return-value---labelfont"></a><span data-ttu-id="31131-1025">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="31131-1025">Return Value - labelFont</span></span>

<span data-ttu-id="31131-1026">フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="31131-1026">A String data type value that indicates the font for the label text in a form combo box control.</span></span>

### <a name="examples---labelfont"></a><span data-ttu-id="31131-1027">例 - labelFont</span><span class="sxs-lookup"><span data-stu-id="31131-1027">Examples - labelFont</span></span>

<span data-ttu-id="31131-1028">次の例は、フォーム コンボ ボックス コントロール内のラベル テキストのフォントを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1028">The following example shows how to return and set the font for the label text in a form combo box control.</span></span>

```xpp
str strLabelFont; 
// The ctrl variable was previously assigned  
// as a form combo box control variable. 
// Retrieve the font. 
strLabelFont = ctrl.labelFont(); 
// Set the label font. 
ctrl.labelFont("Times New Roman");
```

## <a name="method-labelfontsize"></a><span data-ttu-id="31131-1029">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="31131-1029">Method labelFontSize</span></span>

<span data-ttu-id="31131-1030">フォーム コンボ ボックス コントロールのラベル テキストのフォント サイズをポイント単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1030">Sets or returns the font size in points for the label text in a form combo box control.</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="31131-1031">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="31131-1031">Parameters - labelFontSize</span></span>

<span data-ttu-id="31131-1032">値</span><span class="sxs-lookup"><span data-stu-id="31131-1032">value</span></span>  
<span data-ttu-id="31131-1033">フォーム コンボ ボックス コントロール内にラベル テキストのフォント サイズをポイントで示す整数データ型 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1033">An Integer data type that indicates the font size in points for the label text in a form combo box control; optional.</span></span>

### <a name="return-value---labelfontsize"></a><span data-ttu-id="31131-1034">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="31131-1034">Return Value - labelFontSize</span></span>

<span data-ttu-id="31131-1035">フォーム コンボ ボックス コントロール内にテキストのラベル フォント サイズをポイントで示す整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="31131-1035">An Integer data type value that indicates the label font size in points for the text in a form combo box control.</span></span>

### <a name="examples---labelfontsize"></a><span data-ttu-id="31131-1036">例 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="31131-1036">Examples - labelFontSize</span></span>

<span data-ttu-id="31131-1037">次の例は、フォーム コンボ ボックス コントロールのラベルのフォント サイズを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1037">The following example shows how to return and set the label font size for a form combo box control.</span></span>

```xpp
int nSize; 
// The ctrl variable was previously assigned  
// as a form combo box control. 
// Retrieve the label font size. 
nSize = ctrl.labelFontSize(); 
// Set the label font size. 
ctrl.labelFontSize(16);
```

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="31131-1038">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-1038">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="31131-1039">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-1039">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="31131-1040">値</span><span class="sxs-lookup"><span data-stu-id="31131-1040">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="31131-1041">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="31131-1041">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="31131-1042">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="31131-1042">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="31131-1043">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="31131-1043">Parameters - labelGuide</span></span>

<span data-ttu-id="31131-1044">値</span><span class="sxs-lookup"><span data-stu-id="31131-1044">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="31131-1045">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="31131-1045">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="31131-1046">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="31131-1046">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="31131-1047">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="31131-1047">Parameters - labelHeight</span></span>

<span data-ttu-id="31131-1048">値</span><span class="sxs-lookup"><span data-stu-id="31131-1048">value</span></span>  

<!-- -->

<span data-ttu-id="31131-1049">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1049">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="31131-1050">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="31131-1050">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="31131-1051">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="31131-1051">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="31131-1052">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="31131-1052">Parameters - labelHeightMode</span></span>

<span data-ttu-id="31131-1053">値</span><span class="sxs-lookup"><span data-stu-id="31131-1053">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="31131-1054">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="31131-1054">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="31131-1055">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="31131-1055">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="31131-1056">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="31131-1056">Parameters - labelHeightValue</span></span>

<span data-ttu-id="31131-1057">値</span><span class="sxs-lookup"><span data-stu-id="31131-1057">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="31131-1058">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="31131-1058">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="31131-1059">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="31131-1059">Method labelItalic</span></span>

<span data-ttu-id="31131-1060">コントロールのラベルのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1060">Sets or returns a value that indicates whether the text in the label of the control is italic.</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="31131-1061">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="31131-1061">Parameters - labelItalic</span></span>

<span data-ttu-id="31131-1062">値</span><span class="sxs-lookup"><span data-stu-id="31131-1062">value</span></span>  
<span data-ttu-id="31131-1063">コントロールのラベルのイタリック設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1063">The value to assign to the italic setting of the label of the control; optional.</span></span>

### <a name="return-value---labelitalic"></a><span data-ttu-id="31131-1064">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="31131-1064">Return Value - labelItalic</span></span>

<span data-ttu-id="31131-1065">コントロールのラベル内のテキストが斜体である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-1065">true if the text in the label of the control is italic; otherwise, false.</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="31131-1066">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1066">Method labelMouseDblClick</span></span>

<span data-ttu-id="31131-1067">コントロールのラベルがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1067">Is called when the label for the control is double-clicked by the user.</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="31131-1068">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1068">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="31131-1069">x</span><span class="sxs-lookup"><span data-stu-id="31131-1069">x</span></span>  
<span data-ttu-id="31131-1070">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1070">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1071">y</span><span class="sxs-lookup"><span data-stu-id="31131-1071">y</span></span>  
<span data-ttu-id="31131-1072">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1072">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1073">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1073">button</span></span>  
<span data-ttu-id="31131-1074">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1074">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1075">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1075">Ctrl</span></span>  
<span data-ttu-id="31131-1076">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1076">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1077">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1077">Shift</span></span>  
<span data-ttu-id="31131-1078">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1078">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="31131-1079">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1079">Return Value - labelMouseDblClick</span></span>

<span data-ttu-id="31131-1080">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-1080">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---labelmousedblclick"></a><span data-ttu-id="31131-1081">備考 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1081">Remarks - labelMouseDblClick</span></span>

<span data-ttu-id="31131-1082">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1082">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="31131-1083">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1083">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---labelmousedblclick"></a><span data-ttu-id="31131-1084">例 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1084">Examples - labelMouseDblClick</span></span>

<span data-ttu-id="31131-1085">次の例は、Infolog に labelMouseDblClick イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1085">The following example shows how to display the parameters of a labelMouseDblClick event in the Infolog.</span></span>

```xpp
public int labelMouseDblClick(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    ; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-labelmousedown"></a><span data-ttu-id="31131-1086">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1086">Method labelMouseDown</span></span>

<span data-ttu-id="31131-1087">ユーザーがコントロールのラベル上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1087">Is called when the user clicks the mouse button over the label for the control.</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="31131-1088">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1088">Parameters - labelMouseDown</span></span>

<span data-ttu-id="31131-1089">x</span><span class="sxs-lookup"><span data-stu-id="31131-1089">x</span></span>  
<span data-ttu-id="31131-1090">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1090">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1091">y</span><span class="sxs-lookup"><span data-stu-id="31131-1091">y</span></span>  
<span data-ttu-id="31131-1092">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1092">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1093">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1093">button</span></span>  
<span data-ttu-id="31131-1094">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1094">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1095">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1095">Ctrl</span></span>  
<span data-ttu-id="31131-1096">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1096">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1097">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1097">Shift</span></span>  
<span data-ttu-id="31131-1098">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1098">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---labelmousedown"></a><span data-ttu-id="31131-1099">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1099">Return Value - labelMouseDown</span></span>

<span data-ttu-id="31131-1100">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-1100">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---labelmousedown"></a><span data-ttu-id="31131-1101">備考 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1101">Remarks - labelMouseDown</span></span>

<span data-ttu-id="31131-1102">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1102">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="31131-1103">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1103">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---labelmousedown"></a><span data-ttu-id="31131-1104">例 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1104">Examples - labelMouseDown</span></span>

<span data-ttu-id="31131-1105">次の例は、Infolog に labelMouseDown イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1105">The following example shows how to display the parameters of a labelMouseDown event in the Infolog.</span></span>

```xpp
public int labelMouseDown(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-labelmouseup"></a><span data-ttu-id="31131-1106">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1106">Method labelMouseUp</span></span>

<span data-ttu-id="31131-1107">ユーザーがコントロールのラベル上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1107">Is called when the user releases the mouse button over the label for the control.</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="31131-1108">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1108">Parameters - labelMouseUp</span></span>

<span data-ttu-id="31131-1109">x</span><span class="sxs-lookup"><span data-stu-id="31131-1109">x</span></span>  
<span data-ttu-id="31131-1110">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1110">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1111">y</span><span class="sxs-lookup"><span data-stu-id="31131-1111">y</span></span>  
<span data-ttu-id="31131-1112">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1112">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1113">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1113">button</span></span>  
<span data-ttu-id="31131-1114">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1114">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1115">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1115">Ctrl</span></span>  
<span data-ttu-id="31131-1116">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1116">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1117">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1117">Shift</span></span>  
<span data-ttu-id="31131-1118">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1118">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---labelmouseup"></a><span data-ttu-id="31131-1119">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1119">Return Value - labelMouseUp</span></span>

<span data-ttu-id="31131-1120">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-1120">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---labelmouseup"></a><span data-ttu-id="31131-1121">備考 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1121">Remarks - labelMouseUp</span></span>

<span data-ttu-id="31131-1122">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1122">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="31131-1123">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1123">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---labelmouseup"></a><span data-ttu-id="31131-1124">例 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1124">Examples - labelMouseUp</span></span>

<span data-ttu-id="31131-1125">次の例は、Infolog に labelMouseUp イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1125">The following example shows how to display the parameters of a labelMouseUp event in the Infolog.</span></span>

```xpp
public int labelMouseUp(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    ; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-labelposition"></a><span data-ttu-id="31131-1126">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="31131-1126">Method labelPosition</span></span>

<span data-ttu-id="31131-1127">コントロールのラベルの位置を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1127">Sets or returns the position of the label for the control.</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="31131-1128">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="31131-1128">Parameters - labelPosition</span></span>

<span data-ttu-id="31131-1129">値</span><span class="sxs-lookup"><span data-stu-id="31131-1129">value</span></span>  
<span data-ttu-id="31131-1130">ラベル位置に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1130">The value to assign to the label position; optional.</span></span>

### <a name="return-value---labelposition"></a><span data-ttu-id="31131-1131">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="31131-1131">Return Value - labelPosition</span></span>

<span data-ttu-id="31131-1132">ラベルの位置を表す整数。</span><span class="sxs-lookup"><span data-stu-id="31131-1132">An integer that represents the position of the label.</span></span>

### <a name="remarks---labelposition"></a><span data-ttu-id="31131-1133">備考 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="31131-1133">Remarks - labelPosition</span></span>

<span data-ttu-id="31131-1134">値パラメーターが 0 (ゼロ) に設定されている場合、ラベルは、コントロールの左側に配置されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1134">If the value parameter is set to 0 (zero), the label is put to the left of the control.</span></span> <span data-ttu-id="31131-1135">値パラメーターが 1 に設定されている場合、ラベルはコントロールの上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1135">If the value parameter is set to 1, the label is put above the control.</span></span> <span data-ttu-id="31131-1136">0 (ゼロ) の戻り値は、ラベルがコントロールの左側に置かれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1136">A return value of 0 (zero) indicates that the label is put to the left of the control.</span></span> <span data-ttu-id="31131-1137">1 の戻り値は、ラベルがコントロールの上に置かれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1137">A return value of 1 indicates that the label is put above the control.</span></span>

### <a name="examples---labelposition"></a><span data-ttu-id="31131-1138">例 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="31131-1138">Examples - labelPosition</span></span>

<span data-ttu-id="31131-1139">次の例は、ラベルの位置を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1139">The following example shows how to return and set the label position.</span></span>

```xpp
// Retrieve the label position. 
info (strfmt("label: %1", this.labelPosition())); 
// Set the label position. 
this.labelPosition(1);  // 1 == Above, 0 == Left
```

## <a name="method-labelunderline"></a><span data-ttu-id="31131-1140">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="31131-1140">Method labelUnderline</span></span>

<span data-ttu-id="31131-1141">コントロールのラベルのテキストが下線付きで表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1141">Sets or returns a value that indicates whether the text in the label of the control is underlined.</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="31131-1142">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="31131-1142">Parameters - labelUnderline</span></span>

<span data-ttu-id="31131-1143">値</span><span class="sxs-lookup"><span data-stu-id="31131-1143">value</span></span>  
<span data-ttu-id="31131-1144">コントロールのラベルの下線設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1144">The value to assign to the underline setting of the label of the control; optional.</span></span>

### <a name="return-value---labelunderline"></a><span data-ttu-id="31131-1145">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="31131-1145">Return Value - labelUnderline</span></span>

<span data-ttu-id="31131-1146">コントロールのラベル内のテキストが下線付きである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-1146">true if the text in the label of the control is underlined; otherwise, false.</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="31131-1147">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1147">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="31131-1148">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1148">Parameters - labelWidth</span></span>

<span data-ttu-id="31131-1149">値</span><span class="sxs-lookup"><span data-stu-id="31131-1149">value</span></span>  

<!-- -->

<span data-ttu-id="31131-1150">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1150">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="31131-1151">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1151">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="31131-1152">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1152">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="31131-1153">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1153">Parameters - labelWidthMode</span></span>

<span data-ttu-id="31131-1154">値</span><span class="sxs-lookup"><span data-stu-id="31131-1154">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="31131-1155">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1155">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="31131-1156">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1156">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="31131-1157">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1157">Parameters - labelWidthValue</span></span>

<span data-ttu-id="31131-1158">値</span><span class="sxs-lookup"><span data-stu-id="31131-1158">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="31131-1159">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1159">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="31131-1160">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="31131-1160">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="31131-1161">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="31131-1161">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="31131-1162">メソッド left</span><span class="sxs-lookup"><span data-stu-id="31131-1162">Method left</span></span>

<span data-ttu-id="31131-1163">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1163">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="31131-1164">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="31131-1164">Parameters - left</span></span>

<span data-ttu-id="31131-1165">値</span><span class="sxs-lookup"><span data-stu-id="31131-1165">value</span></span>  
<span data-ttu-id="31131-1166">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1166">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="31131-1167">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1167">mode</span></span>  
<span data-ttu-id="31131-1168">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1168">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="31131-1169">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="31131-1169">Return Value - left</span></span>

<span data-ttu-id="31131-1170">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="31131-1170">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="31131-1171">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="31131-1171">Method leftMode</span></span>

<span data-ttu-id="31131-1172">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1172">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="31131-1173">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="31131-1173">Parameters - leftMode</span></span>

<span data-ttu-id="31131-1174">値</span><span class="sxs-lookup"><span data-stu-id="31131-1174">value</span></span>  
<span data-ttu-id="31131-1175">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1175">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="31131-1176">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="31131-1176">Return Value - leftMode</span></span>

<span data-ttu-id="31131-1177">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="31131-1177">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="31131-1178">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="31131-1178">Method leftValue</span></span>

<span data-ttu-id="31131-1179">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1179">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="31131-1180">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="31131-1180">Parameters - leftValue</span></span>

<span data-ttu-id="31131-1181">値</span><span class="sxs-lookup"><span data-stu-id="31131-1181">value</span></span>  
<span data-ttu-id="31131-1182">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1182">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="31131-1183">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="31131-1183">Return Value - leftValue</span></span>

<span data-ttu-id="31131-1184">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="31131-1184">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="31131-1185">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="31131-1185">Method markAsUserAdd</span></span>

<span data-ttu-id="31131-1186">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="31131-1186">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="31131-1187">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="31131-1187">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="31131-1188">値</span><span class="sxs-lookup"><span data-stu-id="31131-1188">value</span></span>  
<span data-ttu-id="31131-1189">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1189">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="31131-1190">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="31131-1190">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="31131-1191">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-1191">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="31131-1192">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="31131-1192">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="31131-1193">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="31131-1193">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="31131-1194">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1194">Method mouseDblClick</span></span>

<span data-ttu-id="31131-1195">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1195">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="31131-1196">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1196">Parameters - mouseDblClick</span></span>

<span data-ttu-id="31131-1197">x</span><span class="sxs-lookup"><span data-stu-id="31131-1197">x</span></span>  
<span data-ttu-id="31131-1198">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1198">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1199">y</span><span class="sxs-lookup"><span data-stu-id="31131-1199">y</span></span>  
<span data-ttu-id="31131-1200">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1200">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1201">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1201">button</span></span>  
<span data-ttu-id="31131-1202">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1202">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1203">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1203">Ctrl</span></span>  
<span data-ttu-id="31131-1204">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1204">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1205">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1205">Shift</span></span>  
<span data-ttu-id="31131-1206">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1206">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="31131-1207">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1207">Return Value - mouseDblClick</span></span>

<span data-ttu-id="31131-1208">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-1208">0 (zero) if the event has been handled.</span></span>

### <a name="examples---mousedblclick"></a><span data-ttu-id="31131-1209">例 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="31131-1209">Examples - mouseDblClick</span></span>

<span data-ttu-id="31131-1210">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1210">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="31131-1211">次の例は、Infolog に mouseDblClick イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1211">The following example shows how to display the parameters of a mouseDblClick event in the Infolog.</span></span>

```xpp
public int mouseDblClick(int x,  
                         int y,  
                         int button, 
                         boolean Ctrl, 
                         boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousedown"></a><span data-ttu-id="31131-1212">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1212">Method mouseDown</span></span>

<span data-ttu-id="31131-1213">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1213">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="31131-1214">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1214">Parameters - mouseDown</span></span>

<span data-ttu-id="31131-1215">x</span><span class="sxs-lookup"><span data-stu-id="31131-1215">x</span></span>  
<span data-ttu-id="31131-1216">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1216">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1217">y</span><span class="sxs-lookup"><span data-stu-id="31131-1217">y</span></span>  
<span data-ttu-id="31131-1218">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1218">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1219">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1219">button</span></span>  
<span data-ttu-id="31131-1220">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1220">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1221">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1221">Ctrl</span></span>  
<span data-ttu-id="31131-1222">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1222">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1223">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1223">Shift</span></span>  
<span data-ttu-id="31131-1224">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1224">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="31131-1225">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1225">Return Value - mouseDown</span></span>

<span data-ttu-id="31131-1226">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-1226">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="31131-1227">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1227">Remarks - mouseDown</span></span>

<span data-ttu-id="31131-1228">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1228">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="31131-1229">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1229">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---mousedown"></a><span data-ttu-id="31131-1230">例 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="31131-1230">Examples - mouseDown</span></span>

<span data-ttu-id="31131-1231">次の例は、Infolog に mouseDown イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1231">The following example shows how to display the parameters of a mouseDown event in the Infolog.</span></span>

```xpp
public int mouseDown(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    ; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousemove"></a><span data-ttu-id="31131-1232">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="31131-1232">Method mouseMove</span></span>

<span data-ttu-id="31131-1233">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1233">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="31131-1234">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="31131-1234">Parameters - mouseMove</span></span>

<span data-ttu-id="31131-1235">x</span><span class="sxs-lookup"><span data-stu-id="31131-1235">x</span></span>  
<span data-ttu-id="31131-1236">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1236">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1237">y</span><span class="sxs-lookup"><span data-stu-id="31131-1237">y</span></span>  
<span data-ttu-id="31131-1238">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1238">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1239">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1239">button</span></span>  
<span data-ttu-id="31131-1240">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1240">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1241">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1241">Ctrl</span></span>  
<span data-ttu-id="31131-1242">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1242">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1243">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1243">Shift</span></span>  
<span data-ttu-id="31131-1244">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1244">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="31131-1245">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="31131-1245">Return Value - mouseMove</span></span>

<span data-ttu-id="31131-1246">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-1246">0 (zero) if the event has been handled.</span></span>

### <a name="examples---mousemove"></a><span data-ttu-id="31131-1247">例 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="31131-1247">Examples - mouseMove</span></span>

<span data-ttu-id="31131-1248">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1248">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="31131-1249">次の例は、Infolog に mouseMove イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1249">The following example shows how to display the parameters of a mouseMove event in the Infolog.</span></span>

```xpp
public int mouseMove(int x,  
                     int y,  
                     int button, 
                     boolean Ctrl, 
                     boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mouseup"></a><span data-ttu-id="31131-1250">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1250">Method mouseUp</span></span>

<span data-ttu-id="31131-1251">ユーザーがコントロール上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1251">Is called when the user releases the mouse button over the control.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="31131-1252">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1252">Parameters - mouseUp</span></span>

<span data-ttu-id="31131-1253">x</span><span class="sxs-lookup"><span data-stu-id="31131-1253">x</span></span>  
<span data-ttu-id="31131-1254">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1254">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1255">y</span><span class="sxs-lookup"><span data-stu-id="31131-1255">y</span></span>  
<span data-ttu-id="31131-1256">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1256">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1257">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1257">button</span></span>  
<span data-ttu-id="31131-1258">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1258">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1259">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1259">Ctrl</span></span>  
<span data-ttu-id="31131-1260">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1260">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1261">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1261">Shift</span></span>  
<span data-ttu-id="31131-1262">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1262">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="31131-1263">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1263">Return Value - mouseUp</span></span>

<span data-ttu-id="31131-1264">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="31131-1264">0 (zero) if the event has been handled.</span></span>

### <a name="examples---mouseup"></a><span data-ttu-id="31131-1265">例 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="31131-1265">Examples - mouseUp</span></span>

<span data-ttu-id="31131-1266">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1266">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="31131-1267">次の例は、Infolog に mouseUp イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1267">The following example shows how to display the parameters of a mouseUp event in the Infolog.</span></span>

```xpp
public int mouseUp(int x,  
                   int y,  
                   int button, 
                   boolean Ctrl, 
                   boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-name"></a><span data-ttu-id="31131-1268">メソッド名</span><span class="sxs-lookup"><span data-stu-id="31131-1268">Method name</span></span>

<span data-ttu-id="31131-1269">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1269">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="31131-1270">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="31131-1270">Parameters - name</span></span>

<span data-ttu-id="31131-1271">値</span><span class="sxs-lookup"><span data-stu-id="31131-1271">value</span></span>  
<span data-ttu-id="31131-1272">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1272">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="31131-1273">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="31131-1273">Return Value - name</span></span>

<span data-ttu-id="31131-1274">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="31131-1274">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="31131-1275">備考 - name</span><span class="sxs-lookup"><span data-stu-id="31131-1275">Remarks - name</span></span>

<span data-ttu-id="31131-1276">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="31131-1276">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="31131-1277">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="31131-1277">It must start with a letter.</span></span>
-   <span data-ttu-id="31131-1278">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="31131-1278">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="31131-1279">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="31131-1279">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="31131-1280">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="31131-1280">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="31131-1281">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="31131-1281">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="31131-1282">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="31131-1282">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="31131-1283">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="31131-1283">Parameters - neededPermission</span></span>

<span data-ttu-id="31131-1284">値</span><span class="sxs-lookup"><span data-stu-id="31131-1284">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="31131-1285">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="31131-1285">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="31131-1286">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="31131-1286">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="31131-1287">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="31131-1287">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="31131-1288">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="31131-1288">Method parentControl</span></span>

<span data-ttu-id="31131-1289">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="31131-1289">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="31131-1290">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="31131-1290">Return Value - parentControl</span></span>

<span data-ttu-id="31131-1291">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="31131-1291">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="31131-1292">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="31131-1292">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="31131-1293">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="31131-1293">Parameters - previewPartRef</span></span>

<span data-ttu-id="31131-1294">値</span><span class="sxs-lookup"><span data-stu-id="31131-1294">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="31131-1295">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="31131-1295">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="31131-1296">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="31131-1296">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="31131-1297">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="31131-1297">Parameters - promptrect</span></span>

<span data-ttu-id="31131-1298">値</span><span class="sxs-lookup"><span data-stu-id="31131-1298">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="31131-1299">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="31131-1299">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="31131-1300">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="31131-1300">Method securityKey</span></span>

<span data-ttu-id="31131-1301">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1301">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="31131-1302">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="31131-1302">Parameters - securityKey</span></span>

<span data-ttu-id="31131-1303">値</span><span class="sxs-lookup"><span data-stu-id="31131-1303">value</span></span>  
<span data-ttu-id="31131-1304">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1304">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="31131-1305">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="31131-1305">Return Value - securityKey</span></span>

<span data-ttu-id="31131-1306">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="31131-1306">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="examples---securitykey"></a><span data-ttu-id="31131-1307">例 - securityKey</span><span class="sxs-lookup"><span data-stu-id="31131-1307">Examples - securityKey</span></span>

<span data-ttu-id="31131-1308">次の例は、コントロールのセキュリティ キー IDの取得と割り当てを示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1308">The following example shows the retrieval and assignment of a security key ID for a control.</span></span>

```xpp
DictSecurityKey dsk; 
securityKeyId ski; 
; 
// objCtrl previously assigned. 
// Assign a security key ID to the control. 
objCtrl.securityKey(securitykeynum(AdminDaily)); 
// Retrieve the security key ID from the control. 
ski = objCtrl.securityKey(); 
if (ski != 0) 
{ 
    dsk = new DictSecurityKey(ski); 
    if (dsk) 
    { 
        print strfmt("Security Key ID: %1 Security Key Name: %2", 
                     ski, 
                     dsk.name()); 
    } 
}
```

## <a name="method-selection"></a><span data-ttu-id="31131-1309">メソッド selection</span><span class="sxs-lookup"><span data-stu-id="31131-1309">Method selection</span></span>

```xpp
public int selection([int value])
```

### <a name="parameters---selection"></a><span data-ttu-id="31131-1310">パラメーター - selection</span><span class="sxs-lookup"><span data-stu-id="31131-1310">Parameters - selection</span></span>

<span data-ttu-id="31131-1311">値</span><span class="sxs-lookup"><span data-stu-id="31131-1311">value</span></span>  

### <a name="return-value---selection"></a><span data-ttu-id="31131-1312">戻り値 - selection</span><span class="sxs-lookup"><span data-stu-id="31131-1312">Return Value - selection</span></span>

## <a name="method-selectionchange"></a><span data-ttu-id="31131-1313">メソッド selectionChange</span><span class="sxs-lookup"><span data-stu-id="31131-1313">Method selectionChange</span></span>

<span data-ttu-id="31131-1314">ユーザーがコンボ ボックス コントロールで選択した項目を変更したことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1314">Indicates that the user has changed the selected item in the combo box control.</span></span>

```xpp
public int selectionChange()
```

### <a name="return-value---selectionchange"></a><span data-ttu-id="31131-1315">戻り値 - selectionChange</span><span class="sxs-lookup"><span data-stu-id="31131-1315">Return Value - selectionChange</span></span>

<span data-ttu-id="31131-1316">イベントが正常に処理された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-1316">true if the event was processed successfully; otherwise, false.</span></span>

### <a name="examples---selectionchange"></a><span data-ttu-id="31131-1317">例 - selectionChange</span><span class="sxs-lookup"><span data-stu-id="31131-1317">Examples - selectionChange</span></span>

<span data-ttu-id="31131-1318">次の例は、ユーザーがコンボ ボックス コントロールで選択した項目を変更するときに、Infolog メッセージを表示するために selectionChange メソッドを上書きする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1318">The following example shows how the selectionChange method can be overridden to display an Infolog message when the user changes the selected item in the combo box control.</span></span>

```xpp
public int selectionChange() 
{ 
    int ret; 
    info("The selection has changed."); 
    ret = super(); 
    return ret; 
}
```

## <a name="method-selecttext"></a><span data-ttu-id="31131-1319">メソッド selectText</span><span class="sxs-lookup"><span data-stu-id="31131-1319">Method selectText</span></span>

```xpp
public int selectText(str string)
```

### <a name="parameters---selecttext"></a><span data-ttu-id="31131-1320">パラメーター - selectText</span><span class="sxs-lookup"><span data-stu-id="31131-1320">Parameters - selectText</span></span>

<span data-ttu-id="31131-1321">文字列</span><span class="sxs-lookup"><span data-stu-id="31131-1321">string</span></span>  

### <a name="return-value---selecttext"></a><span data-ttu-id="31131-1322">戻り値 - selectText</span><span class="sxs-lookup"><span data-stu-id="31131-1322">Return Value - selectText</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="31131-1323">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="31131-1323">Method showContextMenu</span></span>

<span data-ttu-id="31131-1324">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1324">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="31131-1325">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="31131-1325">Parameters - showContextMenu</span></span>

<span data-ttu-id="31131-1326">menuHandle</span><span class="sxs-lookup"><span data-stu-id="31131-1326">menuHandle</span></span>  
<span data-ttu-id="31131-1327">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="31131-1327">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="31131-1328">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="31131-1328">Return Value - showContextMenu</span></span>

<span data-ttu-id="31131-1329">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1329">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="31131-1330">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="31131-1330">Method showLabel</span></span>

<span data-ttu-id="31131-1331">コントロールのラベルがフォームに表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1331">Sets or returns a value that indicates whether the label for the control is displayed in the form.</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="31131-1332">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="31131-1332">Parameters - showLabel</span></span>

<span data-ttu-id="31131-1333">値</span><span class="sxs-lookup"><span data-stu-id="31131-1333">value</span></span>  
<span data-ttu-id="31131-1334">コントロールの showLabel プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="31131-1334">The value to assign to the showLabel property for the control.</span></span>

### <a name="return-value---showlabel"></a><span data-ttu-id="31131-1335">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="31131-1335">Return Value - showLabel</span></span>

<span data-ttu-id="31131-1336">ラベルを表示する必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-1336">true if the label should be displayed; otherwise, false.</span></span>

### <a name="examples---showlabel"></a><span data-ttu-id="31131-1337">例 - showLabel</span><span class="sxs-lookup"><span data-stu-id="31131-1337">Examples - showLabel</span></span>

<span data-ttu-id="31131-1338">次の例は、コントロールの showLabel プロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1338">The following example shows how to return and set the showLabel property for a control.</span></span>

```xpp
// Return the showLabel value. 
info(strfmt("showLabel: %1", this.showLabel())); 
// Set the showLabel value. 
this.showLabel(false);
```

## <a name="method-skip"></a><span data-ttu-id="31131-1339">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="31131-1339">Method skip</span></span>

<span data-ttu-id="31131-1340">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1340">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="31131-1341">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="31131-1341">Parameters - skip</span></span>

<span data-ttu-id="31131-1342">値</span><span class="sxs-lookup"><span data-stu-id="31131-1342">value</span></span>  
<span data-ttu-id="31131-1343">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1343">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="31131-1344">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="31131-1344">Return Value - skip</span></span>

<span data-ttu-id="31131-1345">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-1345">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="31131-1346">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="31131-1346">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="31131-1347">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="31131-1347">Parameters - sort</span></span>

<span data-ttu-id="31131-1348">sortDirection</span><span class="sxs-lookup"><span data-stu-id="31131-1348">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="31131-1349">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="31131-1349">Return Value - sort</span></span>

## <a name="method-text"></a><span data-ttu-id="31131-1350">メソッド text</span><span class="sxs-lookup"><span data-stu-id="31131-1350">Method text</span></span>

<span data-ttu-id="31131-1351">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1351">Sets or returns the text for the control.</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="31131-1352">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="31131-1352">Parameters - text</span></span>

<span data-ttu-id="31131-1353">値</span><span class="sxs-lookup"><span data-stu-id="31131-1353">value</span></span>  
<span data-ttu-id="31131-1354">コントロールのテキストとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1354">The value to assign as the text for the control; optional.</span></span>

### <a name="return-value---text"></a><span data-ttu-id="31131-1355">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="31131-1355">Return Value - text</span></span>

<span data-ttu-id="31131-1356">コントロールのテキスト。コントロールにテキストが割り当てられていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="31131-1356">The text for the control; an empty string if no text has been assigned for the control.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="31131-1357">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="31131-1357">Method toolTip</span></span>

<span data-ttu-id="31131-1358">コントロールのツールヒント テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1358">Returns the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="31131-1359">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="31131-1359">Return Value - toolTip</span></span>

<span data-ttu-id="31131-1360">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="31131-1360">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="31131-1361">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="31131-1361">Remarks - toolTip</span></span>

<span data-ttu-id="31131-1362">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="31131-1362">The method can be overridden to provide a value to the toolTip method.</span></span>

### <a name="examples---tooltip"></a><span data-ttu-id="31131-1363">例 - toolTip</span><span class="sxs-lookup"><span data-stu-id="31131-1363">Examples - toolTip</span></span>

<span data-ttu-id="31131-1364">次の例は、toolTip メソッドを上書きする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1364">The following example shows how to override the toolTip method.</span></span>

```xpp
str toolTip() 
{ 
    return "Account numbers of customers eligible for discount"; 
}
```

## <a name="method-top"></a><span data-ttu-id="31131-1365">メソッド top</span><span class="sxs-lookup"><span data-stu-id="31131-1365">Method top</span></span>

<span data-ttu-id="31131-1366">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1366">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="31131-1367">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="31131-1367">Parameters - top</span></span>

<span data-ttu-id="31131-1368">値</span><span class="sxs-lookup"><span data-stu-id="31131-1368">value</span></span>  
<span data-ttu-id="31131-1369">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1369">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="31131-1370">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1370">mode</span></span>  
<span data-ttu-id="31131-1371">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1371">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="31131-1372">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="31131-1372">Return Value - top</span></span>

<span data-ttu-id="31131-1373">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="31131-1373">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="31131-1374">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="31131-1374">Method topMode</span></span>

<span data-ttu-id="31131-1375">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1375">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="31131-1376">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="31131-1376">Parameters - topMode</span></span>

<span data-ttu-id="31131-1377">値</span><span class="sxs-lookup"><span data-stu-id="31131-1377">value</span></span>  
<span data-ttu-id="31131-1378">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1378">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="31131-1379">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="31131-1379">Return Value - topMode</span></span>

<span data-ttu-id="31131-1380">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="31131-1380">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="31131-1381">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="31131-1381">Method topValue</span></span>

<span data-ttu-id="31131-1382">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1382">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="31131-1383">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="31131-1383">Parameters - topValue</span></span>

<span data-ttu-id="31131-1384">値</span><span class="sxs-lookup"><span data-stu-id="31131-1384">value</span></span>  
<span data-ttu-id="31131-1385">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1385">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="31131-1386">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="31131-1386">Return Value - topValue</span></span>

<span data-ttu-id="31131-1387">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="31131-1387">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="31131-1388">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="31131-1388">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="31131-1389">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="31131-1389">Parameters - type</span></span>

<span data-ttu-id="31131-1390">値</span><span class="sxs-lookup"><span data-stu-id="31131-1390">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="31131-1391">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="31131-1391">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="31131-1392">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="31131-1392">Method underline</span></span>

<span data-ttu-id="31131-1393">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1393">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="31131-1394">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="31131-1394">Parameters - underline</span></span>

<span data-ttu-id="31131-1395">値</span><span class="sxs-lookup"><span data-stu-id="31131-1395">value</span></span>  
<span data-ttu-id="31131-1396">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1396">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="31131-1397">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="31131-1397">Return Value - underline</span></span>

<span data-ttu-id="31131-1398">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="31131-1398">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="31131-1399">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="31131-1399">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="31131-1400">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="31131-1400">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="31131-1401">データ</span><span class="sxs-lookup"><span data-stu-id="31131-1401">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="31131-1402">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="31131-1402">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="31131-1403">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="31131-1403">Method userData</span></span>

<span data-ttu-id="31131-1404">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1404">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="31131-1405">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="31131-1405">Parameters - userData</span></span>

<span data-ttu-id="31131-1406">値</span><span class="sxs-lookup"><span data-stu-id="31131-1406">value</span></span>  
<span data-ttu-id="31131-1407">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1407">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="31131-1408">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="31131-1408">Return Value - userData</span></span>

<span data-ttu-id="31131-1409">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="31131-1409">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="31131-1410">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="31131-1410">Method userDataItem</span></span>

<span data-ttu-id="31131-1411">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1411">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="31131-1412">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="31131-1412">Parameters - userDataItem</span></span>

<span data-ttu-id="31131-1413">値</span><span class="sxs-lookup"><span data-stu-id="31131-1413">value</span></span>  
<span data-ttu-id="31131-1414">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1414">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="31131-1415">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="31131-1415">Return Value - userDataItem</span></span>

<span data-ttu-id="31131-1416">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="31131-1416">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="31131-1417">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="31131-1417">Method userDataItems</span></span>

<span data-ttu-id="31131-1418">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1418">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="31131-1419">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="31131-1419">Parameters - userDataItems</span></span>

<span data-ttu-id="31131-1420">値</span><span class="sxs-lookup"><span data-stu-id="31131-1420">value</span></span>  
<span data-ttu-id="31131-1421">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1421">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="31131-1422">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="31131-1422">Return Value - userDataItems</span></span>

<span data-ttu-id="31131-1423">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="31131-1423">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="31131-1424">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="31131-1424">Method userDisable</span></span>

<span data-ttu-id="31131-1425">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1425">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="31131-1426">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="31131-1426">Parameters - userDisable</span></span>

<span data-ttu-id="31131-1427">値</span><span class="sxs-lookup"><span data-stu-id="31131-1427">value</span></span>  
<span data-ttu-id="31131-1428">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1428">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="31131-1429">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="31131-1429">Return Value - userDisable</span></span>

<span data-ttu-id="31131-1430">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="31131-1430">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="31131-1431">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="31131-1431">Method userHeight</span></span>

<span data-ttu-id="31131-1432">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1432">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="31131-1433">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="31131-1433">Parameters - userHeight</span></span>

<span data-ttu-id="31131-1434">値</span><span class="sxs-lookup"><span data-stu-id="31131-1434">value</span></span>  
<span data-ttu-id="31131-1435">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1435">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="31131-1436">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="31131-1436">Return Value - userHeight</span></span>

<span data-ttu-id="31131-1437">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="31131-1437">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="31131-1438">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="31131-1438">Method userHide</span></span>

<span data-ttu-id="31131-1439">フォーム コンボ ボックス コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1439">Returns or sets the value that indicates whether the form combo box control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="31131-1440">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="31131-1440">Parameters - userHide</span></span>

<span data-ttu-id="31131-1441">値</span><span class="sxs-lookup"><span data-stu-id="31131-1441">value</span></span>  
<span data-ttu-id="31131-1442">コントロールがユーザーから非表示になっているどうかを示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1442">A value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="31131-1443">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="31131-1443">Return Value - userHide</span></span>

<span data-ttu-id="31131-1444">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="31131-1444">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="31131-1445">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="31131-1445">Remarks - userHide</span></span>

<span data-ttu-id="31131-1446">ユーザーは、コンボ ボックス コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コンボ ボックス コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1446">The user specifies whether a combo box control is hidden by right-clicking the control when it can be viewed or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="31131-1447">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="31131-1447">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="31131-1448">userHide メソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="31131-1448">The userHide method lets you programmatically determine and set the value.</span></span>

### <a name="examples---userhide"></a><span data-ttu-id="31131-1449">例 - userHide</span><span class="sxs-lookup"><span data-stu-id="31131-1449">Examples - userHide</span></span>

<span data-ttu-id="31131-1450">次の例は、コンボ ボックス コントロールがユーザーから隠されているかどうかを示す値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1450">The following example shows how to return and set the value that indicates whether the combo box control is hidden from the user.</span></span>

```xpp
int nUserHide; 
// The ctrl variable was previously assigned  
// as a form combo box control variable. 
// Retrieve the userHide value. 
nUserHide = ctrl.userHide(); 
// Set the userHide value. 
ctrl.userHide(1);
```

## <a name="method-userorgcontainer"></a><span data-ttu-id="31131-1451">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="31131-1451">Method userOrgContainer</span></span>

<span data-ttu-id="31131-1452">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1452">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="31131-1453">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="31131-1453">Parameters - userOrgContainer</span></span>

<span data-ttu-id="31131-1454">値</span><span class="sxs-lookup"><span data-stu-id="31131-1454">value</span></span>  
<span data-ttu-id="31131-1455">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1455">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="31131-1456">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="31131-1456">Return Value - userOrgContainer</span></span>

<span data-ttu-id="31131-1457">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="31131-1457">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="31131-1458">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="31131-1458">Method userOrgSibling</span></span>

<span data-ttu-id="31131-1459">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1459">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="31131-1460">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="31131-1460">Parameters - userOrgSibling</span></span>

<span data-ttu-id="31131-1461">値</span><span class="sxs-lookup"><span data-stu-id="31131-1461">value</span></span>  
<span data-ttu-id="31131-1462">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1462">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="31131-1463">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="31131-1463">Return Value - userOrgSibling</span></span>

<span data-ttu-id="31131-1464">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="31131-1464">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="31131-1465">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="31131-1465">Method userPromptText</span></span>

<span data-ttu-id="31131-1466">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1466">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="31131-1467">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="31131-1467">Parameters - userPromptText</span></span>

<span data-ttu-id="31131-1468">値</span><span class="sxs-lookup"><span data-stu-id="31131-1468">value</span></span>  
<span data-ttu-id="31131-1469">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1469">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="31131-1470">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="31131-1470">Return Value - userPromptText</span></span>

<span data-ttu-id="31131-1471">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="31131-1471">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="31131-1472">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="31131-1472">Method userSecurityLevel</span></span>

<span data-ttu-id="31131-1473">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1473">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="31131-1474">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="31131-1474">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="31131-1475">値</span><span class="sxs-lookup"><span data-stu-id="31131-1475">value</span></span>  
<span data-ttu-id="31131-1476">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1476">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="31131-1477">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="31131-1477">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="31131-1478">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="31131-1478">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="31131-1479">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="31131-1479">Method userSkip</span></span>

<span data-ttu-id="31131-1480">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コンボ ボックス コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1480">Sets or returns the value that indicates whether the form combo box control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="31131-1481">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="31131-1481">Parameters - userSkip</span></span>

<span data-ttu-id="31131-1482">値</span><span class="sxs-lookup"><span data-stu-id="31131-1482">value</span></span>  
<span data-ttu-id="31131-1483">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1483">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="31131-1484">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="31131-1484">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="31131-1485">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="31131-1485">Return Value - userSkip</span></span>

<span data-ttu-id="31131-1486">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="31131-1486">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="examples---userskip"></a><span data-ttu-id="31131-1487">例 - userSkip</span><span class="sxs-lookup"><span data-stu-id="31131-1487">Examples - userSkip</span></span>

<span data-ttu-id="31131-1488">次の例は、userSkip プロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1488">The following example shows how to return and set the userSkip property.</span></span>

```xpp
int nUserSkip 
// The ctrl variable was previously assigned as a 
// FormComboBoxControl variable. 
// Return the userSkip property. 
nUserSkip = ctrl.userSkip(); 
// Set the userSkip property. 
ctrl.userSkip(1);
```

## <a name="method-userwidth"></a><span data-ttu-id="31131-1489">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1489">Method userWidth</span></span>

<span data-ttu-id="31131-1490">ピクセル単位でフォーム コンボ ボックス コントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1490">Sets or returns the width of the form combo box control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="31131-1491">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1491">Parameters - userWidth</span></span>

<span data-ttu-id="31131-1492">値</span><span class="sxs-lookup"><span data-stu-id="31131-1492">value</span></span>  
<span data-ttu-id="31131-1493">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1493">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="31131-1494">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1494">Return Value - userWidth</span></span>

<span data-ttu-id="31131-1495">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="31131-1495">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="31131-1496">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1496">Remarks - userWidth</span></span>

<span data-ttu-id="31131-1497">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1497">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="31131-1498">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="31131-1498">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="31131-1499">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="31131-1499">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="examples---userwidth"></a><span data-ttu-id="31131-1500">例 - userWidth</span><span class="sxs-lookup"><span data-stu-id="31131-1500">Examples - userWidth</span></span>

<span data-ttu-id="31131-1501">次の例は、フォーム コンボ ボックス コントロールのユーザーの幅を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1501">The following example shows how to return and set the user width of a form combo box control.</span></span>

```xpp
int nWidth; 
// The ctrl variable was previously defined  
// as the FormComboBoxControl variable. 
// Return the width. 
nWidth = ctrl.userWidth(); 
// Specify the width. 
ctrl.userWidth(90);  // 15 characters * 6 pixels == 90
```

## <a name="method-validate"></a><span data-ttu-id="31131-1502">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="31131-1502">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="31131-1503">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="31131-1503">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="31131-1504">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="31131-1504">Method verticalSpacing</span></span>

<span data-ttu-id="31131-1505">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1505">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="31131-1506">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="31131-1506">Parameters - verticalSpacing</span></span>

<span data-ttu-id="31131-1507">値</span><span class="sxs-lookup"><span data-stu-id="31131-1507">value</span></span>  
<span data-ttu-id="31131-1508">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1508">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="31131-1509">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1509">mode</span></span>  
<span data-ttu-id="31131-1510">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1510">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="31131-1511">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="31131-1511">Return Value - verticalSpacing</span></span>

<span data-ttu-id="31131-1512">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="31131-1512">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="31131-1513">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="31131-1513">Method verticalSpacingMode</span></span>

<span data-ttu-id="31131-1514">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1514">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="31131-1515">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="31131-1515">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="31131-1516">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1516">mode</span></span>  
<span data-ttu-id="31131-1517">コントロールの AutoMode 列挙値; オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1517">A AutoMode enumeration value for the control; optional.</span></span>

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="31131-1518">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="31131-1518">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="31131-1519">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="31131-1519">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="31131-1520">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="31131-1520">Method verticalSpacingValue</span></span>

<span data-ttu-id="31131-1521">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1521">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="31131-1522">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="31131-1522">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="31131-1523">値</span><span class="sxs-lookup"><span data-stu-id="31131-1523">value</span></span>  
<span data-ttu-id="31131-1524">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1524">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="31131-1525">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="31131-1525">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="31131-1526">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="31131-1526">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="31131-1527">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="31131-1527">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="31131-1528">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="31131-1528">Parameters - viewEditMode</span></span>

<span data-ttu-id="31131-1529">値</span><span class="sxs-lookup"><span data-stu-id="31131-1529">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="31131-1530">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="31131-1530">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="31131-1531">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="31131-1531">Method visible</span></span>

<span data-ttu-id="31131-1532">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="31131-1532">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="31131-1533">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="31131-1533">Parameters - visible</span></span>

<span data-ttu-id="31131-1534">値</span><span class="sxs-lookup"><span data-stu-id="31131-1534">value</span></span>  
<span data-ttu-id="31131-1535">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1535">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="31131-1536">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="31131-1536">Return Value - visible</span></span>

<span data-ttu-id="31131-1537">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="31131-1537">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="31131-1538">メソッド width</span><span class="sxs-lookup"><span data-stu-id="31131-1538">Method width</span></span>

<span data-ttu-id="31131-1539">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1539">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="31131-1540">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="31131-1540">Parameters - width</span></span>

<span data-ttu-id="31131-1541">値</span><span class="sxs-lookup"><span data-stu-id="31131-1541">value</span></span>  
<span data-ttu-id="31131-1542">幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1542">An integer value that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="31131-1543">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1543">mode</span></span>  
<span data-ttu-id="31131-1544">幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1544">An integer value that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="31131-1545">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="31131-1545">Return Value - width</span></span>

<span data-ttu-id="31131-1546">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="31131-1546">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="31131-1547">備考 - width</span><span class="sxs-lookup"><span data-stu-id="31131-1547">Remarks - width</span></span>

<span data-ttu-id="31131-1548">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1548">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="31131-1549">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="31131-1549">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="31131-1550">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1550">Mode</span></span>             | <span data-ttu-id="31131-1551">幅計算</span><span class="sxs-lookup"><span data-stu-id="31131-1551">Width calculation</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="31131-1552">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="31131-1552">-1 � Exact</span></span>       | <span data-ttu-id="31131-1553">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1553">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="31131-1554">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="31131-1554">0 � Auto</span></span>         | <span data-ttu-id="31131-1555">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1555">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="31131-1556">1 � 列の幅</span><span class="sxs-lookup"><span data-stu-id="31131-1556">1 � Column width</span></span> | <span data-ttu-id="31131-1557">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="31131-1557">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="31131-1558">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="31131-1558">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="31131-1559">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1559">Method widthMode</span></span>

<span data-ttu-id="31131-1560">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1560">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="31131-1561">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1561">Parameters - widthMode</span></span>

<span data-ttu-id="31131-1562">値</span><span class="sxs-lookup"><span data-stu-id="31131-1562">value</span></span>  
<span data-ttu-id="31131-1563">コントロール幅の計算方法を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1563">An integer value that indicates how a control width is calculated.</span></span> <span data-ttu-id="31131-1564">値は、Exact モードの場合は -1、Auto モードの場合は 0、Column width モードの場合は 1 になります。</span><span class="sxs-lookup"><span data-stu-id="31131-1564">The value can be -1 for Exact mode, 0 for Auto mode, or 1 for Column width mode.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="31131-1565">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1565">Return Value - widthMode</span></span>

<span data-ttu-id="31131-1566">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1566">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="31131-1567">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1567">Remarks - widthMode</span></span>

<span data-ttu-id="31131-1568">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="31131-1568">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="31131-1569">モード</span><span class="sxs-lookup"><span data-stu-id="31131-1569">Mode</span></span>         | <span data-ttu-id="31131-1570">幅計算。</span><span class="sxs-lookup"><span data-stu-id="31131-1570">Width Calculation.</span></span>                                                                        |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="31131-1571">正確</span><span class="sxs-lookup"><span data-stu-id="31131-1571">Exact</span></span>        | <span data-ttu-id="31131-1572">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1572">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="31131-1573">自動</span><span class="sxs-lookup"><span data-stu-id="31131-1573">Auto</span></span>         | <span data-ttu-id="31131-1574">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1574">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="31131-1575">列の幅</span><span class="sxs-lookup"><span data-stu-id="31131-1575">Column width</span></span> | <span data-ttu-id="31131-1576">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="31131-1576">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="31131-1577">計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="31131-1577">The width of the control might change when the calculation mode is set to Auto or Column width.</span></span>

### <a name="examples---widthmode"></a><span data-ttu-id="31131-1578">例 - widthMode</span><span class="sxs-lookup"><span data-stu-id="31131-1578">Examples - widthMode</span></span>

<span data-ttu-id="31131-1579">次の例は、フォーム コンボ ボックス コントロールの幅の計算モードを返す方法と設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1579">The following example shows how to return and set the width calculation mode for a combo box control in a form.</span></span>

```xpp
int nWidthMode; 
; 
// The ctrl variable was previously assigned 
// as a form combo box control variable. 
// Retrieve the width mode. 
nWidthMode = ctrl.widthMode (); 
// Set the width mode. 
ctrl.widthMode(-1); 
// Set the width. 
ctrl.widthValue(180);
```

## <a name="method-widthvalue"></a><span data-ttu-id="31131-1580">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1580">Method widthValue</span></span>

<span data-ttu-id="31131-1581">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1581">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="31131-1582">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1582">Parameters - widthValue</span></span>

<span data-ttu-id="31131-1583">値</span><span class="sxs-lookup"><span data-stu-id="31131-1583">value</span></span>  
<span data-ttu-id="31131-1584">幅をピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="31131-1584">An integer value that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="31131-1585">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1585">Return Value - widthValue</span></span>

<span data-ttu-id="31131-1586">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="31131-1586">The width of the control in pixels.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="31131-1587">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1587">Remarks - widthValue</span></span>

<span data-ttu-id="31131-1588">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="31131-1588">To change the width of the control, use the Exact width calculation mode.</span></span>

### <a name="examples---widthvalue"></a><span data-ttu-id="31131-1589">例 - widthValue</span><span class="sxs-lookup"><span data-stu-id="31131-1589">Examples - widthValue</span></span>

<span data-ttu-id="31131-1590">次の例は、フォーム コンボ ボックス コントロールの幅の値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1590">The following example shows how to return and set the width value of a form combo box control.</span></span>

```xpp
int nWidthValue; 
// The ctrl variable was previously assigned 
// as a form combo box control variable. 
// Retrieve the width value. 
nWidthValue = ctrl.widthValue(); 
// Set the width value. 
ctrl.widthMode(-1); 
ctrl.widthValue(160);
```

## <a name="method-filter"></a><span data-ttu-id="31131-1591">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="31131-1591">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="31131-1592">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="31131-1592">Parameters - filter</span></span>

<span data-ttu-id="31131-1593">filterStr</span><span class="sxs-lookup"><span data-stu-id="31131-1593">filterStr</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="31131-1594">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="31131-1594">Method displayControl</span></span>

<span data-ttu-id="31131-1595">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1595">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onvalidated"></a><span data-ttu-id="31131-1596">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="31131-1596">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="31131-1597">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="31131-1597">Parameters - OnValidated</span></span>

<span data-ttu-id="31131-1598">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1598">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1599">e</span><span class="sxs-lookup"><span data-stu-id="31131-1599">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="31131-1600">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="31131-1600">Method dragLeave</span></span>

<span data-ttu-id="31131-1601">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-1601">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="31131-1602">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="31131-1602">Method resetUserSetting</span></span>

<span data-ttu-id="31131-1603">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="31131-1603">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-onmodified"></a><span data-ttu-id="31131-1604">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="31131-1604">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="31131-1605">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="31131-1605">Parameters - OnModified</span></span>

<span data-ttu-id="31131-1606">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1606">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1607">e</span><span class="sxs-lookup"><span data-stu-id="31131-1607">e</span></span>  

## <a name="method-context"></a><span data-ttu-id="31131-1608">メソッド context</span><span class="sxs-lookup"><span data-stu-id="31131-1608">Method context</span></span>

<span data-ttu-id="31131-1609">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1609">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-beginupdate"></a><span data-ttu-id="31131-1610">メソッド beginUpdate</span><span class="sxs-lookup"><span data-stu-id="31131-1610">Method beginUpdate</span></span>

```xpp
public void beginUpdate()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="31131-1611">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="31131-1611">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="31131-1612">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="31131-1612">Parameters - OnGotFocus</span></span>

<span data-ttu-id="31131-1613">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1613">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1614">e</span><span class="sxs-lookup"><span data-stu-id="31131-1614">e</span></span>  

## <a name="method-setedittext"></a><span data-ttu-id="31131-1615">メソッド setEditText</span><span class="sxs-lookup"><span data-stu-id="31131-1615">Method setEditText</span></span>

```xpp
public void setEditText(str string)
```

### <a name="parameters---setedittext"></a><span data-ttu-id="31131-1616">パラメーター - setEditText</span><span class="sxs-lookup"><span data-stu-id="31131-1616">Parameters - setEditText</span></span>

<span data-ttu-id="31131-1617">文字列</span><span class="sxs-lookup"><span data-stu-id="31131-1617">string</span></span>  

## <a name="method-enter"></a><span data-ttu-id="31131-1618">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="31131-1618">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-inputsearch"></a><span data-ttu-id="31131-1619">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="31131-1619">Method inputSearch</span></span>

<span data-ttu-id="31131-1620">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="31131-1620">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="31131-1621">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="31131-1621">Parameters - inputSearch</span></span>

<span data-ttu-id="31131-1622">searchStr</span><span class="sxs-lookup"><span data-stu-id="31131-1622">searchStr</span></span>  
<span data-ttu-id="31131-1623">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="31131-1623">The string value to use to filter data; optional.</span></span>

## <a name="method-paste"></a><span data-ttu-id="31131-1624">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="31131-1624">Method paste</span></span>

<span data-ttu-id="31131-1625">フォーム コンボ ボックス コントロールをフォームに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="31131-1625">Pastes the form combo box control into the form.</span></span>

```xpp
public void paste()
```

## <a name="method-clear"></a><span data-ttu-id="31131-1626">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="31131-1626">Method clear</span></span>

<span data-ttu-id="31131-1627">コンボ ボックス リストのエントリをクリアします。</span><span class="sxs-lookup"><span data-stu-id="31131-1627">Clears the entries in the combo box list.</span></span>

```xpp
public void clear()
```

### <a name="examples---clear"></a><span data-ttu-id="31131-1628">例 - clear</span><span class="sxs-lookup"><span data-stu-id="31131-1628">Examples - clear</span></span>

<span data-ttu-id="31131-1629">次の例は、コンボ ボックス リスト内のエントリをクリアする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1629">The following example shows how to clear the entries in the combo box list.</span></span>

```xpp
this.clear();
```

## <a name="method-gotfocus"></a><span data-ttu-id="31131-1630">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="31131-1630">Method gotFocus</span></span>

<span data-ttu-id="31131-1631">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1631">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="31131-1632">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="31131-1632">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="31131-1633">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="31131-1633">Parameters - OnLostFocus</span></span>

<span data-ttu-id="31131-1634">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1634">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1635">e</span><span class="sxs-lookup"><span data-stu-id="31131-1635">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="31131-1636">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="31131-1636">Method drop</span></span>

<span data-ttu-id="31131-1637">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-1637">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="31131-1638">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="31131-1638">Parameters - drop</span></span>

<span data-ttu-id="31131-1639">dragSource</span><span class="sxs-lookup"><span data-stu-id="31131-1639">dragSource</span></span>  
<span data-ttu-id="31131-1640">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1640">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-1641">dragMode</span><span class="sxs-lookup"><span data-stu-id="31131-1641">dragMode</span></span>  
<span data-ttu-id="31131-1642">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1642">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-1643">x</span><span class="sxs-lookup"><span data-stu-id="31131-1643">x</span></span>  
<span data-ttu-id="31131-1644">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1644">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-1645">y</span><span class="sxs-lookup"><span data-stu-id="31131-1645">y</span></span>  
<span data-ttu-id="31131-1646">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1646">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-copy"></a><span data-ttu-id="31131-1647">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="31131-1647">Method copy</span></span>

<span data-ttu-id="31131-1648">フォームのコンボ ボックス コントロールをコピーします。</span><span class="sxs-lookup"><span data-stu-id="31131-1648">Copies the form combo box control.</span></span>

```xpp
public void copy()
```

## <a name="method-onselectionchanging"></a><span data-ttu-id="31131-1649">メソッド OnSelectionChanging</span><span class="sxs-lookup"><span data-stu-id="31131-1649">Method OnSelectionChanging</span></span>

```xpp
private void OnSelectionChanging([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanging"></a><span data-ttu-id="31131-1650">パラメーター - OnSelectionChanging</span><span class="sxs-lookup"><span data-stu-id="31131-1650">Parameters - OnSelectionChanging</span></span>

<span data-ttu-id="31131-1651">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1651">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1652">e</span><span class="sxs-lookup"><span data-stu-id="31131-1652">e</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="31131-1653">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="31131-1653">Method endDrag</span></span>

<span data-ttu-id="31131-1654">ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1654">Is called when the user has finished dragging a form combo box control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="31131-1655">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="31131-1655">Remarks - endDrag</span></span>

<span data-ttu-id="31131-1656">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="31131-1656">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="31131-1657">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="31131-1657">To drag the control, the user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="examples---enddrag"></a><span data-ttu-id="31131-1658">例 - endDrag</span><span class="sxs-lookup"><span data-stu-id="31131-1658">Examples - endDrag</span></span>

<span data-ttu-id="31131-1659">次の例では、ユーザーがフォーム コンボ ボックス コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1659">The following example displays a message in the Infolog when the user has finished dragging the form combo box control.</span></span>

```xpp
public void endDrag() 
{ 
    info("EndDrag completed"); 
    super(); 
}
```

## <a name="method-lookup"></a><span data-ttu-id="31131-1660">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="31131-1660">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-setfocus"></a><span data-ttu-id="31131-1661">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="31131-1661">Method setFocus</span></span>

<span data-ttu-id="31131-1662">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1662">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-insert"></a><span data-ttu-id="31131-1663">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="31131-1663">Method insert</span></span>

<span data-ttu-id="31131-1664">指定した位置にあるコンボ ボックスに文字列の値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="31131-1664">Inserts a string value into the combo box list at the specified position.</span></span>

```xpp
public void insert(str string, int index)
```

### <a name="parameters---insert"></a><span data-ttu-id="31131-1665">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="31131-1665">Parameters - insert</span></span>

<span data-ttu-id="31131-1666">文字列</span><span class="sxs-lookup"><span data-stu-id="31131-1666">string</span></span>  
<span data-ttu-id="31131-1667">後に続く文字列を挿入する位置。</span><span class="sxs-lookup"><span data-stu-id="31131-1667">The position to insert the string after.</span></span> <span data-ttu-id="31131-1668">文字列をリストの最初の項目にする場合は、値を 0 (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1668">If you want the string to be the first item in the list, set the value to 0 (zero).</span></span>

<!-- -->

<span data-ttu-id="31131-1669">指数</span><span class="sxs-lookup"><span data-stu-id="31131-1669">index</span></span>  
<span data-ttu-id="31131-1670">後に続く文字列を挿入する位置。</span><span class="sxs-lookup"><span data-stu-id="31131-1670">The position to insert the string after.</span></span> <span data-ttu-id="31131-1671">文字列をリストの最初の項目にする場合は、値を 0 (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1671">If you want the string to be the first item in the list, set the value to 0 (zero).</span></span>

### <a name="examples---insert"></a><span data-ttu-id="31131-1672">例 - insert</span><span class="sxs-lookup"><span data-stu-id="31131-1672">Examples - insert</span></span>

<span data-ttu-id="31131-1673">次の例は、コンボ ボックス リストに文字列を挿入する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1673">The following example shows how to insert a string into the combo box list.</span></span>

```xpp
this.insert("willow", 3);
```

## <a name="method-mouseenter"></a><span data-ttu-id="31131-1674">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="31131-1674">Method mouseEnter</span></span>

<span data-ttu-id="31131-1675">ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1675">Is called when the user moves the mouse pointer into the control.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="31131-1676">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="31131-1676">Parameters - mouseEnter</span></span>

<span data-ttu-id="31131-1677">x</span><span class="sxs-lookup"><span data-stu-id="31131-1677">x</span></span>  
<span data-ttu-id="31131-1678">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1678">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1679">y</span><span class="sxs-lookup"><span data-stu-id="31131-1679">y</span></span>  
<span data-ttu-id="31131-1680">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1680">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1681">ボタン</span><span class="sxs-lookup"><span data-stu-id="31131-1681">button</span></span>  
<span data-ttu-id="31131-1682">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1682">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1683">Ctrl</span><span class="sxs-lookup"><span data-stu-id="31131-1683">Ctrl</span></span>  
<span data-ttu-id="31131-1684">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1684">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="31131-1685">シフト</span><span class="sxs-lookup"><span data-stu-id="31131-1685">Shift</span></span>  
<span data-ttu-id="31131-1686">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="31131-1686">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="examples---mouseenter"></a><span data-ttu-id="31131-1687">例 - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="31131-1687">Examples - mouseEnter</span></span>

<span data-ttu-id="31131-1688">次の例は、Infolog に mouseEnter イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1688">The following example shows how to display the parameters of a mouseEnter event in the Infolog.</span></span>

```xpp
public void mouseEnter(int x,  
                      int y,  
                      int button, 
                      boolean Ctrl, 
                      boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info("Shift set"); 
    } 
    if (Ctrl) 
    { 
        info("Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
}
```

## <a name="method-onenter"></a><span data-ttu-id="31131-1689">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="31131-1689">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="31131-1690">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="31131-1690">Parameters - OnEnter</span></span>

<span data-ttu-id="31131-1691">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1691">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1692">e</span><span class="sxs-lookup"><span data-stu-id="31131-1692">e</span></span>  

## <a name="method-delete"></a><span data-ttu-id="31131-1693">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="31131-1693">Method delete</span></span>

<span data-ttu-id="31131-1694">コンボ ボックスのリストから文字列値を削除します。</span><span class="sxs-lookup"><span data-stu-id="31131-1694">Removes a string value from the combo box list.</span></span>

```xpp
public void delete(str string)
```

### <a name="parameters---delete"></a><span data-ttu-id="31131-1695">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="31131-1695">Parameters - delete</span></span>

<span data-ttu-id="31131-1696">文字列</span><span class="sxs-lookup"><span data-stu-id="31131-1696">string</span></span>  
<span data-ttu-id="31131-1697">コンボ ボックスのリストから削除する文字列値。</span><span class="sxs-lookup"><span data-stu-id="31131-1697">The string value to remove from the combo box list.</span></span>

### <a name="examples---delete"></a><span data-ttu-id="31131-1698">例 - delete</span><span class="sxs-lookup"><span data-stu-id="31131-1698">Examples - delete</span></span>

<span data-ttu-id="31131-1699">次の例は、コンボ ボックス リストから文字列値を削除する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1699">The following example shows how to remove a string value from the combo box list.</span></span>

```xpp
this.delete("Model 12357");
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="31131-1700">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="31131-1700">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="31131-1701">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="31131-1701">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="31131-1702">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="31131-1702">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="31131-1703">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="31131-1703">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="31131-1704">overrideObject</span><span class="sxs-lookup"><span data-stu-id="31131-1704">overrideObject</span></span>  

## <a name="method-add"></a><span data-ttu-id="31131-1705">メソッド add</span><span class="sxs-lookup"><span data-stu-id="31131-1705">Method add</span></span>

<span data-ttu-id="31131-1706">コンボ ボックス リストに文字列値を追加します。</span><span class="sxs-lookup"><span data-stu-id="31131-1706">Adds a string value to the combo box list.</span></span>

```xpp
public void add(str string)
```

### <a name="parameters---add"></a><span data-ttu-id="31131-1707">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="31131-1707">Parameters - add</span></span>

<span data-ttu-id="31131-1708">文字列</span><span class="sxs-lookup"><span data-stu-id="31131-1708">string</span></span>  
<span data-ttu-id="31131-1709">コンボ ボックスのリストに追加する文字列値。</span><span class="sxs-lookup"><span data-stu-id="31131-1709">The string value to add to the combo box list.</span></span>

### <a name="remarks---add"></a><span data-ttu-id="31131-1710">備考 - add</span><span class="sxs-lookup"><span data-stu-id="31131-1710">Remarks - add</span></span>

<span data-ttu-id="31131-1711">文字列はリストの末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="31131-1711">The string is added to the end of the list.</span></span> <span data-ttu-id="31131-1712">文字列を一覧の特定の位置に格納するには、insert メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="31131-1712">If you want to put the string in a specific position in the list, use the insert method.</span></span>

### <a name="examples---add"></a><span data-ttu-id="31131-1713">例 - add</span><span class="sxs-lookup"><span data-stu-id="31131-1713">Examples - add</span></span>

<span data-ttu-id="31131-1714">次の例は、コンボ ボックス リストに文字列を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1714">The following example shows how to add a string to the combo box list.</span></span>

```xpp
this.add("maple"); 
this.add("oak"); 
this.add("pine");
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="31131-1715">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="31131-1715">Method prefColumnSize</span></span>

<span data-ttu-id="31131-1716">フォーム コンボ ボックス コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="31131-1716">Specifies the preferred column width and height for the form combo box control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="31131-1717">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="31131-1717">Parameters - prefColumnSize</span></span>

<span data-ttu-id="31131-1718">width</span><span class="sxs-lookup"><span data-stu-id="31131-1718">width</span></span>  
<span data-ttu-id="31131-1719">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="31131-1719">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="31131-1720">height</span><span class="sxs-lookup"><span data-stu-id="31131-1720">height</span></span>  
<span data-ttu-id="31131-1721">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="31131-1721">The preferred height of the control.</span></span>

### <a name="examples---prefcolumnsize"></a><span data-ttu-id="31131-1722">例 - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="31131-1722">Examples - prefColumnSize</span></span>

<span data-ttu-id="31131-1723">次の例は、コンボ ボックス コントロールの優先幅と高さを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31131-1723">The following example shows how to set the preferred width and height of a combo box control.</span></span>

```xpp
// The nWidth and nHeight variables were  
// previously assigned as int variables. 
// The ctrl variable was previously assigned 
// as a FormComboBoxControl variable. 
ctrl.prefColumnSize( nWidth, nHeight);
```

## <a name="method-onvalidating"></a><span data-ttu-id="31131-1724">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="31131-1724">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="31131-1725">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="31131-1725">Parameters - OnValidating</span></span>

<span data-ttu-id="31131-1726">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1726">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1727">e</span><span class="sxs-lookup"><span data-stu-id="31131-1727">e</span></span>  

## <a name="method-undo"></a><span data-ttu-id="31131-1728">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="31131-1728">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-jumpref"></a><span data-ttu-id="31131-1729">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="31131-1729">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onselectionchanged"></a><span data-ttu-id="31131-1730">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="31131-1730">Method OnSelectionChanged</span></span>

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a><span data-ttu-id="31131-1731">パラメーター - OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="31131-1731">Parameters - OnSelectionChanged</span></span>

<span data-ttu-id="31131-1732">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1732">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1733">e</span><span class="sxs-lookup"><span data-stu-id="31131-1733">e</span></span>  

## <a name="method-endupdate"></a><span data-ttu-id="31131-1734">メソッド endUpdate</span><span class="sxs-lookup"><span data-stu-id="31131-1734">Method endUpdate</span></span>

```xpp
public void endUpdate()
```

## <a name="method-lostfocus"></a><span data-ttu-id="31131-1735">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="31131-1735">Method lostFocus</span></span>

<span data-ttu-id="31131-1736">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1736">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-mouseleave"></a><span data-ttu-id="31131-1737">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="31131-1737">Method mouseLeave</span></span>

<span data-ttu-id="31131-1738">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="31131-1738">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-onlookup"></a><span data-ttu-id="31131-1739">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="31131-1739">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="31131-1740">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="31131-1740">Parameters - OnLookup</span></span>

<span data-ttu-id="31131-1741">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1741">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1742">e</span><span class="sxs-lookup"><span data-stu-id="31131-1742">e</span></span>  

## <a name="method-cut"></a><span data-ttu-id="31131-1743">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="31131-1743">Method cut</span></span>

<span data-ttu-id="31131-1744">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="31131-1744">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-dropex"></a><span data-ttu-id="31131-1745">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="31131-1745">Method dropEx</span></span>

<span data-ttu-id="31131-1746">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="31131-1746">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="31131-1747">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="31131-1747">Parameters - dropEx</span></span>

<span data-ttu-id="31131-1748">dragSource</span><span class="sxs-lookup"><span data-stu-id="31131-1748">dragSource</span></span>  
<span data-ttu-id="31131-1749">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1749">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-1750">dragMode</span><span class="sxs-lookup"><span data-stu-id="31131-1750">dragMode</span></span>  
<span data-ttu-id="31131-1751">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1751">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-1752">x</span><span class="sxs-lookup"><span data-stu-id="31131-1752">x</span></span>  
<span data-ttu-id="31131-1753">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1753">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="31131-1754">y</span><span class="sxs-lookup"><span data-stu-id="31131-1754">y</span></span>  
<span data-ttu-id="31131-1755">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="31131-1755">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="31131-1756">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="31131-1756">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="31131-1757">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="31131-1757">Parameters - OnLeaving</span></span>

<span data-ttu-id="31131-1758">sender</span><span class="sxs-lookup"><span data-stu-id="31131-1758">sender</span></span>  

<!-- -->

<span data-ttu-id="31131-1759">e</span><span class="sxs-lookup"><span data-stu-id="31131-1759">e</span></span>  

## <a name="method-setdropsize"></a><span data-ttu-id="31131-1760">メソッド setDropSize</span><span class="sxs-lookup"><span data-stu-id="31131-1760">Method setDropSize</span></span>

```xpp
public void setDropSize([int lines])
```

### <a name="parameters---setdropsize"></a><span data-ttu-id="31131-1761">パラメーター - setDropSize</span><span class="sxs-lookup"><span data-stu-id="31131-1761">Parameters - setDropSize</span></span>

<span data-ttu-id="31131-1762">明細行</span><span class="sxs-lookup"><span data-stu-id="31131-1762">lines</span></span>  

