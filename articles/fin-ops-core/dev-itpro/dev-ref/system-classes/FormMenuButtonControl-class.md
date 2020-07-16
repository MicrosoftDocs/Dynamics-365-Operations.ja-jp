---
title: FormMenuButtonControl クラス
description: このトピックでは、FormMenuButtonControl クラスについて説明します。
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
ms.openlocfilehash: bfe827681d06261269cde55144091836bc0f4906
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502933"
---
# <a name="class-formmenubuttoncontrol"></a><span data-ttu-id="54fb0-103">クラス FormMenuButtonControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-103">Class FormMenuButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormMenuButtonControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="54fb0-104">備考</span><span class="sxs-lookup"><span data-stu-id="54fb0-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="54fb0-105">例</span><span class="sxs-lookup"><span data-stu-id="54fb0-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="54fb0-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="54fb0-106">Methods</span></span>

| <span data-ttu-id="54fb0-107">方法</span><span class="sxs-lookup"><span data-stu-id="54fb0-107">Method</span></span>                                                                                                              | <span data-ttu-id="54fb0-108">説明</span><span class="sxs-lookup"><span data-stu-id="54fb0-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fb0-109">public int acquireFocus(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-109">public int acquireFocus(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-110">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-110">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-111">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-111">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-112">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-112">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-113">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-113">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="54fb0-114">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-114">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="54fb0-115">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-115">public int alignment(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="54fb0-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-117">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="54fb0-118">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="54fb0-118">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="54fb0-119">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-119">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="54fb0-120">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-120">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="54fb0-121">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-121">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="54fb0-122">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-122">public boolean autoRefreshData(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-123">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-123">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="54fb0-124">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-124">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="54fb0-125">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-125">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="54fb0-126">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-126">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="54fb0-127">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="54fb0-127">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="54fb0-128">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-128">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="54fb0-129">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-129">public boolean big(\[boolean value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-130">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-130">public int bold(\[int value\])</span></span>                                                                                      | <span data-ttu-id="54fb0-131">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-131">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="54fb0-132">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-132">public int border(\[int value\])</span></span>                                                                                    | <span data-ttu-id="54fb0-133">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-133">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="54fb0-134">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-134">public int bottomMargin(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-135">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-135">public int buttonDisplay(\[int value\])</span></span>                                                                             | <span data-ttu-id="54fb0-136">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-136">Gets or sets the appearance of the button control.</span></span>                                                                                                                      |
| <span data-ttu-id="54fb0-137">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="54fb0-137">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="54fb0-138">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-138">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="54fb0-139">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-139">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-140">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="54fb0-140">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-141">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-141">public int characterSet(\[int value\])</span></span>                                                                              | <span data-ttu-id="54fb0-142">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-142">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="54fb0-143">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-143">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="54fb0-144">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-144">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="54fb0-145">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-145">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="54fb0-146">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-146">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="54fb0-147">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="54fb0-147">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="54fb0-148">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-148">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="54fb0-149">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="54fb0-149">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-150">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="54fb0-150">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-151">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="54fb0-151">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-152">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-152">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="54fb0-153">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-153">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="54fb0-154">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-154">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="54fb0-155">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-155">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="54fb0-156">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-156">public boolean defaultButton(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="54fb0-157">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-157">Determines whether the button should be the default button in the form.</span></span>                                                                                                 |
| <span data-ttu-id="54fb0-158">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-158">public str disabledImage(\[str value\])</span></span>                                                                             | <span data-ttu-id="54fb0-159">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-159">Gets or sets the disabled image of the button.</span></span>                                                                                                                          |
| <span data-ttu-id="54fb0-160">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-160">public int disabledImageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-161">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-161">public int disabledResource(\[int value\])</span></span>                                                                          | <span data-ttu-id="54fb0-162">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-162">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                                          |
| <span data-ttu-id="54fb0-163">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-163">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="54fb0-164">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-164">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="54fb0-165">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-165">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-166">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-166">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="54fb0-167">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="54fb0-167">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="54fb0-168">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-168">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="54fb0-169">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="54fb0-169">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="54fb0-170">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-170">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="54fb0-171">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="54fb0-171">public str dragText()</span></span>                                                                                               | <span data-ttu-id="54fb0-172">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-172">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="54fb0-173">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-173">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="54fb0-174">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-174">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="54fb0-175">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-175">public str font(\[str value\])</span></span>                                                                                      | <span data-ttu-id="54fb0-176">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-176">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="54fb0-177">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-177">public int fontSize(\[int value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-178">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-178">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="54fb0-179">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-179">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-180">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-180">public int foregroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="54fb0-181">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-181">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="54fb0-182">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-182">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="54fb0-183">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-183">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="54fb0-184">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="54fb0-184">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="54fb0-185">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-185">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="54fb0-186">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-186">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="54fb0-187">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-187">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="54fb0-188">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-188">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="54fb0-189">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-189">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="54fb0-190">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-190">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="54fb0-191">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-191">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="54fb0-192">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="54fb0-192">public str helpField()</span></span>                                                                                              | <span data-ttu-id="54fb0-193">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-193">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="54fb0-194">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-194">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-195">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-195">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="54fb0-196">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-196">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="54fb0-197">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-197">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="54fb0-198">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="54fb0-198">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="54fb0-199">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-199">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="54fb0-200">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-200">public int imageLocation(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-201">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="54fb0-201">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-202">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="54fb0-202">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="54fb0-203">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-203">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="54fb0-204">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="54fb0-204">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="54fb0-205">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-205">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="54fb0-206">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="54fb0-206">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="54fb0-207">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-207">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="54fb0-208">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-208">public boolean italic(\[boolean value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-209">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-209">public str keyTip(\[str value\])</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-210">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-210">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="54fb0-211">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-211">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="54fb0-212">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-212">public int leftMargin(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-213">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-213">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-214">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-214">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="54fb0-215">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-215">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="54fb0-216">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-216">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="54fb0-217">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-217">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="54fb0-218">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-218">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="54fb0-219">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="54fb0-219">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="54fb0-220">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-220">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="54fb0-221">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="54fb0-221">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="54fb0-222">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-222">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="54fb0-223">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="54fb0-223">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="54fb0-224">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-224">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="54fb0-225">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="54fb0-225">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="54fb0-226">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-226">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="54fb0-227">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-227">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-228">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-228">public int multiSelect(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-229">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-229">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="54fb0-230">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-230">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="54fb0-231">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-231">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-232">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-232">public int needsRecord(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-233">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-233">public str normalImage(\[str value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-234">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-234">public int normalResource(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-235">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="54fb0-235">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-236">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="54fb0-236">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="54fb0-237">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-237">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="54fb0-238">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-238">public boolean primary(\[boolean value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-239">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-239">public int rightMargin(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-240">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-240">public boolean saveRecord(\[boolean value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="54fb0-242">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-242">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="54fb0-243">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-243">public int shortkey(\[int value\])</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-244">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="54fb0-244">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="54fb0-245">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-245">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="54fb0-246">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-246">public boolean showShortCut(\[boolean value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-247">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-247">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="54fb0-248">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-248">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="54fb0-249">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-249">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-250">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-250">public str text(\[str value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-251">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="54fb0-251">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="54fb0-252">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-252">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="54fb0-253">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-253">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="54fb0-254">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-254">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="54fb0-255">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-255">public int topMargin(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-256">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-256">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="54fb0-257">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-257">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="54fb0-258">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-258">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-259">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-259">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="54fb0-260">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-260">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-261">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-261">public boolean underline(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="54fb0-262">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-262">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="54fb0-263">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="54fb0-263">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-264">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-264">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-265">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-265">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="54fb0-266">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-266">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="54fb0-267">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-267">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="54fb0-268">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-268">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="54fb0-269">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-269">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="54fb0-270">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-270">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="54fb0-271">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-271">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="54fb0-272">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-272">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="54fb0-273">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-273">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="54fb0-274">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-274">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-275">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-275">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="54fb0-276">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-276">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="54fb0-277">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-277">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="54fb0-278">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-278">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="54fb0-279">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-279">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="54fb0-280">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-280">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="54fb0-281">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-281">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="54fb0-282">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-282">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="54fb0-283">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-283">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="54fb0-284">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-284">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="54fb0-285">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-285">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="54fb0-286">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-286">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="54fb0-287">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-287">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="54fb0-288">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-288">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-289">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-289">public boolean value(\[boolean value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-290">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-290">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="54fb0-291">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-291">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="54fb0-292">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-292">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="54fb0-293">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-293">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="54fb0-294">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-294">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="54fb0-295">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-295">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="54fb0-296">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-296">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="54fb0-297">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-297">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="54fb0-298">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-298">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="54fb0-299">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-299">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="54fb0-300">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-300">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="54fb0-301">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-301">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="54fb0-302">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-302">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="54fb0-303">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-303">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="54fb0-304">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="54fb0-304">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="54fb0-305">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-305">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="54fb0-306">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="54fb0-306">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="54fb0-307">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-307">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="54fb0-308">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="54fb0-308">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="54fb0-309">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-309">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="54fb0-310">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="54fb0-310">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="54fb0-311">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-311">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="54fb0-312">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-312">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-313">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-313">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-314">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="54fb0-314">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-315">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="54fb0-315">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="54fb0-316">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-316">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="54fb0-317">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="54fb0-317">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="54fb0-318">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-318">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="54fb0-319">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="54fb0-319">public void clicked()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-320">public void copy()</span><span class="sxs-lookup"><span data-stu-id="54fb0-320">public void copy()</span></span>                                                                                                  | <span data-ttu-id="54fb0-321">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-321">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="54fb0-322">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="54fb0-322">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="54fb0-323">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-323">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="54fb0-324">public void cut()</span><span class="sxs-lookup"><span data-stu-id="54fb0-324">public void cut()</span></span>                                                                                                   | <span data-ttu-id="54fb0-325">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-325">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="54fb0-326">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-326">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-327">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="54fb0-327">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="54fb0-328">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="54fb0-328">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="54fb0-329">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-329">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="54fb0-330">public void context()</span><span class="sxs-lookup"><span data-stu-id="54fb0-330">public void context()</span></span>                                                                                               | <span data-ttu-id="54fb0-331">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-331">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="54fb0-332">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="54fb0-332">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="54fb0-333">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-333">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="54fb0-334">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="54fb0-334">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="54fb0-335">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-335">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="54fb0-336">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="54fb0-336">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="54fb0-337">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-337">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="54fb0-338">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="54fb0-338">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="54fb0-339">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-339">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="54fb0-340">public void paste()</span><span class="sxs-lookup"><span data-stu-id="54fb0-340">public void paste()</span></span>                                                                                                 | <span data-ttu-id="54fb0-341">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-341">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="54fb0-342">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="54fb0-342">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="54fb0-343">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-343">Displays the control.</span></span>                                                                                                                                                   |

## <a name="method-acquirefocus"></a><span data-ttu-id="54fb0-344">メソッド acquireFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-344">Method acquireFocus</span></span>

```xpp
public int acquireFocus([int value])
```

### <a name="parameters---acquirefocus"></a><span data-ttu-id="54fb0-345">パラメーター - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-345">Parameters - acquireFocus</span></span>

<span data-ttu-id="54fb0-346">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-346">value</span></span>  

### <a name="return-value---acquirefocus"></a><span data-ttu-id="54fb0-347">戻り値 - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-347">Return Value - acquireFocus</span></span>

## <a name="method-addcontrol"></a><span data-ttu-id="54fb0-348">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-348">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="54fb0-349">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-349">Parameters - addControl</span></span>

<span data-ttu-id="54fb0-350">controlType</span><span class="sxs-lookup"><span data-stu-id="54fb0-350">controlType</span></span>  

<!-- -->

<span data-ttu-id="54fb0-351">controlName</span><span class="sxs-lookup"><span data-stu-id="54fb0-351">controlName</span></span>  

<!-- -->

<span data-ttu-id="54fb0-352">insertAfter</span><span class="sxs-lookup"><span data-stu-id="54fb0-352">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="54fb0-353">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-353">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="54fb0-354">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-354">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="54fb0-355">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-355">Parameters - addControlEx</span></span>

<span data-ttu-id="54fb0-356">controlClass</span><span class="sxs-lookup"><span data-stu-id="54fb0-356">controlClass</span></span>  

<!-- -->

<span data-ttu-id="54fb0-357">controlName</span><span class="sxs-lookup"><span data-stu-id="54fb0-357">controlName</span></span>  

<!-- -->

<span data-ttu-id="54fb0-358">insertAfter</span><span class="sxs-lookup"><span data-stu-id="54fb0-358">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="54fb0-359">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-359">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="54fb0-360">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="54fb0-360">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="54fb0-361">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="54fb0-361">Parameters - addDataField</span></span>

<span data-ttu-id="54fb0-362">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="54fb0-362">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="54fb0-363">fieldId</span><span class="sxs-lookup"><span data-stu-id="54fb0-363">fieldId</span></span>  

<!-- -->

<span data-ttu-id="54fb0-364">insertAfter</span><span class="sxs-lookup"><span data-stu-id="54fb0-364">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="54fb0-365">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="54fb0-365">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="54fb0-366">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="54fb0-366">Return Value - addDataField</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="54fb0-367">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-367">Method alignControl</span></span>

<span data-ttu-id="54fb0-368">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-368">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="54fb0-369">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-369">Parameters - alignControl</span></span>

<span data-ttu-id="54fb0-370">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-370">value</span></span>  
<span data-ttu-id="54fb0-371">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-371">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="54fb0-372">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-372">Return Value - alignControl</span></span>

<span data-ttu-id="54fb0-373">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-373">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="54fb0-374">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-374">Remarks - alignControl</span></span>

<span data-ttu-id="54fb0-375">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-375">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="54fb0-376">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="54fb0-376">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="54fb0-377">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="54fb0-377">Parameters - alignment</span></span>

<span data-ttu-id="54fb0-378">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-378">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="54fb0-379">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="54fb0-379">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="54fb0-380">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="54fb0-380">Method allowEdit</span></span>

<span data-ttu-id="54fb0-381">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-381">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="54fb0-382">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="54fb0-382">Parameters - allowEdit</span></span>

<span data-ttu-id="54fb0-383">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-383">value</span></span>  
<span data-ttu-id="54fb0-384">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-384">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="54fb0-385">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="54fb0-385">Return Value - allowEdit</span></span>

<span data-ttu-id="54fb0-386">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-386">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="54fb0-387">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="54fb0-387">Remarks - allowEdit</span></span>

<span data-ttu-id="54fb0-388">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-388">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="54fb0-389">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="54fb0-389">Method allowSysSetup</span></span>

<span data-ttu-id="54fb0-390">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-390">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="54fb0-391">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="54fb0-391">Return Value - allowSysSetup</span></span>

<span data-ttu-id="54fb0-392">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-392">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="54fb0-393">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="54fb0-393">Method autoDeclaration</span></span>

<span data-ttu-id="54fb0-394">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-394">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="54fb0-395">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="54fb0-395">Parameters - autoDeclaration</span></span>

<span data-ttu-id="54fb0-396">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-396">value</span></span>  
<span data-ttu-id="54fb0-397">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-397">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="54fb0-398">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="54fb0-398">Return Value - autoDeclaration</span></span>

<span data-ttu-id="54fb0-399">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-399">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="54fb0-400">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="54fb0-400">Remarks - autoDeclaration</span></span>

<span data-ttu-id="54fb0-401">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-401">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="54fb0-402">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="54fb0-402">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="54fb0-403">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="54fb0-403">Parameters - autoRefreshData</span></span>

<span data-ttu-id="54fb0-404">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-404">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="54fb0-405">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="54fb0-405">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="54fb0-406">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-406">Method backgroundColor</span></span>

<span data-ttu-id="54fb0-407">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-407">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="54fb0-408">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-408">Parameters - backgroundColor</span></span>

<span data-ttu-id="54fb0-409">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-409">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="54fb0-410">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-410">Return Value - backgroundColor</span></span>

<span data-ttu-id="54fb0-411">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-411">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="54fb0-412">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-412">Remarks - backgroundColor</span></span>

<span data-ttu-id="54fb0-413">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-413">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="54fb0-414">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-414">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="54fb0-415">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-415">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="54fb0-416">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-416">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="54fb0-417">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-417">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="54fb0-418">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-418">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="54fb0-419">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="54fb0-419">Method backStyle</span></span>

<span data-ttu-id="54fb0-420">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-420">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="54fb0-421">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="54fb0-421">Parameters - backStyle</span></span>

<span data-ttu-id="54fb0-422">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-422">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="54fb0-423">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="54fb0-423">Return Value - backStyle</span></span>

<span data-ttu-id="54fb0-424">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-424">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="54fb0-425">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="54fb0-425">Method beginDrag</span></span>

<span data-ttu-id="54fb0-426">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-426">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="54fb0-427">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="54fb0-427">Parameters - beginDrag</span></span>

<span data-ttu-id="54fb0-428">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-428">x</span></span>  
<span data-ttu-id="54fb0-429">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-429">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="54fb0-430">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-430">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="54fb0-431">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-431">y</span></span>  
<span data-ttu-id="54fb0-432">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-432">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="54fb0-433">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-433">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="54fb0-434">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="54fb0-434">Return Value - beginDrag</span></span>

<span data-ttu-id="54fb0-435">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-435">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="54fb0-436">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="54fb0-436">Remarks - beginDrag</span></span>

<span data-ttu-id="54fb0-437">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-437">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="54fb0-438">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-438">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-big"></a><span data-ttu-id="54fb0-439">メソッド big</span><span class="sxs-lookup"><span data-stu-id="54fb0-439">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="54fb0-440">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="54fb0-440">Parameters - big</span></span>

<span data-ttu-id="54fb0-441">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-441">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="54fb0-442">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="54fb0-442">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="54fb0-443">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="54fb0-443">Method bold</span></span>

<span data-ttu-id="54fb0-444">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-444">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="54fb0-445">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="54fb0-445">Parameters - bold</span></span>

<span data-ttu-id="54fb0-446">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-446">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="54fb0-447">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="54fb0-447">Return Value - bold</span></span>

<span data-ttu-id="54fb0-448">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-448">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="54fb0-449">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="54fb0-449">Remarks - bold</span></span>

<span data-ttu-id="54fb0-450">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-450">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="54fb0-451">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-451">0 Use the default font weight.</span></span>
-   <span data-ttu-id="54fb0-452">1 シン。</span><span class="sxs-lookup"><span data-stu-id="54fb0-452">1 Thin.</span></span>
-   <span data-ttu-id="54fb0-453">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="54fb0-453">2 Extra-light.</span></span>
-   <span data-ttu-id="54fb0-454">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="54fb0-454">3 Light.</span></span>
-   <span data-ttu-id="54fb0-455">4 標準。</span><span class="sxs-lookup"><span data-stu-id="54fb0-455">4 Normal.</span></span>
-   <span data-ttu-id="54fb0-456">5 中。</span><span class="sxs-lookup"><span data-stu-id="54fb0-456">5 Medium.</span></span>
-   <span data-ttu-id="54fb0-457">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="54fb0-457">6 Semibold.</span></span>
-   <span data-ttu-id="54fb0-458">7 太字。</span><span class="sxs-lookup"><span data-stu-id="54fb0-458">7 Bold.</span></span>
-   <span data-ttu-id="54fb0-459">8 極太。</span><span class="sxs-lookup"><span data-stu-id="54fb0-459">8 Extra-bold.</span></span>
-   <span data-ttu-id="54fb0-460">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="54fb0-460">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="54fb0-461">メソッド border</span><span class="sxs-lookup"><span data-stu-id="54fb0-461">Method border</span></span>

<span data-ttu-id="54fb0-462">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-462">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="54fb0-463">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="54fb0-463">Parameters - border</span></span>

<span data-ttu-id="54fb0-464">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-464">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="54fb0-465">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="54fb0-465">Return Value - border</span></span>

<span data-ttu-id="54fb0-466">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-466">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="54fb0-467">備考 - border</span><span class="sxs-lookup"><span data-stu-id="54fb0-467">Remarks - border</span></span>

<span data-ttu-id="54fb0-468">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-468">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="54fb0-469">先頭値</span><span class="sxs-lookup"><span data-stu-id="54fb0-469">Value</span></span> | <span data-ttu-id="54fb0-470">説明</span><span class="sxs-lookup"><span data-stu-id="54fb0-470">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="54fb0-471">0</span><span class="sxs-lookup"><span data-stu-id="54fb0-471">0</span></span>     | <span data-ttu-id="54fb0-472">自動</span><span class="sxs-lookup"><span data-stu-id="54fb0-472">Auto</span></span>        |
| <span data-ttu-id="54fb0-473">1</span><span class="sxs-lookup"><span data-stu-id="54fb0-473">1</span></span>     | <span data-ttu-id="54fb0-474">3D</span><span class="sxs-lookup"><span data-stu-id="54fb0-474">3D</span></span>          |
| <span data-ttu-id="54fb0-475">2</span><span class="sxs-lookup"><span data-stu-id="54fb0-475">2</span></span>     | <span data-ttu-id="54fb0-476">1 行</span><span class="sxs-lookup"><span data-stu-id="54fb0-476">Single line</span></span> |
| <span data-ttu-id="54fb0-477">3</span><span class="sxs-lookup"><span data-stu-id="54fb0-477">3</span></span>     | <span data-ttu-id="54fb0-478">集合住宅</span><span class="sxs-lookup"><span data-stu-id="54fb0-478">Flat</span></span>        |
| <span data-ttu-id="54fb0-479">4</span><span class="sxs-lookup"><span data-stu-id="54fb0-479">4</span></span>     | <span data-ttu-id="54fb0-480">None</span><span class="sxs-lookup"><span data-stu-id="54fb0-480">None</span></span>        |

## <a name="method-bottommargin"></a><span data-ttu-id="54fb0-481">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-481">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="54fb0-482">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-482">Parameters - bottomMargin</span></span>

<span data-ttu-id="54fb0-483">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-483">value</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="54fb0-484">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-484">Return Value - bottomMargin</span></span>

## <a name="method-buttondisplay"></a><span data-ttu-id="54fb0-485">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="54fb0-485">Method buttonDisplay</span></span>

<span data-ttu-id="54fb0-486">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-486">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="54fb0-487">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="54fb0-487">Parameters - buttonDisplay</span></span>

<span data-ttu-id="54fb0-488">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-488">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="54fb0-489">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="54fb0-489">Return Value - buttonDisplay</span></span>

<span data-ttu-id="54fb0-490">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-490">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="54fb0-491">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="54fb0-491">Remarks - buttonDisplay</span></span>

<span data-ttu-id="54fb0-492">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-492">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="54fb0-493">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-493">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="54fb0-494">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-494">The integer value that is returned contains the appearance of the button control as follows.</span></span>

| <span data-ttu-id="54fb0-495">先頭値</span><span class="sxs-lookup"><span data-stu-id="54fb0-495">Value</span></span> | <span data-ttu-id="54fb0-496">説明</span><span class="sxs-lookup"><span data-stu-id="54fb0-496">Description</span></span>                                                      |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="54fb0-497">0</span><span class="sxs-lookup"><span data-stu-id="54fb0-497">0</span></span>     | <span data-ttu-id="54fb0-498">テキストのみ</span><span class="sxs-lookup"><span data-stu-id="54fb0-498">Text only</span></span>                                                        |
| <span data-ttu-id="54fb0-499">1</span><span class="sxs-lookup"><span data-stu-id="54fb0-499">1</span></span>     | <span data-ttu-id="54fb0-500">イメージのみ</span><span class="sxs-lookup"><span data-stu-id="54fb0-500">Image Only</span></span>                                                       |
| <span data-ttu-id="54fb0-501">2</span><span class="sxs-lookup"><span data-stu-id="54fb0-501">2</span></span>     | <span data-ttu-id="54fb0-502">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-502">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="54fb0-503">3</span><span class="sxs-lookup"><span data-stu-id="54fb0-503">3</span></span>     | <span data-ttu-id="54fb0-504">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-504">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="54fb0-505">4</span><span class="sxs-lookup"><span data-stu-id="54fb0-505">4</span></span>     | <span data-ttu-id="54fb0-506">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-506">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="54fb0-507">5</span><span class="sxs-lookup"><span data-stu-id="54fb0-507">5</span></span>     | <span data-ttu-id="54fb0-508">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-508">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-calccontrolsize"></a><span data-ttu-id="54fb0-509">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-509">Method calcControlSize</span></span>

<span data-ttu-id="54fb0-510">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-510">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="54fb0-511">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-511">Parameters - calcControlSize</span></span>

<span data-ttu-id="54fb0-512">chars</span><span class="sxs-lookup"><span data-stu-id="54fb0-512">chars</span></span>  
<span data-ttu-id="54fb0-513">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-513">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="54fb0-514">明細行</span><span class="sxs-lookup"><span data-stu-id="54fb0-514">lines</span></span>  
<span data-ttu-id="54fb0-515">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-515">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="54fb0-516">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-516">Return Value - calcControlSize</span></span>

<span data-ttu-id="54fb0-517">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="54fb0-517">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="54fb0-518">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="54fb0-518">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="54fb0-519">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="54fb0-519">Parameters - canAddDataField</span></span>

<span data-ttu-id="54fb0-520">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="54fb0-520">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="54fb0-521">fieldId</span><span class="sxs-lookup"><span data-stu-id="54fb0-521">fieldId</span></span>  

<!-- -->

<span data-ttu-id="54fb0-522">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="54fb0-522">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="54fb0-523">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="54fb0-523">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="54fb0-524">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="54fb0-524">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="54fb0-525">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="54fb0-525">Parameters - canContain</span></span>

<span data-ttu-id="54fb0-526">control</span><span class="sxs-lookup"><span data-stu-id="54fb0-526">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="54fb0-527">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="54fb0-527">Return Value - canContain</span></span>

## <a name="method-characterset"></a><span data-ttu-id="54fb0-528">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="54fb0-528">Method characterSet</span></span>

<span data-ttu-id="54fb0-529">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-529">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="54fb0-530">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="54fb0-530">Parameters - characterSet</span></span>

<span data-ttu-id="54fb0-531">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-531">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="54fb0-532">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="54fb0-532">Return Value - characterSet</span></span>

<span data-ttu-id="54fb0-533">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-533">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="54fb0-534">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="54fb0-534">Remarks - characterSet</span></span>

<span data-ttu-id="54fb0-535">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-535">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="54fb0-536">先頭値</span><span class="sxs-lookup"><span data-stu-id="54fb0-536">Value</span></span> | <span data-ttu-id="54fb0-537">説明</span><span class="sxs-lookup"><span data-stu-id="54fb0-537">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="54fb0-538">0</span><span class="sxs-lookup"><span data-stu-id="54fb0-538">0</span></span>     | <span data-ttu-id="54fb0-539">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-539">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="54fb0-540">1</span><span class="sxs-lookup"><span data-stu-id="54fb0-540">1</span></span>     | <span data-ttu-id="54fb0-541">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-541">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="54fb0-542">2</span><span class="sxs-lookup"><span data-stu-id="54fb0-542">2</span></span>     | <span data-ttu-id="54fb0-543">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-543">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="54fb0-544">77</span><span class="sxs-lookup"><span data-stu-id="54fb0-544">77</span></span>    | <span data-ttu-id="54fb0-545">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-545">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="54fb0-546">128</span><span class="sxs-lookup"><span data-stu-id="54fb0-546">128</span></span>   | <span data-ttu-id="54fb0-547">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-547">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="54fb0-548">129</span><span class="sxs-lookup"><span data-stu-id="54fb0-548">129</span></span>   | <span data-ttu-id="54fb0-549">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-549">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="54fb0-550">134</span><span class="sxs-lookup"><span data-stu-id="54fb0-550">134</span></span>   | <span data-ttu-id="54fb0-551">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-551">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="54fb0-552">136</span><span class="sxs-lookup"><span data-stu-id="54fb0-552">136</span></span>   | <span data-ttu-id="54fb0-553">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-553">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="54fb0-554">161</span><span class="sxs-lookup"><span data-stu-id="54fb0-554">161</span></span>   | <span data-ttu-id="54fb0-555">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-555">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="54fb0-556">162</span><span class="sxs-lookup"><span data-stu-id="54fb0-556">162</span></span>   | <span data-ttu-id="54fb0-557">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-557">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="54fb0-558">163</span><span class="sxs-lookup"><span data-stu-id="54fb0-558">163</span></span>   | <span data-ttu-id="54fb0-559">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-559">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="54fb0-560">186</span><span class="sxs-lookup"><span data-stu-id="54fb0-560">186</span></span>   | <span data-ttu-id="54fb0-561">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-561">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="54fb0-562">204</span><span class="sxs-lookup"><span data-stu-id="54fb0-562">204</span></span>   | <span data-ttu-id="54fb0-563">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-563">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="54fb0-564">238</span><span class="sxs-lookup"><span data-stu-id="54fb0-564">238</span></span>   | <span data-ttu-id="54fb0-565">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-565">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="54fb0-566">255</span><span class="sxs-lookup"><span data-stu-id="54fb0-566">255</span></span>   | <span data-ttu-id="54fb0-567">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-567">OEM\_CHARSET</span></span>         |

<span data-ttu-id="54fb0-568">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-568">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="54fb0-569">金額</span><span class="sxs-lookup"><span data-stu-id="54fb0-569">Value</span></span> | <span data-ttu-id="54fb0-570">説明</span><span class="sxs-lookup"><span data-stu-id="54fb0-570">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="54fb0-571">130</span><span class="sxs-lookup"><span data-stu-id="54fb0-571">130</span></span>   | <span data-ttu-id="54fb0-572">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-572">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="54fb0-573">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-573">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="54fb0-574">先頭値</span><span class="sxs-lookup"><span data-stu-id="54fb0-574">Value</span></span> | <span data-ttu-id="54fb0-575">説明</span><span class="sxs-lookup"><span data-stu-id="54fb0-575">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="54fb0-576">177</span><span class="sxs-lookup"><span data-stu-id="54fb0-576">177</span></span>   | <span data-ttu-id="54fb0-577">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-577">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="54fb0-578">178</span><span class="sxs-lookup"><span data-stu-id="54fb0-578">178</span></span>   | <span data-ttu-id="54fb0-579">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-579">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="54fb0-580">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-580">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="54fb0-581">先頭値</span><span class="sxs-lookup"><span data-stu-id="54fb0-581">Value</span></span> | <span data-ttu-id="54fb0-582">説明</span><span class="sxs-lookup"><span data-stu-id="54fb0-582">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="54fb0-583">222</span><span class="sxs-lookup"><span data-stu-id="54fb0-583">222</span></span>   | <span data-ttu-id="54fb0-584">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="54fb0-584">THAI\_CHARSET</span></span> |

<span data-ttu-id="54fb0-585">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-585">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="54fb0-586">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-586">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="54fb0-587">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54fb0-587">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="54fb0-588">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="54fb0-588">Method colorScheme</span></span>

<span data-ttu-id="54fb0-589">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-589">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="54fb0-590">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="54fb0-590">Parameters - colorScheme</span></span>

<span data-ttu-id="54fb0-591">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-591">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="54fb0-592">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="54fb0-592">Return Value - colorScheme</span></span>

<span data-ttu-id="54fb0-593">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-593">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="54fb0-594">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="54fb0-594">Remarks - colorScheme</span></span>

<span data-ttu-id="54fb0-595">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-595">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="54fb0-596">先頭値</span><span class="sxs-lookup"><span data-stu-id="54fb0-596">Value</span></span> | <span data-ttu-id="54fb0-597">スタイル</span><span class="sxs-lookup"><span data-stu-id="54fb0-597">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="54fb0-598">0</span><span class="sxs-lookup"><span data-stu-id="54fb0-598">0</span></span>     | <span data-ttu-id="54fb0-599">既定</span><span class="sxs-lookup"><span data-stu-id="54fb0-599">Default</span></span>               |
| <span data-ttu-id="54fb0-600">1</span><span class="sxs-lookup"><span data-stu-id="54fb0-600">1</span></span>     | <span data-ttu-id="54fb0-601">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="54fb0-601">The Windows palette</span></span>   |
| <span data-ttu-id="54fb0-602">2</span><span class="sxs-lookup"><span data-stu-id="54fb0-602">2</span></span>     | <span data-ttu-id="54fb0-603">真の配色</span><span class="sxs-lookup"><span data-stu-id="54fb0-603">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="54fb0-604">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="54fb0-604">Method configurationKey</span></span>

<span data-ttu-id="54fb0-605">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-605">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="54fb0-606">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="54fb0-606">Parameters - configurationKey</span></span>

<span data-ttu-id="54fb0-607">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-607">value</span></span>  
<span data-ttu-id="54fb0-608">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-608">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="54fb0-609">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="54fb0-609">Return Value - configurationKey</span></span>

<span data-ttu-id="54fb0-610">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="54fb0-610">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="54fb0-611">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="54fb0-611">Remarks - configurationKey</span></span>

<span data-ttu-id="54fb0-612">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-612">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="54fb0-613">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-613">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="54fb0-614">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-614">Method configurationKeyEx</span></span>

<span data-ttu-id="54fb0-615">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-615">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="54fb0-616">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-616">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="54fb0-617">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="54fb0-617">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="54fb0-618">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-618">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="54fb0-619">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-619">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="54fb0-620">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-620">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="54fb0-621">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-621">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="54fb0-622">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="54fb0-622">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="54fb0-623">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="54fb0-623">Parameters - contains</span></span>

<span data-ttu-id="54fb0-624">control</span><span class="sxs-lookup"><span data-stu-id="54fb0-624">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="54fb0-625">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="54fb0-625">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="54fb0-626">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="54fb0-626">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="54fb0-627">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="54fb0-627">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="54fb0-628">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="54fb0-628">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="54fb0-629">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="54fb0-629">Parameters - controlNum</span></span>

<span data-ttu-id="54fb0-630">controlNo</span><span class="sxs-lookup"><span data-stu-id="54fb0-630">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="54fb0-631">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="54fb0-631">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="54fb0-632">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="54fb0-632">Method countryRegionCodes</span></span>

<span data-ttu-id="54fb0-633">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-633">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="54fb0-634">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="54fb0-634">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="54fb0-635">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-635">value</span></span>  
<span data-ttu-id="54fb0-636">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-636">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="54fb0-637">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="54fb0-637">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="54fb0-638">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="54fb0-638">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="54fb0-639">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="54fb0-639">Method dataRelationPath</span></span>

<span data-ttu-id="54fb0-640">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-640">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="54fb0-641">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="54fb0-641">Parameters - dataRelationPath</span></span>

<span data-ttu-id="54fb0-642">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-642">value</span></span>  
<span data-ttu-id="54fb0-643">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-643">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="54fb0-644">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="54fb0-644">Return Value - dataRelationPath</span></span>

<span data-ttu-id="54fb0-645">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="54fb0-645">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="54fb0-646">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="54fb0-646">Remarks - dataRelationPath</span></span>

<span data-ttu-id="54fb0-647">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-647">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="54fb0-648">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="54fb0-648">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="54fb0-649">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="54fb0-649">Method defaultButton</span></span>

<span data-ttu-id="54fb0-650">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-650">Determines whether the button should be the default button in the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="54fb0-651">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="54fb0-651">Parameters - defaultButton</span></span>

<span data-ttu-id="54fb0-652">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-652">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="54fb0-653">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="54fb0-653">Return Value - defaultButton</span></span>

<span data-ttu-id="54fb0-654">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-654">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="54fb0-655">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="54fb0-655">Method disabledImage</span></span>

<span data-ttu-id="54fb0-656">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-656">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="54fb0-657">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="54fb0-657">Parameters - disabledImage</span></span>

<span data-ttu-id="54fb0-658">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-658">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="54fb0-659">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="54fb0-659">Return Value - disabledImage</span></span>

<span data-ttu-id="54fb0-660">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="54fb0-660">The full name of an image file.</span></span> <span data-ttu-id="54fb0-661">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-661">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="54fb0-662">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="54fb0-662">Remarks - disabledImage</span></span>

<span data-ttu-id="54fb0-663">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-663">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="54fb0-664">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-664">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="54fb0-665">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="54fb0-665">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="54fb0-666">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="54fb0-666">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="54fb0-667">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-667">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="54fb0-668">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="54fb0-668">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="54fb0-669">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="54fb0-669">Method disabledResource</span></span>

<span data-ttu-id="54fb0-670">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-670">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="54fb0-671">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="54fb0-671">Parameters - disabledResource</span></span>

<span data-ttu-id="54fb0-672">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-672">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="54fb0-673">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="54fb0-673">Return Value - disabledResource</span></span>

<span data-ttu-id="54fb0-674">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="54fb0-674">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="54fb0-675">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-675">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="54fb0-676">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="54fb0-676">Method displayTarget</span></span>

<span data-ttu-id="54fb0-677">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-677">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="54fb0-678">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="54fb0-678">Parameters - displayTarget</span></span>

<span data-ttu-id="54fb0-679">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-679">value</span></span>  
<span data-ttu-id="54fb0-680">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-680">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="54fb0-681">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="54fb0-681">Return Value - displayTarget</span></span>

<span data-ttu-id="54fb0-682">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-682">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="54fb0-683">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="54fb0-683">Method dragDrop</span></span>

<span data-ttu-id="54fb0-684">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-684">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="54fb0-685">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="54fb0-685">Parameters - dragDrop</span></span>

<span data-ttu-id="54fb0-686">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-686">value</span></span>  
<span data-ttu-id="54fb0-687">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-687">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="54fb0-688">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="54fb0-688">Return Value - dragDrop</span></span>

<span data-ttu-id="54fb0-689">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-689">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="54fb0-690">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="54fb0-690">Remarks - dragDrop</span></span>

<span data-ttu-id="54fb0-691">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-691">Use the dragLeave, the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="54fb0-692">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="54fb0-692">Method dragOver</span></span>

<span data-ttu-id="54fb0-693">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-693">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="54fb0-694">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="54fb0-694">Parameters - dragOver</span></span>

<span data-ttu-id="54fb0-695">dragSource</span><span class="sxs-lookup"><span data-stu-id="54fb0-695">dragSource</span></span>  
<span data-ttu-id="54fb0-696">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-696">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-697">dragMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-697">dragMode</span></span>  
<span data-ttu-id="54fb0-698">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-698">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-699">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-699">x</span></span>  
<span data-ttu-id="54fb0-700">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-700">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-701">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-701">y</span></span>  
<span data-ttu-id="54fb0-702">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-702">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="54fb0-703">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="54fb0-703">Return Value - dragOver</span></span>

<span data-ttu-id="54fb0-704">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-704">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="54fb0-705">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-705">Method dragOverEx</span></span>

<span data-ttu-id="54fb0-706">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-706">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="54fb0-707">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-707">Parameters - dragOverEx</span></span>

<span data-ttu-id="54fb0-708">dragSource</span><span class="sxs-lookup"><span data-stu-id="54fb0-708">dragSource</span></span>  
<span data-ttu-id="54fb0-709">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-709">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-710">dragMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-710">dragMode</span></span>  
<span data-ttu-id="54fb0-711">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-711">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-712">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-712">x</span></span>  
<span data-ttu-id="54fb0-713">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-713">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-714">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-714">y</span></span>  
<span data-ttu-id="54fb0-715">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-715">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="54fb0-716">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-716">Return Value - dragOverEx</span></span>

<span data-ttu-id="54fb0-717">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-717">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="54fb0-718">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="54fb0-718">Method dragText</span></span>

<span data-ttu-id="54fb0-719">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-719">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="54fb0-720">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="54fb0-720">Return Value - dragText</span></span>

<span data-ttu-id="54fb0-721">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="54fb0-721">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="54fb0-722">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-722">Method enabled</span></span>

<span data-ttu-id="54fb0-723">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-723">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="54fb0-724">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-724">Parameters - enabled</span></span>

<span data-ttu-id="54fb0-725">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-725">value</span></span>  
<span data-ttu-id="54fb0-726">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-726">A Boolean value that indicates whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="54fb0-727">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-727">Return Value - enabled</span></span>

<span data-ttu-id="54fb0-728">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-728">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="54fb0-729">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-729">Remarks - enabled</span></span>

<span data-ttu-id="54fb0-730">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-730">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="54fb0-731">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-731">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="54fb0-732">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-732">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="54fb0-733">メソッド font</span><span class="sxs-lookup"><span data-stu-id="54fb0-733">Method font</span></span>

<span data-ttu-id="54fb0-734">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-734">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="54fb0-735">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="54fb0-735">Parameters - font</span></span>

<span data-ttu-id="54fb0-736">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-736">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="54fb0-737">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="54fb0-737">Return Value - font</span></span>

<span data-ttu-id="54fb0-738">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="54fb0-738">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="54fb0-739">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-739">Method fontSize</span></span>

<span data-ttu-id="54fb0-740">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-740">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="54fb0-741">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-741">Parameters - fontSize</span></span>

<span data-ttu-id="54fb0-742">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-742">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="54fb0-743">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-743">Return Value - fontSize</span></span>

<span data-ttu-id="54fb0-744">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="54fb0-744">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="54fb0-745">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="54fb0-745">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="54fb0-746">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="54fb0-746">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="54fb0-747">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-747">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="54fb0-748">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="54fb0-748">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="54fb0-749">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-749">Method foregroundColor</span></span>

<span data-ttu-id="54fb0-750">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-750">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="54fb0-751">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-751">Parameters - foregroundColor</span></span>

<span data-ttu-id="54fb0-752">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-752">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="54fb0-753">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-753">Return Value - foregroundColor</span></span>

<span data-ttu-id="54fb0-754">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-754">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="54fb0-755">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="54fb0-755">Remarks - foregroundColor</span></span>

<span data-ttu-id="54fb0-756">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-756">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="54fb0-757">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-757">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="54fb0-758">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-758">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="54fb0-759">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="54fb0-759">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="54fb0-760">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-760">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="54fb0-761">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-761">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="54fb0-762">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="54fb0-762">Method hasChanged</span></span>

<span data-ttu-id="54fb0-763">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-763">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="54fb0-764">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="54fb0-764">Parameters - hasChanged</span></span>

<span data-ttu-id="54fb0-765">val</span><span class="sxs-lookup"><span data-stu-id="54fb0-765">val</span></span>  
<span data-ttu-id="54fb0-766">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-766">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="54fb0-767">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="54fb0-767">Return Value - hasChanged</span></span>

<span data-ttu-id="54fb0-768">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-768">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="54fb0-769">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="54fb0-769">Method hasUserSetting</span></span>

<span data-ttu-id="54fb0-770">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-770">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="54fb0-771">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="54fb0-771">Return Value - hasUserSetting</span></span>

<span data-ttu-id="54fb0-772">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-772">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="54fb0-773">メソッド height</span><span class="sxs-lookup"><span data-stu-id="54fb0-773">Method height</span></span>

<span data-ttu-id="54fb0-774">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-774">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="54fb0-775">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="54fb0-775">Parameters - height</span></span>

<span data-ttu-id="54fb0-776">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-776">value</span></span>  
<span data-ttu-id="54fb0-777">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-777">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="54fb0-778">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-778">mode</span></span>  
<span data-ttu-id="54fb0-779">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-779">An Integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="54fb0-780">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="54fb0-780">Return Value - height</span></span>

<span data-ttu-id="54fb0-781">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="54fb0-781">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="54fb0-782">備考 - height</span><span class="sxs-lookup"><span data-stu-id="54fb0-782">Remarks - height</span></span>

<span data-ttu-id="54fb0-783">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-783">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="54fb0-784">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="54fb0-784">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="54fb0-785">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-785">Mode</span></span>            | <span data-ttu-id="54fb0-786">高さの計算</span><span class="sxs-lookup"><span data-stu-id="54fb0-786">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fb0-787">-1 正確</span><span class="sxs-lookup"><span data-stu-id="54fb0-787">-1 Exact</span></span>        | <span data-ttu-id="54fb0-788">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-788">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="54fb0-789">0 自動</span><span class="sxs-lookup"><span data-stu-id="54fb0-789">0 Auto</span></span>          | <span data-ttu-id="54fb0-790">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-790">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="54fb0-791">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="54fb0-791">1 Column height</span></span> | <span data-ttu-id="54fb0-792">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-792">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="54fb0-793">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-793">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="54fb0-794">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-794">Method heightMode</span></span>

<span data-ttu-id="54fb0-795">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-795">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="54fb0-796">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-796">Parameters - heightMode</span></span>

<span data-ttu-id="54fb0-797">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-797">value</span></span>  
<span data-ttu-id="54fb0-798">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-798">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="54fb0-799">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-799">Return Value - heightMode</span></span>

<span data-ttu-id="54fb0-800">計算モード。</span><span class="sxs-lookup"><span data-stu-id="54fb0-800">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="54fb0-801">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-801">Remarks - heightMode</span></span>

<span data-ttu-id="54fb0-802">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="54fb0-802">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="54fb0-803">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-803">Mode</span></span>          | <span data-ttu-id="54fb0-804">高さの計算</span><span class="sxs-lookup"><span data-stu-id="54fb0-804">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fb0-805">正確</span><span class="sxs-lookup"><span data-stu-id="54fb0-805">Exact</span></span>         | <span data-ttu-id="54fb0-806">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-806">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="54fb0-807">自動</span><span class="sxs-lookup"><span data-stu-id="54fb0-807">Auto</span></span>          | <span data-ttu-id="54fb0-808">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-808">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="54fb0-809">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="54fb0-809">Column height</span></span> | <span data-ttu-id="54fb0-810">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-810">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="54fb0-811">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-811">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="54fb0-812">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-812">Method heightValue</span></span>

<span data-ttu-id="54fb0-813">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-813">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="54fb0-814">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-814">Parameters - heightValue</span></span>

<span data-ttu-id="54fb0-815">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-815">value</span></span>  
<span data-ttu-id="54fb0-816">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-816">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="54fb0-817">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-817">Return Value - heightValue</span></span>

<span data-ttu-id="54fb0-818">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="54fb0-818">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="54fb0-819">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-819">Remarks - heightValue</span></span>

<span data-ttu-id="54fb0-820">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-820">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="54fb0-821">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="54fb0-821">Method helpField</span></span>

<span data-ttu-id="54fb0-822">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-822">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="54fb0-823">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="54fb0-823">Return Value - helpField</span></span>

<span data-ttu-id="54fb0-824">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="54fb0-824">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="54fb0-825">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="54fb0-825">Remarks - helpField</span></span>

<span data-ttu-id="54fb0-826">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-826">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="54fb0-827">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-827">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="54fb0-828">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="54fb0-828">Method helpText</span></span>

<span data-ttu-id="54fb0-829">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-829">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="54fb0-830">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="54fb0-830">Parameters - helpText</span></span>

<span data-ttu-id="54fb0-831">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-831">value</span></span>  
<span data-ttu-id="54fb0-832">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-832">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="54fb0-833">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="54fb0-833">Return Value - helpText</span></span>

<span data-ttu-id="54fb0-834">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="54fb0-834">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="54fb0-835">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="54fb0-835">Remarks - helpText</span></span>

<span data-ttu-id="54fb0-836">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-836">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="54fb0-837">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-837">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="54fb0-838">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="54fb0-838">Method hierarchyParent</span></span>

<span data-ttu-id="54fb0-839">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-839">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="54fb0-840">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="54fb0-840">Parameters - hierarchyParent</span></span>

<span data-ttu-id="54fb0-841">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-841">value</span></span>  
<span data-ttu-id="54fb0-842">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-842">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="54fb0-843">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="54fb0-843">Return Value - hierarchyParent</span></span>

<span data-ttu-id="54fb0-844">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-844">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="54fb0-845">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="54fb0-845">Method hWnd</span></span>

<span data-ttu-id="54fb0-846">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-846">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="54fb0-847">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="54fb0-847">Return Value - hWnd</span></span>

<span data-ttu-id="54fb0-848">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="54fb0-848">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="54fb0-849">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="54fb0-849">Remarks - hWnd</span></span>

<span data-ttu-id="54fb0-850">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-850">The handle can be used with the Windows API.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="54fb0-851">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="54fb0-851">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="54fb0-852">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="54fb0-852">Parameters - imageLocation</span></span>

<span data-ttu-id="54fb0-853">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-853">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="54fb0-854">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="54fb0-854">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="54fb0-855">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="54fb0-855">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="54fb0-856">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="54fb0-856">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="54fb0-857">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="54fb0-857">Method isDisplayed</span></span>

<span data-ttu-id="54fb0-858">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-858">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="54fb0-859">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="54fb0-859">Return Value - isDisplayed</span></span>

<span data-ttu-id="54fb0-860">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-860">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="54fb0-861">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="54fb0-861">Remarks - isDisplayed</span></span>

<span data-ttu-id="54fb0-862">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-862">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="54fb0-863">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="54fb0-863">Method isRestricted</span></span>

<span data-ttu-id="54fb0-864">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-864">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="54fb0-865">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="54fb0-865">Return Value - isRestricted</span></span>

<span data-ttu-id="54fb0-866">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-866">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="54fb0-867">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-867">Method isUserSetupEnabled</span></span>

<span data-ttu-id="54fb0-868">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-868">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="54fb0-869">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-869">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="54fb0-870">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="54fb0-870">neededSetupRights</span></span>  
<span data-ttu-id="54fb0-871">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-871">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="54fb0-872">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-872">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="54fb0-873">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-873">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="54fb0-874">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-874">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="54fb0-875">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="54fb0-875">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="54fb0-876">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-876">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fb0-877">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="54fb0-877">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="54fb0-878">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-878">No changes can be made to the control.</span></span> <span data-ttu-id="54fb0-879">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-879">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="54fb0-880">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="54fb0-880">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="54fb0-881">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-881">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="54fb0-882">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-882">The user cannot move the control.</span></span>   |
| <span data-ttu-id="54fb0-883">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="54fb0-883">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="54fb0-884">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-884">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="54fb0-885">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-885">The user can also move the control.</span></span> |

<span data-ttu-id="54fb0-886">クリックされたメソッドが上書きされる場合、ユーザーは制限されているカスタマイズのみに限定されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-886">If the clicked method is overridden, the user is limited to only restricted customization.</span></span>

## <a name="method-italic"></a><span data-ttu-id="54fb0-887">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="54fb0-887">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="54fb0-888">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="54fb0-888">Parameters - italic</span></span>

<span data-ttu-id="54fb0-889">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-889">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="54fb0-890">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="54fb0-890">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="54fb0-891">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="54fb0-891">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="54fb0-892">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="54fb0-892">Parameters - keyTip</span></span>

<span data-ttu-id="54fb0-893">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-893">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="54fb0-894">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="54fb0-894">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="54fb0-895">メソッド left</span><span class="sxs-lookup"><span data-stu-id="54fb0-895">Method left</span></span>

<span data-ttu-id="54fb0-896">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-896">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="54fb0-897">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="54fb0-897">Parameters - left</span></span>

<span data-ttu-id="54fb0-898">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-898">value</span></span>  
<span data-ttu-id="54fb0-899">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-899">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="54fb0-900">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-900">mode</span></span>  
<span data-ttu-id="54fb0-901">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-901">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="54fb0-902">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="54fb0-902">Return Value - left</span></span>

<span data-ttu-id="54fb0-903">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="54fb0-903">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="54fb0-904">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-904">Method leftMargin</span></span>

```xpp
public int leftMargin([int value])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="54fb0-905">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-905">Parameters - leftMargin</span></span>

<span data-ttu-id="54fb0-906">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-906">value</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="54fb0-907">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-907">Return Value - leftMargin</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="54fb0-908">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-908">Method leftMode</span></span>

<span data-ttu-id="54fb0-909">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-909">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="54fb0-910">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-910">Parameters - leftMode</span></span>

<span data-ttu-id="54fb0-911">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-911">value</span></span>  
<span data-ttu-id="54fb0-912">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-912">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="54fb0-913">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-913">Return Value - leftMode</span></span>

<span data-ttu-id="54fb0-914">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="54fb0-914">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="54fb0-915">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-915">Method leftValue</span></span>

<span data-ttu-id="54fb0-916">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-916">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="54fb0-917">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-917">Parameters - leftValue</span></span>

<span data-ttu-id="54fb0-918">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-918">value</span></span>  
<span data-ttu-id="54fb0-919">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-919">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="54fb0-920">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-920">Return Value - leftValue</span></span>

<span data-ttu-id="54fb0-921">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="54fb0-921">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="54fb0-922">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="54fb0-922">Method markAsUserAdd</span></span>

<span data-ttu-id="54fb0-923">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-923">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="54fb0-924">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="54fb0-924">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="54fb0-925">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-925">value</span></span>  
<span data-ttu-id="54fb0-926">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-926">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="54fb0-927">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="54fb0-927">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="54fb0-928">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-928">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="54fb0-929">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="54fb0-929">Method mouseDblClick</span></span>

<span data-ttu-id="54fb0-930">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-930">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="54fb0-931">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="54fb0-931">Parameters - mouseDblClick</span></span>

<span data-ttu-id="54fb0-932">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-932">x</span></span>  
<span data-ttu-id="54fb0-933">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-933">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-934">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-934">y</span></span>  
<span data-ttu-id="54fb0-935">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-935">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-936">ボタン</span><span class="sxs-lookup"><span data-stu-id="54fb0-936">button</span></span>  
<span data-ttu-id="54fb0-937">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-937">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-938">Ctrl</span><span class="sxs-lookup"><span data-stu-id="54fb0-938">Ctrl</span></span>  
<span data-ttu-id="54fb0-939">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-939">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-940">シフト</span><span class="sxs-lookup"><span data-stu-id="54fb0-940">Shift</span></span>  
<span data-ttu-id="54fb0-941">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-941">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="54fb0-942">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="54fb0-942">Return Value - mouseDblClick</span></span>

<span data-ttu-id="54fb0-943">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-943">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="54fb0-944">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="54fb0-944">Remarks - mouseDblClick</span></span>

<span data-ttu-id="54fb0-945">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-945">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="54fb0-946">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="54fb0-946">Method mouseDown</span></span>

<span data-ttu-id="54fb0-947">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-947">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="54fb0-948">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="54fb0-948">Parameters - mouseDown</span></span>

<span data-ttu-id="54fb0-949">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-949">x</span></span>  
<span data-ttu-id="54fb0-950">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-950">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-951">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-951">y</span></span>  
<span data-ttu-id="54fb0-952">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-952">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-953">ボタン</span><span class="sxs-lookup"><span data-stu-id="54fb0-953">button</span></span>  
<span data-ttu-id="54fb0-954">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-954">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-955">Ctrl</span><span class="sxs-lookup"><span data-stu-id="54fb0-955">Ctrl</span></span>  
<span data-ttu-id="54fb0-956">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-956">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-957">シフト</span><span class="sxs-lookup"><span data-stu-id="54fb0-957">Shift</span></span>  
<span data-ttu-id="54fb0-958">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-958">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="54fb0-959">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="54fb0-959">Return Value - mouseDown</span></span>

<span data-ttu-id="54fb0-960">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-960">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="54fb0-961">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="54fb0-961">Remarks - mouseDown</span></span>

<span data-ttu-id="54fb0-962">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-962">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="54fb0-963">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-963">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="54fb0-964">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="54fb0-964">Method mouseMove</span></span>

<span data-ttu-id="54fb0-965">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-965">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="54fb0-966">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="54fb0-966">Parameters - mouseMove</span></span>

<span data-ttu-id="54fb0-967">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-967">x</span></span>  
<span data-ttu-id="54fb0-968">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-968">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-969">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-969">y</span></span>  
<span data-ttu-id="54fb0-970">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-970">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-971">ボタン</span><span class="sxs-lookup"><span data-stu-id="54fb0-971">button</span></span>  
<span data-ttu-id="54fb0-972">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-972">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-973">Ctrl</span><span class="sxs-lookup"><span data-stu-id="54fb0-973">Ctrl</span></span>  
<span data-ttu-id="54fb0-974">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-974">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-975">シフト</span><span class="sxs-lookup"><span data-stu-id="54fb0-975">Shift</span></span>  
<span data-ttu-id="54fb0-976">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-976">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="54fb0-977">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="54fb0-977">Return Value - mouseMove</span></span>

<span data-ttu-id="54fb0-978">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-978">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="54fb0-979">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="54fb0-979">Remarks - mouseMove</span></span>

<span data-ttu-id="54fb0-980">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-980">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="54fb0-981">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="54fb0-981">Method mouseUp</span></span>

<span data-ttu-id="54fb0-982">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-982">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="54fb0-983">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="54fb0-983">Parameters - mouseUp</span></span>

<span data-ttu-id="54fb0-984">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-984">x</span></span>  
<span data-ttu-id="54fb0-985">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-985">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-986">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-986">y</span></span>  
<span data-ttu-id="54fb0-987">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-987">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-988">ボタン</span><span class="sxs-lookup"><span data-stu-id="54fb0-988">button</span></span>  
<span data-ttu-id="54fb0-989">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-989">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-990">Ctrl</span><span class="sxs-lookup"><span data-stu-id="54fb0-990">Ctrl</span></span>  
<span data-ttu-id="54fb0-991">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-991">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-992">シフト</span><span class="sxs-lookup"><span data-stu-id="54fb0-992">Shift</span></span>  
<span data-ttu-id="54fb0-993">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-993">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="54fb0-994">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="54fb0-994">Return Value - mouseUp</span></span>

<span data-ttu-id="54fb0-995">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-995">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="54fb0-996">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="54fb0-996">Remarks - mouseUp</span></span>

<span data-ttu-id="54fb0-997">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-997">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="54fb0-998">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-998">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="54fb0-999">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-999">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="54fb0-1000">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-1000">Parameters - moveControl</span></span>

<span data-ttu-id="54fb0-1001">controlId</span><span class="sxs-lookup"><span data-stu-id="54fb0-1001">controlId</span></span>  

<!-- -->

<span data-ttu-id="54fb0-1002">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="54fb0-1002">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="54fb0-1003">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-1003">Return Value - moveControl</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="54fb0-1004">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="54fb0-1004">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="54fb0-1005">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="54fb0-1005">Parameters - multiSelect</span></span>

<span data-ttu-id="54fb0-1006">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1006">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="54fb0-1007">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="54fb0-1007">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="54fb0-1008">メソッド名</span><span class="sxs-lookup"><span data-stu-id="54fb0-1008">Method name</span></span>

<span data-ttu-id="54fb0-1009">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1009">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="54fb0-1010">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="54fb0-1010">Parameters - name</span></span>

<span data-ttu-id="54fb0-1011">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1011">value</span></span>  
<span data-ttu-id="54fb0-1012">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1012">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="54fb0-1013">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="54fb0-1013">Return Value - name</span></span>

<span data-ttu-id="54fb0-1014">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1014">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="54fb0-1015">備考 - name</span><span class="sxs-lookup"><span data-stu-id="54fb0-1015">Remarks - name</span></span>

<span data-ttu-id="54fb0-1016">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1016">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="54fb0-1017">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1017">It must start with a letter.</span></span>
-   <span data-ttu-id="54fb0-1018">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1018">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="54fb0-1019">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1019">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="54fb0-1020">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1020">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="54fb0-1021">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1021">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="54fb0-1022">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="54fb0-1022">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="54fb0-1023">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="54fb0-1023">Parameters - neededPermission</span></span>

<span data-ttu-id="54fb0-1024">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1024">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="54fb0-1025">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="54fb0-1025">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="54fb0-1026">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="54fb0-1026">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="54fb0-1027">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="54fb0-1027">Parameters - needsRecord</span></span>

<span data-ttu-id="54fb0-1028">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1028">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="54fb0-1029">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="54fb0-1029">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="54fb0-1030">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="54fb0-1030">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="54fb0-1031">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="54fb0-1031">Parameters - normalImage</span></span>

<span data-ttu-id="54fb0-1032">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1032">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="54fb0-1033">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="54fb0-1033">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="54fb0-1034">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="54fb0-1034">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="54fb0-1035">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="54fb0-1035">Parameters - normalResource</span></span>

<span data-ttu-id="54fb0-1036">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1036">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="54fb0-1037">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="54fb0-1037">Return Value - normalResource</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="54fb0-1038">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="54fb0-1038">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="54fb0-1039">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="54fb0-1039">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="54fb0-1040">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-1040">Method parentControl</span></span>

<span data-ttu-id="54fb0-1041">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1041">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="54fb0-1042">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-1042">Return Value - parentControl</span></span>

<span data-ttu-id="54fb0-1043">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1043">The parent control for the control.</span></span>

## <a name="method-primary"></a><span data-ttu-id="54fb0-1044">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="54fb0-1044">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="54fb0-1045">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="54fb0-1045">Parameters - primary</span></span>

<span data-ttu-id="54fb0-1046">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1046">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="54fb0-1047">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="54fb0-1047">Return Value - primary</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="54fb0-1048">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-1048">Method rightMargin</span></span>

```xpp
public int rightMargin([int value])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="54fb0-1049">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-1049">Parameters - rightMargin</span></span>

<span data-ttu-id="54fb0-1050">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1050">value</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="54fb0-1051">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-1051">Return Value - rightMargin</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="54fb0-1052">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="54fb0-1052">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="54fb0-1053">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="54fb0-1053">Parameters - saveRecord</span></span>

<span data-ttu-id="54fb0-1054">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1054">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="54fb0-1055">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="54fb0-1055">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="54fb0-1056">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="54fb0-1056">Method securityKey</span></span>

<span data-ttu-id="54fb0-1057">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1057">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="54fb0-1058">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="54fb0-1058">Parameters - securityKey</span></span>

<span data-ttu-id="54fb0-1059">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1059">value</span></span>  
<span data-ttu-id="54fb0-1060">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1060">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="54fb0-1061">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="54fb0-1061">Return Value - securityKey</span></span>

<span data-ttu-id="54fb0-1062">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1062">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="54fb0-1063">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="54fb0-1063">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="54fb0-1064">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="54fb0-1064">Parameters - shortkey</span></span>

<span data-ttu-id="54fb0-1065">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1065">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="54fb0-1066">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="54fb0-1066">Return Value - shortkey</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="54fb0-1067">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="54fb0-1067">Method showContextMenu</span></span>

<span data-ttu-id="54fb0-1068">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1068">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="54fb0-1069">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="54fb0-1069">Parameters - showContextMenu</span></span>

<span data-ttu-id="54fb0-1070">menuHandle</span><span class="sxs-lookup"><span data-stu-id="54fb0-1070">menuHandle</span></span>  
<span data-ttu-id="54fb0-1071">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1071">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="54fb0-1072">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="54fb0-1072">Return Value - showContextMenu</span></span>

<span data-ttu-id="54fb0-1073">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1073">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="54fb0-1074">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="54fb0-1074">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="54fb0-1075">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="54fb0-1075">Parameters - showShortCut</span></span>

<span data-ttu-id="54fb0-1076">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1076">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="54fb0-1077">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="54fb0-1077">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="54fb0-1078">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1078">Method skip</span></span>

<span data-ttu-id="54fb0-1079">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1079">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="54fb0-1080">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1080">Parameters - skip</span></span>

<span data-ttu-id="54fb0-1081">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1081">value</span></span>  
<span data-ttu-id="54fb0-1082">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1082">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="54fb0-1083">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1083">Return Value - skip</span></span>

<span data-ttu-id="54fb0-1084">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1084">true if the control is skipped when the user presses the TAB key to move to the control; otherwise false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="54fb0-1085">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1085">Remarks - skip</span></span>

<span data-ttu-id="54fb0-1086">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1086">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-style"></a><span data-ttu-id="54fb0-1087">メソッド style</span><span class="sxs-lookup"><span data-stu-id="54fb0-1087">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="54fb0-1088">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="54fb0-1088">Parameters - style</span></span>

<span data-ttu-id="54fb0-1089">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1089">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="54fb0-1090">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="54fb0-1090">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="54fb0-1091">メソッド text</span><span class="sxs-lookup"><span data-stu-id="54fb0-1091">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="54fb0-1092">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="54fb0-1092">Parameters - text</span></span>

<span data-ttu-id="54fb0-1093">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1093">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="54fb0-1094">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="54fb0-1094">Return Value - text</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="54fb0-1095">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1095">Method toolTip</span></span>

<span data-ttu-id="54fb0-1096">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1096">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="54fb0-1097">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1097">Return Value - toolTip</span></span>

<span data-ttu-id="54fb0-1098">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1098">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="54fb0-1099">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1099">Remarks - toolTip</span></span>

<span data-ttu-id="54fb0-1100">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1100">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="54fb0-1101">メソッド top</span><span class="sxs-lookup"><span data-stu-id="54fb0-1101">Method top</span></span>

<span data-ttu-id="54fb0-1102">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1102">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="54fb0-1103">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="54fb0-1103">Parameters - top</span></span>

<span data-ttu-id="54fb0-1104">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1104">value</span></span>  
<span data-ttu-id="54fb0-1105">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1105">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1106">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-1106">mode</span></span>  
<span data-ttu-id="54fb0-1107">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1107">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="54fb0-1108">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="54fb0-1108">Return Value - top</span></span>

<span data-ttu-id="54fb0-1109">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1109">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="54fb0-1110">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-1110">Method topMargin</span></span>

```xpp
public int topMargin([int value])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="54fb0-1111">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-1111">Parameters - topMargin</span></span>

<span data-ttu-id="54fb0-1112">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1112">value</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="54fb0-1113">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="54fb0-1113">Return Value - topMargin</span></span>

## <a name="method-topmode"></a><span data-ttu-id="54fb0-1114">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1114">Method topMode</span></span>

<span data-ttu-id="54fb0-1115">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1115">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="54fb0-1116">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1116">Parameters - topMode</span></span>

<span data-ttu-id="54fb0-1117">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1117">value</span></span>  
<span data-ttu-id="54fb0-1118">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1118">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="54fb0-1119">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1119">Return Value - topMode</span></span>

<span data-ttu-id="54fb0-1120">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1120">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="54fb0-1121">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1121">Method topValue</span></span>

<span data-ttu-id="54fb0-1122">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1122">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="54fb0-1123">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1123">Parameters - topValue</span></span>

<span data-ttu-id="54fb0-1124">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1124">value</span></span>  
<span data-ttu-id="54fb0-1125">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1125">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="54fb0-1126">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1126">Return Value - topValue</span></span>

<span data-ttu-id="54fb0-1127">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1127">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="54fb0-1128">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="54fb0-1128">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="54fb0-1129">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="54fb0-1129">Parameters - type</span></span>

<span data-ttu-id="54fb0-1130">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1130">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="54fb0-1131">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="54fb0-1131">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="54fb0-1132">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="54fb0-1132">Method underline</span></span>

<span data-ttu-id="54fb0-1133">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1133">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="54fb0-1134">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="54fb0-1134">Parameters - underline</span></span>

<span data-ttu-id="54fb0-1135">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1135">value</span></span>  
<span data-ttu-id="54fb0-1136">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1136">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="54fb0-1137">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="54fb0-1137">Return Value - underline</span></span>

<span data-ttu-id="54fb0-1138">コントロール内のテキストが下線付きである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1138">true if the text in the control is underlined; otherwise false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="54fb0-1139">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="54fb0-1139">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="54fb0-1140">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="54fb0-1140">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="54fb0-1141">データ</span><span class="sxs-lookup"><span data-stu-id="54fb0-1141">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="54fb0-1142">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="54fb0-1142">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="54fb0-1143">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="54fb0-1143">Method userData</span></span>

<span data-ttu-id="54fb0-1144">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1144">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="54fb0-1145">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="54fb0-1145">Parameters - userData</span></span>

<span data-ttu-id="54fb0-1146">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1146">value</span></span>  
<span data-ttu-id="54fb0-1147">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1147">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="54fb0-1148">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="54fb0-1148">Return Value - userData</span></span>

<span data-ttu-id="54fb0-1149">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1149">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="54fb0-1150">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="54fb0-1150">Method userDataItem</span></span>

<span data-ttu-id="54fb0-1151">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1151">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="54fb0-1152">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="54fb0-1152">Parameters - userDataItem</span></span>

<span data-ttu-id="54fb0-1153">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1153">value</span></span>  
<span data-ttu-id="54fb0-1154">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1154">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="54fb0-1155">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="54fb0-1155">Return Value - userDataItem</span></span>

<span data-ttu-id="54fb0-1156">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1156">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="54fb0-1157">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="54fb0-1157">Method userDataItems</span></span>

<span data-ttu-id="54fb0-1158">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1158">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="54fb0-1159">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="54fb0-1159">Parameters - userDataItems</span></span>

<span data-ttu-id="54fb0-1160">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1160">value</span></span>  
<span data-ttu-id="54fb0-1161">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1161">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="54fb0-1162">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="54fb0-1162">Return Value - userDataItems</span></span>

<span data-ttu-id="54fb0-1163">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1163">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="54fb0-1164">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="54fb0-1164">Method userDisable</span></span>

<span data-ttu-id="54fb0-1165">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1165">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="54fb0-1166">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="54fb0-1166">Parameters - userDisable</span></span>

<span data-ttu-id="54fb0-1167">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1167">value</span></span>  
<span data-ttu-id="54fb0-1168">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1168">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="54fb0-1169">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="54fb0-1169">Return Value - userDisable</span></span>

<span data-ttu-id="54fb0-1170">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1170">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="54fb0-1171">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="54fb0-1171">Method userHeight</span></span>

<span data-ttu-id="54fb0-1172">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1172">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="54fb0-1173">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="54fb0-1173">Parameters - userHeight</span></span>

<span data-ttu-id="54fb0-1174">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1174">value</span></span>  
<span data-ttu-id="54fb0-1175">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1175">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="54fb0-1176">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="54fb0-1176">Return Value - userHeight</span></span>

<span data-ttu-id="54fb0-1177">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1177">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="54fb0-1178">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="54fb0-1178">Method userHide</span></span>

<span data-ttu-id="54fb0-1179">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1179">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="54fb0-1180">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="54fb0-1180">Parameters - userHide</span></span>

<span data-ttu-id="54fb0-1181">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1181">value</span></span>  
<span data-ttu-id="54fb0-1182">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1182">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="54fb0-1183">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="54fb0-1183">Return Value - userHide</span></span>

<span data-ttu-id="54fb0-1184">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1184">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="54fb0-1185">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="54fb0-1185">Remarks - userHide</span></span>

<span data-ttu-id="54fb0-1186">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1186">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="54fb0-1187">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1187">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="54fb0-1188">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1188">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="54fb0-1189">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="54fb0-1189">Method userOrgContainer</span></span>

<span data-ttu-id="54fb0-1190">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1190">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="54fb0-1191">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="54fb0-1191">Parameters - userOrgContainer</span></span>

<span data-ttu-id="54fb0-1192">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1192">value</span></span>  
<span data-ttu-id="54fb0-1193">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1193">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="54fb0-1194">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="54fb0-1194">Return Value - userOrgContainer</span></span>

<span data-ttu-id="54fb0-1195">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1195">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="54fb0-1196">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="54fb0-1196">Method userOrgSibling</span></span>

<span data-ttu-id="54fb0-1197">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1197">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="54fb0-1198">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="54fb0-1198">Parameters - userOrgSibling</span></span>

<span data-ttu-id="54fb0-1199">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1199">value</span></span>  
<span data-ttu-id="54fb0-1200">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1200">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="54fb0-1201">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="54fb0-1201">Return Value - userOrgSibling</span></span>

<span data-ttu-id="54fb0-1202">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1202">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="54fb0-1203">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="54fb0-1203">Method userPromptText</span></span>

<span data-ttu-id="54fb0-1204">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1204">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="54fb0-1205">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="54fb0-1205">Parameters - userPromptText</span></span>

<span data-ttu-id="54fb0-1206">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1206">value</span></span>  
<span data-ttu-id="54fb0-1207">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1207">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="54fb0-1208">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="54fb0-1208">Return Value - userPromptText</span></span>

<span data-ttu-id="54fb0-1209">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1209">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="54fb0-1210">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="54fb0-1210">Method userSecurityLevel</span></span>

<span data-ttu-id="54fb0-1211">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1211">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="54fb0-1212">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="54fb0-1212">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="54fb0-1213">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1213">value</span></span>  
<span data-ttu-id="54fb0-1214">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1214">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="54fb0-1215">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="54fb0-1215">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="54fb0-1216">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1216">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="54fb0-1217">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1217">Method userSkip</span></span>

<span data-ttu-id="54fb0-1218">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1218">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="54fb0-1219">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1219">Parameters - userSkip</span></span>

<span data-ttu-id="54fb0-1220">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1220">value</span></span>  
<span data-ttu-id="54fb0-1221">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1221">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="54fb0-1222">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1222">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="54fb0-1223">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="54fb0-1223">Return Value - userSkip</span></span>

<span data-ttu-id="54fb0-1224">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1224">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="54fb0-1225">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="54fb0-1225">Method userWidth</span></span>

<span data-ttu-id="54fb0-1226">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1226">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="54fb0-1227">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="54fb0-1227">Parameters - userWidth</span></span>

<span data-ttu-id="54fb0-1228">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1228">value</span></span>  
<span data-ttu-id="54fb0-1229">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1229">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="54fb0-1230">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="54fb0-1230">Return Value - userWidth</span></span>

<span data-ttu-id="54fb0-1231">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1231">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="54fb0-1232">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="54fb0-1232">Remarks - userWidth</span></span>

<span data-ttu-id="54fb0-1233">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1233">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="54fb0-1234">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1234">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="54fb0-1235">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1235">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="54fb0-1236">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="54fb0-1236">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="54fb0-1237">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="54fb0-1237">Parameters - useUserLayout</span></span>

<span data-ttu-id="54fb0-1238">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1238">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="54fb0-1239">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="54fb0-1239">Return Value - useUserLayout</span></span>

## <a name="method-value"></a><span data-ttu-id="54fb0-1240">メソッド value</span><span class="sxs-lookup"><span data-stu-id="54fb0-1240">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="54fb0-1241">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="54fb0-1241">Parameters - value</span></span>

<span data-ttu-id="54fb0-1242">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1242">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="54fb0-1243">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="54fb0-1243">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="54fb0-1244">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="54fb0-1244">Method verticalSpacing</span></span>

<span data-ttu-id="54fb0-1245">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1245">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="54fb0-1246">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="54fb0-1246">Parameters - verticalSpacing</span></span>

<span data-ttu-id="54fb0-1247">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1247">value</span></span>  
<span data-ttu-id="54fb0-1248">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1248">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1249">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-1249">mode</span></span>  
<span data-ttu-id="54fb0-1250">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1250">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="54fb0-1251">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="54fb0-1251">Return Value - verticalSpacing</span></span>

<span data-ttu-id="54fb0-1252">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1252">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="54fb0-1253">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1253">Method verticalSpacingMode</span></span>

<span data-ttu-id="54fb0-1254">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1254">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="54fb0-1255">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1255">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="54fb0-1256">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-1256">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="54fb0-1257">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1257">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="54fb0-1258">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1258">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="54fb0-1259">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1259">Method verticalSpacingValue</span></span>

<span data-ttu-id="54fb0-1260">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1260">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="54fb0-1261">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1261">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="54fb0-1262">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1262">value</span></span>  
<span data-ttu-id="54fb0-1263">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1263">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="54fb0-1264">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1264">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="54fb0-1265">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1265">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="54fb0-1266">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="54fb0-1266">Method visible</span></span>

<span data-ttu-id="54fb0-1267">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1267">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="54fb0-1268">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="54fb0-1268">Parameters - visible</span></span>

<span data-ttu-id="54fb0-1269">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1269">value</span></span>  
<span data-ttu-id="54fb0-1270">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1270">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="54fb0-1271">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="54fb0-1271">Return Value - visible</span></span>

<span data-ttu-id="54fb0-1272">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1272">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="54fb0-1273">メソッド width</span><span class="sxs-lookup"><span data-stu-id="54fb0-1273">Method width</span></span>

<span data-ttu-id="54fb0-1274">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1274">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="54fb0-1275">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="54fb0-1275">Parameters - width</span></span>

<span data-ttu-id="54fb0-1276">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1276">value</span></span>  
<span data-ttu-id="54fb0-1277">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1277">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1278">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-1278">mode</span></span>  
<span data-ttu-id="54fb0-1279">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1279">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="54fb0-1280">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="54fb0-1280">Return Value - width</span></span>

<span data-ttu-id="54fb0-1281">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1281">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="54fb0-1282">備考 - width</span><span class="sxs-lookup"><span data-stu-id="54fb0-1282">Remarks - width</span></span>

<span data-ttu-id="54fb0-1283">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1283">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="54fb0-1284">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="54fb0-1284">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="54fb0-1285">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-1285">Mode</span></span>           | <span data-ttu-id="54fb0-1286">幅計算</span><span class="sxs-lookup"><span data-stu-id="54fb0-1286">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fb0-1287">-1 正確</span><span class="sxs-lookup"><span data-stu-id="54fb0-1287">-1 Exact</span></span>       | <span data-ttu-id="54fb0-1288">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1288">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="54fb0-1289">0 自動</span><span class="sxs-lookup"><span data-stu-id="54fb0-1289">0 Auto</span></span>         | <span data-ttu-id="54fb0-1290">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1290">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="54fb0-1291">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="54fb0-1291">1 Column width</span></span> | <span data-ttu-id="54fb0-1292">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1292">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="54fb0-1293">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1293">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="54fb0-1294">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1294">Method widthMode</span></span>

<span data-ttu-id="54fb0-1295">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1295">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="54fb0-1296">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1296">Parameters - widthMode</span></span>

<span data-ttu-id="54fb0-1297">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1297">value</span></span>  
<span data-ttu-id="54fb0-1298">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1298">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="54fb0-1299">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1299">Return Value - widthMode</span></span>

<span data-ttu-id="54fb0-1300">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1300">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="54fb0-1301">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1301">Remarks - widthMode</span></span>

<span data-ttu-id="54fb0-1302">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="54fb0-1302">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="54fb0-1303">モード</span><span class="sxs-lookup"><span data-stu-id="54fb0-1303">Mode</span></span>         | <span data-ttu-id="54fb0-1304">幅計算</span><span class="sxs-lookup"><span data-stu-id="54fb0-1304">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fb0-1305">正確</span><span class="sxs-lookup"><span data-stu-id="54fb0-1305">Exact</span></span>        | <span data-ttu-id="54fb0-1306">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1306">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="54fb0-1307">自動</span><span class="sxs-lookup"><span data-stu-id="54fb0-1307">Auto</span></span>         | <span data-ttu-id="54fb0-1308">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1308">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="54fb0-1309">列の幅</span><span class="sxs-lookup"><span data-stu-id="54fb0-1309">Column width</span></span> | <span data-ttu-id="54fb0-1310">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1310">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="54fb0-1311">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1311">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="54fb0-1312">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1312">Method widthValue</span></span>

<span data-ttu-id="54fb0-1313">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1313">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="54fb0-1314">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1314">Parameters - widthValue</span></span>

<span data-ttu-id="54fb0-1315">値</span><span class="sxs-lookup"><span data-stu-id="54fb0-1315">value</span></span>  
<span data-ttu-id="54fb0-1316">幅をピクセル単位で指定する整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1316">An integer value that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="54fb0-1317">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1317">Return Value - widthValue</span></span>

<span data-ttu-id="54fb0-1318">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1318">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="54fb0-1319">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="54fb0-1319">Remarks - widthValue</span></span>

<span data-ttu-id="54fb0-1320">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1320">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-drop"></a><span data-ttu-id="54fb0-1321">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="54fb0-1321">Method drop</span></span>

<span data-ttu-id="54fb0-1322">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1322">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="54fb0-1323">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="54fb0-1323">Parameters - drop</span></span>

<span data-ttu-id="54fb0-1324">dragSource</span><span class="sxs-lookup"><span data-stu-id="54fb0-1324">dragSource</span></span>  
<span data-ttu-id="54fb0-1325">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1325">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1326">dragMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1326">dragMode</span></span>  
<span data-ttu-id="54fb0-1327">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1327">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1328">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-1328">x</span></span>  
<span data-ttu-id="54fb0-1329">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1329">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1330">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-1330">y</span></span>  
<span data-ttu-id="54fb0-1331">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1331">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-prefcolumnsize"></a><span data-ttu-id="54fb0-1332">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-1332">Method prefColumnSize</span></span>

<span data-ttu-id="54fb0-1333">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1333">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="54fb0-1334">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="54fb0-1334">Parameters - prefColumnSize</span></span>

<span data-ttu-id="54fb0-1335">width</span><span class="sxs-lookup"><span data-stu-id="54fb0-1335">width</span></span>  
<span data-ttu-id="54fb0-1336">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1336">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1337">height</span><span class="sxs-lookup"><span data-stu-id="54fb0-1337">height</span></span>  
<span data-ttu-id="54fb0-1338">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1338">The preferred height of the control.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="54fb0-1339">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="54fb0-1339">Method resetUserSetting</span></span>

<span data-ttu-id="54fb0-1340">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1340">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-dropex"></a><span data-ttu-id="54fb0-1341">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-1341">Method dropEx</span></span>

<span data-ttu-id="54fb0-1342">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1342">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="54fb0-1343">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="54fb0-1343">Parameters - dropEx</span></span>

<span data-ttu-id="54fb0-1344">dragSource</span><span class="sxs-lookup"><span data-stu-id="54fb0-1344">dragSource</span></span>  
<span data-ttu-id="54fb0-1345">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1345">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1346">dragMode</span><span class="sxs-lookup"><span data-stu-id="54fb0-1346">dragMode</span></span>  
<span data-ttu-id="54fb0-1347">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1347">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1348">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-1348">x</span></span>  
<span data-ttu-id="54fb0-1349">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1349">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1350">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-1350">y</span></span>  
<span data-ttu-id="54fb0-1351">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1351">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-ongotfocus"></a><span data-ttu-id="54fb0-1352">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-1352">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="54fb0-1353">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-1353">Parameters - OnGotFocus</span></span>

<span data-ttu-id="54fb0-1354">sender</span><span class="sxs-lookup"><span data-stu-id="54fb0-1354">sender</span></span>  

<!-- -->

<span data-ttu-id="54fb0-1355">e</span><span class="sxs-lookup"><span data-stu-id="54fb0-1355">e</span></span>  

## <a name="method-registeroverridemethod"></a><span data-ttu-id="54fb0-1356">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="54fb0-1356">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="54fb0-1357">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="54fb0-1357">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="54fb0-1358">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="54fb0-1358">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="54fb0-1359">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="54fb0-1359">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="54fb0-1360">overrideObject</span><span class="sxs-lookup"><span data-stu-id="54fb0-1360">overrideObject</span></span>  

## <a name="method-arrange"></a><span data-ttu-id="54fb0-1361">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="54fb0-1361">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-inputsearch"></a><span data-ttu-id="54fb0-1362">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="54fb0-1362">Method inputSearch</span></span>

<span data-ttu-id="54fb0-1363">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1363">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="54fb0-1364">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="54fb0-1364">Parameters - inputSearch</span></span>

<span data-ttu-id="54fb0-1365">searchStr</span><span class="sxs-lookup"><span data-stu-id="54fb0-1365">searchStr</span></span>  
<span data-ttu-id="54fb0-1366">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1366">The string value to use to filter data; optional.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="54fb0-1367">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-1367">Method gotFocus</span></span>

<span data-ttu-id="54fb0-1368">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1368">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-clicked"></a><span data-ttu-id="54fb0-1369">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="54fb0-1369">Method clicked</span></span>

```xpp
public void clicked()
```

## <a name="method-copy"></a><span data-ttu-id="54fb0-1370">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="54fb0-1370">Method copy</span></span>

<span data-ttu-id="54fb0-1371">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1371">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-setfocus"></a><span data-ttu-id="54fb0-1372">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-1372">Method setFocus</span></span>

<span data-ttu-id="54fb0-1373">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1373">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-cut"></a><span data-ttu-id="54fb0-1374">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="54fb0-1374">Method cut</span></span>

<span data-ttu-id="54fb0-1375">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1375">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-onclicked"></a><span data-ttu-id="54fb0-1376">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="54fb0-1376">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="54fb0-1377">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="54fb0-1377">Parameters - OnClicked</span></span>

<span data-ttu-id="54fb0-1378">sender</span><span class="sxs-lookup"><span data-stu-id="54fb0-1378">sender</span></span>  

<!-- -->

<span data-ttu-id="54fb0-1379">e</span><span class="sxs-lookup"><span data-stu-id="54fb0-1379">e</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="54fb0-1380">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-1380">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="54fb0-1381">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-1381">Parameters - OnLostFocus</span></span>

<span data-ttu-id="54fb0-1382">sender</span><span class="sxs-lookup"><span data-stu-id="54fb0-1382">sender</span></span>  

<!-- -->

<span data-ttu-id="54fb0-1383">e</span><span class="sxs-lookup"><span data-stu-id="54fb0-1383">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="54fb0-1384">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="54fb0-1384">Method dragLeave</span></span>

<span data-ttu-id="54fb0-1385">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1385">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-context"></a><span data-ttu-id="54fb0-1386">メソッド context</span><span class="sxs-lookup"><span data-stu-id="54fb0-1386">Method context</span></span>

<span data-ttu-id="54fb0-1387">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1387">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enddrag"></a><span data-ttu-id="54fb0-1388">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="54fb0-1388">Method endDrag</span></span>

<span data-ttu-id="54fb0-1389">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1389">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="54fb0-1390">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="54fb0-1390">Remarks - endDrag</span></span>

<span data-ttu-id="54fb0-1391">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1391">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="54fb0-1392">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1392">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="54fb0-1393">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="54fb0-1393">Method mouseLeave</span></span>

<span data-ttu-id="54fb0-1394">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1394">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-mouseenter"></a><span data-ttu-id="54fb0-1395">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="54fb0-1395">Method mouseEnter</span></span>

<span data-ttu-id="54fb0-1396">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1396">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="54fb0-1397">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="54fb0-1397">Parameters - mouseEnter</span></span>

<span data-ttu-id="54fb0-1398">x</span><span class="sxs-lookup"><span data-stu-id="54fb0-1398">x</span></span>  
<span data-ttu-id="54fb0-1399">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1399">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1400">y</span><span class="sxs-lookup"><span data-stu-id="54fb0-1400">y</span></span>  
<span data-ttu-id="54fb0-1401">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1401">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1402">ボタン</span><span class="sxs-lookup"><span data-stu-id="54fb0-1402">button</span></span>  
<span data-ttu-id="54fb0-1403">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1403">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1404">Ctrl</span><span class="sxs-lookup"><span data-stu-id="54fb0-1404">Ctrl</span></span>  
<span data-ttu-id="54fb0-1405">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1405">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="54fb0-1406">シフト</span><span class="sxs-lookup"><span data-stu-id="54fb0-1406">Shift</span></span>  
<span data-ttu-id="54fb0-1407">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1407">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="54fb0-1408">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="54fb0-1408">Method lostFocus</span></span>

<span data-ttu-id="54fb0-1409">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1409">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-paste"></a><span data-ttu-id="54fb0-1410">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="54fb0-1410">Method paste</span></span>

<span data-ttu-id="54fb0-1411">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1411">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="54fb0-1412">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="54fb0-1412">Method displayControl</span></span>

<span data-ttu-id="54fb0-1413">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="54fb0-1413">Displays the control.</span></span>

```xpp
public void displayControl()
```

