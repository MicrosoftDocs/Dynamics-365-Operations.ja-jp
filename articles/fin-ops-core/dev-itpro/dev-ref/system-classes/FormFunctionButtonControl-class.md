---
title: FormFunctionButtonControl クラス
description: このトピックでは、FormFunctionButtonControl クラスについて説明します。
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
ms.openlocfilehash: a875c0af9850d5eb9d0f4f7289af4f8d2185e229
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502939"
---
# <a name="class-formfunctionbuttoncontrol"></a><span data-ttu-id="7497a-103">クラス FormFunctionButtonControl</span><span class="sxs-lookup"><span data-stu-id="7497a-103">Class FormFunctionButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormFunctionButtonControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="7497a-104">備考</span><span class="sxs-lookup"><span data-stu-id="7497a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7497a-105">例</span><span class="sxs-lookup"><span data-stu-id="7497a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7497a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="7497a-106">Methods</span></span>

| <span data-ttu-id="7497a-107">方法</span><span class="sxs-lookup"><span data-stu-id="7497a-107">Method</span></span>                                                                                                      | <span data-ttu-id="7497a-108">説明</span><span class="sxs-lookup"><span data-stu-id="7497a-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7497a-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="7497a-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7497a-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7497a-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="7497a-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="7497a-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="7497a-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="7497a-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="7497a-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="7497a-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="7497a-118">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-118">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="7497a-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="7497a-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="7497a-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="7497a-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="7497a-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7497a-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="7497a-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="7497a-125">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-125">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-126">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-126">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="7497a-127">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-127">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="7497a-128">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-128">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="7497a-129">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-129">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="7497a-130">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-130">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="7497a-131">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-131">Gets or sets the appearance of the button control.</span></span>                                                                                                                      |
| <span data-ttu-id="7497a-132">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="7497a-132">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="7497a-133">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-133">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="7497a-134">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-134">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="7497a-135">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-135">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7497a-136">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-136">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="7497a-137">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-137">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="7497a-138">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-138">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="7497a-139">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-139">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7497a-140">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-140">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="7497a-141">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-141">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="7497a-142">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="7497a-142">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="7497a-143">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-143">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="7497a-144">public int copyCallerQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-144">public int copyCallerQuery(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7497a-145">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-145">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="7497a-146">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-146">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="7497a-147">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-147">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7497a-148">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-148">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="7497a-149">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-149">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="7497a-150">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-150">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="7497a-151">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-151">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="7497a-152">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-152">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="7497a-153">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-153">Determines whether the button should be the default button in the form.</span></span>                                                                                                 |
| <span data-ttu-id="7497a-154">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-154">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="7497a-155">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-155">Gets or sets the disabled image of the button.</span></span>                                                                                                                          |
| <span data-ttu-id="7497a-156">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-156">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="7497a-157">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-157">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="7497a-158">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-158">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                                          |
| <span data-ttu-id="7497a-159">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-159">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="7497a-160">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-160">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="7497a-161">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-161">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="7497a-162">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-162">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="7497a-163">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7497a-163">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="7497a-164">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-164">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="7497a-165">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7497a-165">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="7497a-166">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-166">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="7497a-167">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="7497a-167">public str dragText()</span></span>                                                                                       | <span data-ttu-id="7497a-168">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-168">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="7497a-169">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-169">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="7497a-170">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-170">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="7497a-171">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-171">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="7497a-172">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-172">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="7497a-173">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-173">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="7497a-174">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-174">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="7497a-175">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-175">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="7497a-176">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-176">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="7497a-177">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-177">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="7497a-178">public int formViewOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-178">public int formViewOption(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7497a-179">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="7497a-179">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="7497a-180">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-180">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="7497a-181">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="7497a-181">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="7497a-182">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-182">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="7497a-183">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7497a-183">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="7497a-184">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-184">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7497a-185">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-185">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="7497a-186">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-186">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="7497a-187">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-187">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="7497a-188">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-188">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7497a-189">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="7497a-189">public str helpField()</span></span>                                                                                      | <span data-ttu-id="7497a-190">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-190">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7497a-191">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-191">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="7497a-192">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-192">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="7497a-193">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-193">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="7497a-194">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-194">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="7497a-195">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="7497a-195">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="7497a-196">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-196">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7497a-197">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-197">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7497a-198">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="7497a-198">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7497a-199">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="7497a-199">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="7497a-200">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-200">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="7497a-201">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="7497a-201">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="7497a-202">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-202">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="7497a-203">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="7497a-203">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="7497a-204">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-204">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="7497a-205">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-205">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7497a-206">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-206">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7497a-207">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7497a-207">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="7497a-208">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-208">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="7497a-209">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-209">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="7497a-210">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-210">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7497a-211">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-211">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="7497a-212">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-212">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="7497a-213">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-213">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="7497a-214">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="7497a-214">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="7497a-215">public xMenuFunction menufunction()</span><span class="sxs-lookup"><span data-stu-id="7497a-215">public xMenuFunction menufunction()</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7497a-216">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-216">public str menuItemName(\[str value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7497a-217">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-217">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7497a-218">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7497a-218">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="7497a-219">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-219">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="7497a-220">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7497a-220">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="7497a-221">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-221">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="7497a-222">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7497a-222">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="7497a-223">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-223">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="7497a-224">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7497a-224">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="7497a-225">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-225">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="7497a-226">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-226">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-227">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-227">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="7497a-228">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-228">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="7497a-229">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-229">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7497a-230">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-230">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-231">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-231">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-232">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-232">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7497a-233">public int openMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-233">public int openMode(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="7497a-234">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="7497a-234">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7497a-235">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-235">public str parameters(\[str value\])</span></span>                                                                        | <span data-ttu-id="7497a-236">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-236">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                                                  |
| <span data-ttu-id="7497a-237">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="7497a-237">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="7497a-238">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-238">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7497a-239">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-239">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7497a-240">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-240">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7497a-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="7497a-242">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-242">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="7497a-243">public boolean sendExternalContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-243">public boolean sendExternalContext(\[boolean value\])</span></span>                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-244">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-244">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="7497a-245">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="7497a-245">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="7497a-246">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-246">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7497a-247">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-247">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7497a-248">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-248">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="7497a-249">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-249">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="7497a-250">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="7497a-250">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7497a-251">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-251">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="7497a-252">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-252">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7497a-253">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="7497a-253">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="7497a-254">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-254">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="7497a-255">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7497a-255">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="7497a-256">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-256">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="7497a-257">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-257">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="7497a-258">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-258">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="7497a-259">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-259">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="7497a-260">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-260">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="7497a-261">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-261">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7497a-262">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-262">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7497a-263">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="7497a-263">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7497a-264">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-264">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="7497a-265">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-265">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="7497a-266">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-266">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="7497a-267">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-267">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="7497a-268">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-268">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="7497a-269">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-269">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="7497a-270">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-270">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="7497a-271">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-271">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="7497a-272">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-272">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="7497a-273">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-273">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="7497a-274">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-274">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="7497a-275">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-275">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="7497a-276">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-276">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="7497a-277">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-277">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="7497a-278">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-278">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="7497a-279">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-279">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7497a-280">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-280">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="7497a-281">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-281">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="7497a-282">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-282">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="7497a-283">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-283">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="7497a-284">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-284">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="7497a-285">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-285">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="7497a-286">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-286">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="7497a-287">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-287">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="7497a-288">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-288">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7497a-289">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7497a-289">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="7497a-290">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-290">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7497a-291">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7497a-291">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="7497a-292">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-292">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="7497a-293">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-293">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="7497a-294">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-294">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7497a-295">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-295">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="7497a-296">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-296">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="7497a-297">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7497a-297">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="7497a-298">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-298">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="7497a-299">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-299">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="7497a-300">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-300">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="7497a-301">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7497a-301">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="7497a-302">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-302">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="7497a-303">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="7497a-303">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="7497a-304">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-304">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="7497a-305">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="7497a-305">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="7497a-306">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-306">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="7497a-307">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="7497a-307">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="7497a-308">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7497a-308">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="7497a-309">public void context()</span><span class="sxs-lookup"><span data-stu-id="7497a-309">public void context()</span></span>                                                                                       | <span data-ttu-id="7497a-310">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-310">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7497a-311">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7497a-311">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="7497a-312">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-312">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="7497a-313">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7497a-313">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="7497a-314">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="7497a-314">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="7497a-315">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-315">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="7497a-316">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7497a-316">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="7497a-317">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-317">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="7497a-318">public void paste()</span><span class="sxs-lookup"><span data-stu-id="7497a-318">public void paste()</span></span>                                                                                         | <span data-ttu-id="7497a-319">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7497a-319">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7497a-320">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7497a-320">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="7497a-321">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="7497a-321">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="7497a-322">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-322">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="7497a-323">public void cut()</span><span class="sxs-lookup"><span data-stu-id="7497a-323">public void cut()</span></span>                                                                                           | <span data-ttu-id="7497a-324">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="7497a-324">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="7497a-325">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="7497a-325">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-326">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="7497a-326">public void displayControl()</span></span>                                                                                | <span data-ttu-id="7497a-327">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-327">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="7497a-328">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="7497a-328">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="7497a-329">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="7497a-329">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="7497a-330">public void copy()</span><span class="sxs-lookup"><span data-stu-id="7497a-330">public void copy()</span></span>                                                                                          | <span data-ttu-id="7497a-331">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7497a-331">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="7497a-332">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="7497a-332">public void clicked()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-333">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7497a-333">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="7497a-334">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7497a-334">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="7497a-335">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-335">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="7497a-336">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="7497a-336">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="7497a-337">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-337">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7497a-338">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="7497a-338">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="7497a-339">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-339">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="7497a-340">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="7497a-340">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="7497a-341">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-341">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="7497a-342">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="7497a-342">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7497a-343">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="7497a-343">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="7497a-344">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="7497a-344">Method alignControl</span></span>

<span data-ttu-id="7497a-345">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-345">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="7497a-346">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="7497a-346">Parameters - alignControl</span></span>

<span data-ttu-id="7497a-347">値</span><span class="sxs-lookup"><span data-stu-id="7497a-347">value</span></span>  
<span data-ttu-id="7497a-348">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-348">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="7497a-349">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="7497a-349">Return Value - alignControl</span></span>

<span data-ttu-id="7497a-350">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7497a-350">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="7497a-351">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="7497a-351">Remarks - alignControl</span></span>

<span data-ttu-id="7497a-352">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-352">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="7497a-353">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="7497a-353">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="7497a-354">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="7497a-354">Parameters - alignment</span></span>

<span data-ttu-id="7497a-355">値</span><span class="sxs-lookup"><span data-stu-id="7497a-355">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="7497a-356">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="7497a-356">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="7497a-357">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="7497a-357">Method allowEdit</span></span>

<span data-ttu-id="7497a-358">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-358">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="7497a-359">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7497a-359">Parameters - allowEdit</span></span>

<span data-ttu-id="7497a-360">値</span><span class="sxs-lookup"><span data-stu-id="7497a-360">value</span></span>  
<span data-ttu-id="7497a-361">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="7497a-361">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="7497a-362">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7497a-362">Return Value - allowEdit</span></span>

<span data-ttu-id="7497a-363">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-363">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="7497a-364">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7497a-364">Remarks - allowEdit</span></span>

<span data-ttu-id="7497a-365">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="7497a-365">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="7497a-366">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="7497a-366">Method allowSysSetup</span></span>

<span data-ttu-id="7497a-367">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-367">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="7497a-368">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="7497a-368">Return Value - allowSysSetup</span></span>

<span data-ttu-id="7497a-369">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-369">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="7497a-370">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7497a-370">Method autoDeclaration</span></span>

<span data-ttu-id="7497a-371">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-371">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="7497a-372">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7497a-372">Parameters - autoDeclaration</span></span>

<span data-ttu-id="7497a-373">値</span><span class="sxs-lookup"><span data-stu-id="7497a-373">value</span></span>  
<span data-ttu-id="7497a-374">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-374">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="7497a-375">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7497a-375">Return Value - autoDeclaration</span></span>

<span data-ttu-id="7497a-376">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-376">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="7497a-377">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7497a-377">Remarks - autoDeclaration</span></span>

<span data-ttu-id="7497a-378">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="7497a-378">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="7497a-379">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="7497a-379">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="7497a-380">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="7497a-380">Parameters - autoRefreshData</span></span>

<span data-ttu-id="7497a-381">値</span><span class="sxs-lookup"><span data-stu-id="7497a-381">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="7497a-382">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="7497a-382">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="7497a-383">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-383">Method backgroundColor</span></span>

<span data-ttu-id="7497a-384">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-384">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="7497a-385">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-385">Parameters - backgroundColor</span></span>

<span data-ttu-id="7497a-386">値</span><span class="sxs-lookup"><span data-stu-id="7497a-386">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="7497a-387">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-387">Return Value - backgroundColor</span></span>

<span data-ttu-id="7497a-388">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="7497a-388">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="7497a-389">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-389">Remarks - backgroundColor</span></span>

<span data-ttu-id="7497a-390">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7497a-390">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="7497a-391">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7497a-391">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="7497a-392">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7497a-392">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="7497a-393">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7497a-393">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="7497a-394">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7497a-394">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="7497a-395">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="7497a-395">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="7497a-396">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="7497a-396">Method backStyle</span></span>

<span data-ttu-id="7497a-397">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-397">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="7497a-398">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="7497a-398">Parameters - backStyle</span></span>

<span data-ttu-id="7497a-399">値</span><span class="sxs-lookup"><span data-stu-id="7497a-399">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="7497a-400">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="7497a-400">Return Value - backStyle</span></span>

<span data-ttu-id="7497a-401">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7497a-401">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="7497a-402">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="7497a-402">Method beginDrag</span></span>

<span data-ttu-id="7497a-403">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-403">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="7497a-404">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7497a-404">Parameters - beginDrag</span></span>

<span data-ttu-id="7497a-405">x</span><span class="sxs-lookup"><span data-stu-id="7497a-405">x</span></span>  
<span data-ttu-id="7497a-406">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-406">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="7497a-407">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="7497a-407">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="7497a-408">y</span><span class="sxs-lookup"><span data-stu-id="7497a-408">y</span></span>  
<span data-ttu-id="7497a-409">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-409">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="7497a-410">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="7497a-410">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="7497a-411">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7497a-411">Return Value - beginDrag</span></span>

<span data-ttu-id="7497a-412">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7497a-412">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="7497a-413">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7497a-413">Remarks - beginDrag</span></span>

<span data-ttu-id="7497a-414">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="7497a-414">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="7497a-415">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="7497a-415">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-big"></a><span data-ttu-id="7497a-416">メソッド big</span><span class="sxs-lookup"><span data-stu-id="7497a-416">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="7497a-417">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="7497a-417">Parameters - big</span></span>

<span data-ttu-id="7497a-418">値</span><span class="sxs-lookup"><span data-stu-id="7497a-418">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="7497a-419">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="7497a-419">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="7497a-420">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="7497a-420">Method bold</span></span>

<span data-ttu-id="7497a-421">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-421">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="7497a-422">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="7497a-422">Parameters - bold</span></span>

<span data-ttu-id="7497a-423">値</span><span class="sxs-lookup"><span data-stu-id="7497a-423">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="7497a-424">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="7497a-424">Return Value - bold</span></span>

<span data-ttu-id="7497a-425">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-425">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="7497a-426">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="7497a-426">Remarks - bold</span></span>

<span data-ttu-id="7497a-427">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7497a-427">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="7497a-428">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="7497a-428">0 Use the default font weight.</span></span>
-   <span data-ttu-id="7497a-429">1 シン。</span><span class="sxs-lookup"><span data-stu-id="7497a-429">1 Thin.</span></span>
-   <span data-ttu-id="7497a-430">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="7497a-430">2 Extra-light.</span></span>
-   <span data-ttu-id="7497a-431">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="7497a-431">3 Light.</span></span>
-   <span data-ttu-id="7497a-432">4 標準。</span><span class="sxs-lookup"><span data-stu-id="7497a-432">4 Normal.</span></span>
-   <span data-ttu-id="7497a-433">5 中。</span><span class="sxs-lookup"><span data-stu-id="7497a-433">5 Medium.</span></span>
-   <span data-ttu-id="7497a-434">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="7497a-434">6 Semibold.</span></span>
-   <span data-ttu-id="7497a-435">7 太字。</span><span class="sxs-lookup"><span data-stu-id="7497a-435">7 Bold.</span></span>
-   <span data-ttu-id="7497a-436">8 極太。</span><span class="sxs-lookup"><span data-stu-id="7497a-436">8 Extra-bold.</span></span>
-   <span data-ttu-id="7497a-437">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="7497a-437">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="7497a-438">メソッド border</span><span class="sxs-lookup"><span data-stu-id="7497a-438">Method border</span></span>

<span data-ttu-id="7497a-439">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-439">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="7497a-440">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="7497a-440">Parameters - border</span></span>

<span data-ttu-id="7497a-441">値</span><span class="sxs-lookup"><span data-stu-id="7497a-441">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="7497a-442">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="7497a-442">Return Value - border</span></span>

<span data-ttu-id="7497a-443">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="7497a-443">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="7497a-444">備考 - border</span><span class="sxs-lookup"><span data-stu-id="7497a-444">Remarks - border</span></span>

<span data-ttu-id="7497a-445">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7497a-445">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="7497a-446">値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-446">Value.</span></span> | <span data-ttu-id="7497a-447">説明。</span><span class="sxs-lookup"><span data-stu-id="7497a-447">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="7497a-448">0</span><span class="sxs-lookup"><span data-stu-id="7497a-448">0</span></span>      | <span data-ttu-id="7497a-449">自動。</span><span class="sxs-lookup"><span data-stu-id="7497a-449">Auto.</span></span>        |
| <span data-ttu-id="7497a-450">1</span><span class="sxs-lookup"><span data-stu-id="7497a-450">1</span></span>      | <span data-ttu-id="7497a-451">3D。</span><span class="sxs-lookup"><span data-stu-id="7497a-451">3D.</span></span>          |
| <span data-ttu-id="7497a-452">2</span><span class="sxs-lookup"><span data-stu-id="7497a-452">2</span></span>      | <span data-ttu-id="7497a-453">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="7497a-453">Single line.</span></span> |
| <span data-ttu-id="7497a-454">3</span><span class="sxs-lookup"><span data-stu-id="7497a-454">3</span></span>      | <span data-ttu-id="7497a-455">均一。</span><span class="sxs-lookup"><span data-stu-id="7497a-455">Flat.</span></span>        |
| <span data-ttu-id="7497a-456">4</span><span class="sxs-lookup"><span data-stu-id="7497a-456">4</span></span>      | <span data-ttu-id="7497a-457">なし。</span><span class="sxs-lookup"><span data-stu-id="7497a-457">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="7497a-458">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="7497a-458">Method buttonDisplay</span></span>

<span data-ttu-id="7497a-459">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-459">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="7497a-460">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="7497a-460">Parameters - buttonDisplay</span></span>

<span data-ttu-id="7497a-461">値</span><span class="sxs-lookup"><span data-stu-id="7497a-461">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="7497a-462">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="7497a-462">Return Value - buttonDisplay</span></span>

<span data-ttu-id="7497a-463">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="7497a-463">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="7497a-464">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="7497a-464">Remarks - buttonDisplay</span></span>

<span data-ttu-id="7497a-465">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="7497a-465">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="7497a-466">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="7497a-466">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="7497a-467">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7497a-467">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="7497a-468">値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-468">Value.</span></span> | <span data-ttu-id="7497a-469">説明。</span><span class="sxs-lookup"><span data-stu-id="7497a-469">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="7497a-470">0</span><span class="sxs-lookup"><span data-stu-id="7497a-470">0</span></span>      | <span data-ttu-id="7497a-471">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="7497a-471">Text only.</span></span>                                                       |
| <span data-ttu-id="7497a-472">1</span><span class="sxs-lookup"><span data-stu-id="7497a-472">1</span></span>      | <span data-ttu-id="7497a-473">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="7497a-473">Image Only.</span></span>                                                      |
| <span data-ttu-id="7497a-474">2</span><span class="sxs-lookup"><span data-stu-id="7497a-474">2</span></span>      | <span data-ttu-id="7497a-475">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-475">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="7497a-476">3</span><span class="sxs-lookup"><span data-stu-id="7497a-476">3</span></span>      | <span data-ttu-id="7497a-477">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-477">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="7497a-478">4</span><span class="sxs-lookup"><span data-stu-id="7497a-478">4</span></span>      | <span data-ttu-id="7497a-479">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-479">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="7497a-480">5</span><span class="sxs-lookup"><span data-stu-id="7497a-480">5</span></span>      | <span data-ttu-id="7497a-481">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-481">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-calccontrolsize"></a><span data-ttu-id="7497a-482">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7497a-482">Method calcControlSize</span></span>

<span data-ttu-id="7497a-483">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-483">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="7497a-484">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7497a-484">Parameters - calcControlSize</span></span>

<span data-ttu-id="7497a-485">chars</span><span class="sxs-lookup"><span data-stu-id="7497a-485">chars</span></span>  
<span data-ttu-id="7497a-486">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="7497a-486">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="7497a-487">明細行</span><span class="sxs-lookup"><span data-stu-id="7497a-487">lines</span></span>  
<span data-ttu-id="7497a-488">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="7497a-488">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="7497a-489">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7497a-489">Return Value - calcControlSize</span></span>

<span data-ttu-id="7497a-490">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="7497a-490">The container that holds the width and height.</span></span>

## <a name="method-caption"></a><span data-ttu-id="7497a-491">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="7497a-491">Method caption</span></span>

<span data-ttu-id="7497a-492">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-492">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="7497a-493">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="7497a-493">Parameters - caption</span></span>

<span data-ttu-id="7497a-494">値</span><span class="sxs-lookup"><span data-stu-id="7497a-494">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="7497a-495">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="7497a-495">Return Value - caption</span></span>

<span data-ttu-id="7497a-496">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="7497a-496">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="7497a-497">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="7497a-497">Method characterSet</span></span>

<span data-ttu-id="7497a-498">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-498">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="7497a-499">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="7497a-499">Parameters - characterSet</span></span>

<span data-ttu-id="7497a-500">値</span><span class="sxs-lookup"><span data-stu-id="7497a-500">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="7497a-501">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="7497a-501">Return Value - characterSet</span></span>

<span data-ttu-id="7497a-502">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-502">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="7497a-503">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="7497a-503">Remarks - characterSet</span></span>

<span data-ttu-id="7497a-504">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-504">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="7497a-505">値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-505">Value.</span></span> | <span data-ttu-id="7497a-506">説明。</span><span class="sxs-lookup"><span data-stu-id="7497a-506">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="7497a-507">0</span><span class="sxs-lookup"><span data-stu-id="7497a-507">0</span></span>      | <span data-ttu-id="7497a-508">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-508">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="7497a-509">1</span><span class="sxs-lookup"><span data-stu-id="7497a-509">1</span></span>      | <span data-ttu-id="7497a-510">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-510">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="7497a-511">2</span><span class="sxs-lookup"><span data-stu-id="7497a-511">2</span></span>      | <span data-ttu-id="7497a-512">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-512">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="7497a-513">77</span><span class="sxs-lookup"><span data-stu-id="7497a-513">77</span></span>     | <span data-ttu-id="7497a-514">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-514">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="7497a-515">128</span><span class="sxs-lookup"><span data-stu-id="7497a-515">128</span></span>    | <span data-ttu-id="7497a-516">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-516">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="7497a-517">129</span><span class="sxs-lookup"><span data-stu-id="7497a-517">129</span></span>    | <span data-ttu-id="7497a-518">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-518">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="7497a-519">134</span><span class="sxs-lookup"><span data-stu-id="7497a-519">134</span></span>    | <span data-ttu-id="7497a-520">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-520">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="7497a-521">136</span><span class="sxs-lookup"><span data-stu-id="7497a-521">136</span></span>    | <span data-ttu-id="7497a-522">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-522">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="7497a-523">161</span><span class="sxs-lookup"><span data-stu-id="7497a-523">161</span></span>    | <span data-ttu-id="7497a-524">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-524">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="7497a-525">162</span><span class="sxs-lookup"><span data-stu-id="7497a-525">162</span></span>    | <span data-ttu-id="7497a-526">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-526">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="7497a-527">163</span><span class="sxs-lookup"><span data-stu-id="7497a-527">163</span></span>    | <span data-ttu-id="7497a-528">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-528">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="7497a-529">186</span><span class="sxs-lookup"><span data-stu-id="7497a-529">186</span></span>    | <span data-ttu-id="7497a-530">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-530">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="7497a-531">204</span><span class="sxs-lookup"><span data-stu-id="7497a-531">204</span></span>    | <span data-ttu-id="7497a-532">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-532">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="7497a-533">238</span><span class="sxs-lookup"><span data-stu-id="7497a-533">238</span></span>    | <span data-ttu-id="7497a-534">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-534">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="7497a-535">255</span><span class="sxs-lookup"><span data-stu-id="7497a-535">255</span></span>    | <span data-ttu-id="7497a-536">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-536">OEM\_CHARSET</span></span>         |

<span data-ttu-id="7497a-537">次のテーブルの値は、韓国語版 msCoNameWindows の値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-537">The value in the following table is for the Korean language edition of msCoNameWindows.</span></span>

| <span data-ttu-id="7497a-538">値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-538">Value.</span></span> | <span data-ttu-id="7497a-539">説明。</span><span class="sxs-lookup"><span data-stu-id="7497a-539">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="7497a-540">130</span><span class="sxs-lookup"><span data-stu-id="7497a-540">130</span></span>    | <span data-ttu-id="7497a-541">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-541">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="7497a-542">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-542">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="7497a-543">値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-543">Value.</span></span> | <span data-ttu-id="7497a-544">説明。</span><span class="sxs-lookup"><span data-stu-id="7497a-544">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="7497a-545">177</span><span class="sxs-lookup"><span data-stu-id="7497a-545">177</span></span>    | <span data-ttu-id="7497a-546">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-546">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="7497a-547">178</span><span class="sxs-lookup"><span data-stu-id="7497a-547">178</span></span>    | <span data-ttu-id="7497a-548">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-548">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="7497a-549">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-549">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="7497a-550">値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-550">Value.</span></span> | <span data-ttu-id="7497a-551">説明。</span><span class="sxs-lookup"><span data-stu-id="7497a-551">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="7497a-552">222</span><span class="sxs-lookup"><span data-stu-id="7497a-552">222</span></span>    | <span data-ttu-id="7497a-553">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7497a-553">THAI\_CHARSET</span></span> |

<span data-ttu-id="7497a-554">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-554">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="7497a-555">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-555">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="7497a-556">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7497a-556">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="7497a-557">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="7497a-557">Method colorScheme</span></span>

<span data-ttu-id="7497a-558">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-558">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="7497a-559">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7497a-559">Parameters - colorScheme</span></span>

<span data-ttu-id="7497a-560">値</span><span class="sxs-lookup"><span data-stu-id="7497a-560">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="7497a-561">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7497a-561">Return Value - colorScheme</span></span>

<span data-ttu-id="7497a-562">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="7497a-562">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="7497a-563">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7497a-563">Remarks - colorScheme</span></span>

<span data-ttu-id="7497a-564">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-564">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="7497a-565">値です。</span><span class="sxs-lookup"><span data-stu-id="7497a-565">Value.</span></span> | <span data-ttu-id="7497a-566">スタイル。</span><span class="sxs-lookup"><span data-stu-id="7497a-566">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="7497a-567">0</span><span class="sxs-lookup"><span data-stu-id="7497a-567">0</span></span>      | <span data-ttu-id="7497a-568">既定。</span><span class="sxs-lookup"><span data-stu-id="7497a-568">Default.</span></span>               |
| <span data-ttu-id="7497a-569">1</span><span class="sxs-lookup"><span data-stu-id="7497a-569">1</span></span>      | <span data-ttu-id="7497a-570">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="7497a-570">The Windows palette.</span></span>   |
| <span data-ttu-id="7497a-571">2</span><span class="sxs-lookup"><span data-stu-id="7497a-571">2</span></span>      | <span data-ttu-id="7497a-572">真の配色。</span><span class="sxs-lookup"><span data-stu-id="7497a-572">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="7497a-573">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="7497a-573">Method configurationKey</span></span>

<span data-ttu-id="7497a-574">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-574">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="7497a-575">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7497a-575">Parameters - configurationKey</span></span>

<span data-ttu-id="7497a-576">値</span><span class="sxs-lookup"><span data-stu-id="7497a-576">value</span></span>  
<span data-ttu-id="7497a-577">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-577">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="7497a-578">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7497a-578">Return Value - configurationKey</span></span>

<span data-ttu-id="7497a-579">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="7497a-579">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="7497a-580">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7497a-580">Remarks - configurationKey</span></span>

<span data-ttu-id="7497a-581">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-581">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="7497a-582">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="7497a-582">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="7497a-583">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7497a-583">Method configurationKeyEx</span></span>

<span data-ttu-id="7497a-584">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-584">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="7497a-585">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7497a-585">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="7497a-586">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="7497a-586">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="7497a-587">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7497a-587">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="7497a-588">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="7497a-588">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="7497a-589">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="7497a-589">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="7497a-590">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7497a-590">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-copycallerquery"></a><span data-ttu-id="7497a-591">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="7497a-591">Method copyCallerQuery</span></span>

```xpp
public int copyCallerQuery([int value])
```

### <a name="parameters---copycallerquery"></a><span data-ttu-id="7497a-592">パラメーター - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="7497a-592">Parameters - copyCallerQuery</span></span>

<span data-ttu-id="7497a-593">値</span><span class="sxs-lookup"><span data-stu-id="7497a-593">value</span></span>  

### <a name="return-value---copycallerquery"></a><span data-ttu-id="7497a-594">戻り値 - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="7497a-594">Return Value - copyCallerQuery</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="7497a-595">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7497a-595">Method countryRegionCodes</span></span>

<span data-ttu-id="7497a-596">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-596">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="7497a-597">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7497a-597">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="7497a-598">値</span><span class="sxs-lookup"><span data-stu-id="7497a-598">value</span></span>  
<span data-ttu-id="7497a-599">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-599">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="7497a-600">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7497a-600">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="7497a-601">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="7497a-601">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="7497a-602">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7497a-602">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="7497a-603">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7497a-603">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="7497a-604">値</span><span class="sxs-lookup"><span data-stu-id="7497a-604">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="7497a-605">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7497a-605">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="7497a-606">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7497a-606">Method dataRelationPath</span></span>

<span data-ttu-id="7497a-607">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-607">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="7497a-608">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7497a-608">Parameters - dataRelationPath</span></span>

<span data-ttu-id="7497a-609">値</span><span class="sxs-lookup"><span data-stu-id="7497a-609">value</span></span>  
<span data-ttu-id="7497a-610">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-610">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="7497a-611">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7497a-611">Return Value - dataRelationPath</span></span>

<span data-ttu-id="7497a-612">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="7497a-612">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="7497a-613">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7497a-613">Remarks - dataRelationPath</span></span>

<span data-ttu-id="7497a-614">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="7497a-614">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="7497a-615">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="7497a-615">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="7497a-616">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="7497a-616">Method dataSource</span></span>

<span data-ttu-id="7497a-617">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-617">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="7497a-618">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="7497a-618">Parameters - dataSource</span></span>

<span data-ttu-id="7497a-619">値</span><span class="sxs-lookup"><span data-stu-id="7497a-619">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="7497a-620">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="7497a-620">Return Value - dataSource</span></span>

<span data-ttu-id="7497a-621">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="7497a-621">The identifier of the data source to be used.</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="7497a-622">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="7497a-622">Method defaultButton</span></span>

<span data-ttu-id="7497a-623">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-623">Determines whether the button should be the default button in the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="7497a-624">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="7497a-624">Parameters - defaultButton</span></span>

<span data-ttu-id="7497a-625">値</span><span class="sxs-lookup"><span data-stu-id="7497a-625">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="7497a-626">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="7497a-626">Return Value - defaultButton</span></span>

<span data-ttu-id="7497a-627">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-627">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="7497a-628">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="7497a-628">Method disabledImage</span></span>

<span data-ttu-id="7497a-629">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-629">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="7497a-630">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="7497a-630">Parameters - disabledImage</span></span>

<span data-ttu-id="7497a-631">値</span><span class="sxs-lookup"><span data-stu-id="7497a-631">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="7497a-632">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="7497a-632">Return Value - disabledImage</span></span>

<span data-ttu-id="7497a-633">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="7497a-633">The full name of an image file.</span></span> <span data-ttu-id="7497a-634">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7497a-634">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="7497a-635">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="7497a-635">Remarks - disabledImage</span></span>

<span data-ttu-id="7497a-636">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="7497a-636">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="7497a-637">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-637">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="7497a-638">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="7497a-638">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="7497a-639">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="7497a-639">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="7497a-640">値</span><span class="sxs-lookup"><span data-stu-id="7497a-640">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="7497a-641">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="7497a-641">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="7497a-642">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="7497a-642">Method disabledResource</span></span>

<span data-ttu-id="7497a-643">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-643">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="7497a-644">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="7497a-644">Parameters - disabledResource</span></span>

<span data-ttu-id="7497a-645">値</span><span class="sxs-lookup"><span data-stu-id="7497a-645">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="7497a-646">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="7497a-646">Return Value - disabledResource</span></span>

<span data-ttu-id="7497a-647">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="7497a-647">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="7497a-648">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7497a-648">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="7497a-649">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="7497a-649">Method displayTarget</span></span>

<span data-ttu-id="7497a-650">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-650">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="7497a-651">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="7497a-651">Parameters - displayTarget</span></span>

<span data-ttu-id="7497a-652">値</span><span class="sxs-lookup"><span data-stu-id="7497a-652">value</span></span>  
<span data-ttu-id="7497a-653">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-653">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="7497a-654">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="7497a-654">Return Value - displayTarget</span></span>

<span data-ttu-id="7497a-655">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="7497a-655">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="7497a-656">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="7497a-656">Method dragDrop</span></span>

<span data-ttu-id="7497a-657">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-657">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="7497a-658">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7497a-658">Parameters - dragDrop</span></span>

<span data-ttu-id="7497a-659">値</span><span class="sxs-lookup"><span data-stu-id="7497a-659">value</span></span>  
<span data-ttu-id="7497a-660">ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-660">An Integer data type that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="7497a-661">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7497a-661">Return Value - dragDrop</span></span>

<span data-ttu-id="7497a-662">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="7497a-662">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="7497a-663">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7497a-663">Remarks - dragDrop</span></span>

<span data-ttu-id="7497a-664">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-664">Use the dragLeave , the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="7497a-665">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="7497a-665">Method dragOver</span></span>

<span data-ttu-id="7497a-666">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-666">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="7497a-667">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="7497a-667">Parameters - dragOver</span></span>

<span data-ttu-id="7497a-668">dragSource</span><span class="sxs-lookup"><span data-stu-id="7497a-668">dragSource</span></span>  
<span data-ttu-id="7497a-669">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-669">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-670">dragMode</span><span class="sxs-lookup"><span data-stu-id="7497a-670">dragMode</span></span>  
<span data-ttu-id="7497a-671">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-671">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-672">x</span><span class="sxs-lookup"><span data-stu-id="7497a-672">x</span></span>  
<span data-ttu-id="7497a-673">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-673">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-674">y</span><span class="sxs-lookup"><span data-stu-id="7497a-674">y</span></span>  
<span data-ttu-id="7497a-675">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-675">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="7497a-676">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="7497a-676">Return Value - dragOver</span></span>

<span data-ttu-id="7497a-677">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7497a-677">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="7497a-678">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7497a-678">Method dragOverEx</span></span>

<span data-ttu-id="7497a-679">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-679">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="7497a-680">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7497a-680">Parameters - dragOverEx</span></span>

<span data-ttu-id="7497a-681">dragSource</span><span class="sxs-lookup"><span data-stu-id="7497a-681">dragSource</span></span>  
<span data-ttu-id="7497a-682">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-682">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-683">dragMode</span><span class="sxs-lookup"><span data-stu-id="7497a-683">dragMode</span></span>  
<span data-ttu-id="7497a-684">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-684">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-685">x</span><span class="sxs-lookup"><span data-stu-id="7497a-685">x</span></span>  
<span data-ttu-id="7497a-686">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-686">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-687">y</span><span class="sxs-lookup"><span data-stu-id="7497a-687">y</span></span>  
<span data-ttu-id="7497a-688">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-688">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="7497a-689">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7497a-689">Return Value - dragOverEx</span></span>

<span data-ttu-id="7497a-690">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7497a-690">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="7497a-691">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="7497a-691">Method dragText</span></span>

<span data-ttu-id="7497a-692">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-692">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="7497a-693">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="7497a-693">Return Value - dragText</span></span>

<span data-ttu-id="7497a-694">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7497a-694">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="7497a-695">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="7497a-695">Method enabled</span></span>

<span data-ttu-id="7497a-696">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-696">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="7497a-697">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="7497a-697">Parameters - enabled</span></span>

<span data-ttu-id="7497a-698">値</span><span class="sxs-lookup"><span data-stu-id="7497a-698">value</span></span>  
<span data-ttu-id="7497a-699">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-699">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="7497a-700">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="7497a-700">Return Value - enabled</span></span>

<span data-ttu-id="7497a-701">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-701">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="7497a-702">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="7497a-702">Remarks - enabled</span></span>

<span data-ttu-id="7497a-703">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="7497a-703">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="7497a-704">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7497a-704">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="7497a-705">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="7497a-705">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="7497a-706">メソッド font</span><span class="sxs-lookup"><span data-stu-id="7497a-706">Method font</span></span>

<span data-ttu-id="7497a-707">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-707">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="7497a-708">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="7497a-708">Parameters - font</span></span>

<span data-ttu-id="7497a-709">値</span><span class="sxs-lookup"><span data-stu-id="7497a-709">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="7497a-710">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="7497a-710">Return Value - font</span></span>

<span data-ttu-id="7497a-711">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="7497a-711">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="7497a-712">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="7497a-712">Method fontSize</span></span>

<span data-ttu-id="7497a-713">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-713">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="7497a-714">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="7497a-714">Parameters - fontSize</span></span>

<span data-ttu-id="7497a-715">値</span><span class="sxs-lookup"><span data-stu-id="7497a-715">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="7497a-716">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="7497a-716">Return Value - fontSize</span></span>

<span data-ttu-id="7497a-717">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="7497a-717">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="7497a-718">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="7497a-718">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="7497a-719">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="7497a-719">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="7497a-720">値</span><span class="sxs-lookup"><span data-stu-id="7497a-720">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="7497a-721">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="7497a-721">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="7497a-722">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-722">Method foregroundColor</span></span>

<span data-ttu-id="7497a-723">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-723">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="7497a-724">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-724">Parameters - foregroundColor</span></span>

<span data-ttu-id="7497a-725">値</span><span class="sxs-lookup"><span data-stu-id="7497a-725">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="7497a-726">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-726">Return Value - foregroundColor</span></span>

<span data-ttu-id="7497a-727">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="7497a-727">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="7497a-728">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7497a-728">Remarks - foregroundColor</span></span>

<span data-ttu-id="7497a-729">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7497a-729">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="7497a-730">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7497a-730">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="7497a-731">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7497a-731">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="7497a-732">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7497a-732">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="7497a-733">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7497a-733">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="7497a-734">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="7497a-734">The maximum value for a single byte is 255.</span></span>

## <a name="method-formviewoption"></a><span data-ttu-id="7497a-735">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="7497a-735">Method formViewOption</span></span>

```xpp
public int formViewOption([int value])
```

### <a name="parameters---formviewoption"></a><span data-ttu-id="7497a-736">パラメータ-formViewOption</span><span class="sxs-lookup"><span data-stu-id="7497a-736">Parameters - formViewOption</span></span>

<span data-ttu-id="7497a-737">値</span><span class="sxs-lookup"><span data-stu-id="7497a-737">value</span></span>  

### <a name="return-value---formviewoption"></a><span data-ttu-id="7497a-738">戻り値 - formViewOption</span><span class="sxs-lookup"><span data-stu-id="7497a-738">Return Value - formViewOption</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="7497a-739">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="7497a-739">Method hasChanged</span></span>

<span data-ttu-id="7497a-740">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-740">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="7497a-741">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="7497a-741">Parameters - hasChanged</span></span>

<span data-ttu-id="7497a-742">val</span><span class="sxs-lookup"><span data-stu-id="7497a-742">val</span></span>  
<span data-ttu-id="7497a-743">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-743">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="7497a-744">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="7497a-744">Return Value - hasChanged</span></span>

<span data-ttu-id="7497a-745">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-745">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="7497a-746">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="7497a-746">Method hasUserSetting</span></span>

<span data-ttu-id="7497a-747">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-747">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="7497a-748">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="7497a-748">Return Value - hasUserSetting</span></span>

<span data-ttu-id="7497a-749">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-749">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="7497a-750">メソッド height</span><span class="sxs-lookup"><span data-stu-id="7497a-750">Method height</span></span>

<span data-ttu-id="7497a-751">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-751">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="7497a-752">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="7497a-752">Parameters - height</span></span>

<span data-ttu-id="7497a-753">値</span><span class="sxs-lookup"><span data-stu-id="7497a-753">value</span></span>  
<span data-ttu-id="7497a-754">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-754">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="7497a-755">モード</span><span class="sxs-lookup"><span data-stu-id="7497a-755">mode</span></span>  
<span data-ttu-id="7497a-756">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-756">An Integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="7497a-757">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="7497a-757">Return Value - height</span></span>

<span data-ttu-id="7497a-758">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="7497a-758">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="7497a-759">備考 - height</span><span class="sxs-lookup"><span data-stu-id="7497a-759">Remarks - height</span></span>

<span data-ttu-id="7497a-760">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-760">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7497a-761">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="7497a-761">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="7497a-762">モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-762">Mode.</span></span>            | <span data-ttu-id="7497a-763">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="7497a-763">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7497a-764">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="7497a-764">-1 Exact.</span></span>        | <span data-ttu-id="7497a-765">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-765">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7497a-766">0 自動。</span><span class="sxs-lookup"><span data-stu-id="7497a-766">0 Auto.</span></span>          | <span data-ttu-id="7497a-767">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-767">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7497a-768">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="7497a-768">1 Column height.</span></span> | <span data-ttu-id="7497a-769">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7497a-769">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7497a-770">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7497a-770">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="7497a-771">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="7497a-771">Method heightMode</span></span>

<span data-ttu-id="7497a-772">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-772">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="7497a-773">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="7497a-773">Parameters - heightMode</span></span>

<span data-ttu-id="7497a-774">値</span><span class="sxs-lookup"><span data-stu-id="7497a-774">value</span></span>  
<span data-ttu-id="7497a-775">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-775">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="7497a-776">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7497a-776">Return Value - heightMode</span></span>

<span data-ttu-id="7497a-777">計算モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-777">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="7497a-778">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7497a-778">Remarks - heightMode</span></span>

<span data-ttu-id="7497a-779">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="7497a-779">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="7497a-780">モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-780">Mode.</span></span>          | <span data-ttu-id="7497a-781">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="7497a-781">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7497a-782">正確。</span><span class="sxs-lookup"><span data-stu-id="7497a-782">Exact.</span></span>         | <span data-ttu-id="7497a-783">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-783">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7497a-784">自動。</span><span class="sxs-lookup"><span data-stu-id="7497a-784">Auto.</span></span>          | <span data-ttu-id="7497a-785">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-785">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7497a-786">列の高さ</span><span class="sxs-lookup"><span data-stu-id="7497a-786">Column height.</span></span> | <span data-ttu-id="7497a-787">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7497a-787">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7497a-788">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7497a-788">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="7497a-789">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="7497a-789">Method heightValue</span></span>

<span data-ttu-id="7497a-790">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-790">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="7497a-791">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="7497a-791">Parameters - heightValue</span></span>

<span data-ttu-id="7497a-792">値</span><span class="sxs-lookup"><span data-stu-id="7497a-792">value</span></span>  
<span data-ttu-id="7497a-793">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-793">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="7497a-794">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7497a-794">Return Value - heightValue</span></span>

<span data-ttu-id="7497a-795">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="7497a-795">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="7497a-796">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7497a-796">Remarks - heightValue</span></span>

<span data-ttu-id="7497a-797">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7497a-797">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="7497a-798">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="7497a-798">Method helpField</span></span>

<span data-ttu-id="7497a-799">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-799">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="7497a-800">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="7497a-800">Return Value - helpField</span></span>

<span data-ttu-id="7497a-801">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7497a-801">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="7497a-802">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="7497a-802">Remarks - helpField</span></span>

<span data-ttu-id="7497a-803">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="7497a-803">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="7497a-804">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7497a-804">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="7497a-805">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7497a-805">Method helpText</span></span>

<span data-ttu-id="7497a-806">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-806">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="7497a-807">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="7497a-807">Parameters - helpText</span></span>

<span data-ttu-id="7497a-808">値</span><span class="sxs-lookup"><span data-stu-id="7497a-808">value</span></span>  
<span data-ttu-id="7497a-809">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="7497a-809">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="7497a-810">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="7497a-810">Return Value - helpText</span></span>

<span data-ttu-id="7497a-811">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7497a-811">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="7497a-812">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="7497a-812">Remarks - helpText</span></span>

<span data-ttu-id="7497a-813">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-813">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="7497a-814">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7497a-814">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="7497a-815">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7497a-815">Method hierarchyParent</span></span>

<span data-ttu-id="7497a-816">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-816">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="7497a-817">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7497a-817">Parameters - hierarchyParent</span></span>

<span data-ttu-id="7497a-818">値</span><span class="sxs-lookup"><span data-stu-id="7497a-818">value</span></span>  
<span data-ttu-id="7497a-819">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="7497a-819">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="7497a-820">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7497a-820">Return Value - hierarchyParent</span></span>

<span data-ttu-id="7497a-821">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="7497a-821">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="7497a-822">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="7497a-822">Method hWnd</span></span>

<span data-ttu-id="7497a-823">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-823">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="7497a-824">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="7497a-824">Return Value - hWnd</span></span>

<span data-ttu-id="7497a-825">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="7497a-825">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="7497a-826">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="7497a-826">Remarks - hWnd</span></span>

<span data-ttu-id="7497a-827">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7497a-827">The handle can be used with the Windows API.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="7497a-828">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="7497a-828">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="7497a-829">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="7497a-829">Parameters - imageLocation</span></span>

<span data-ttu-id="7497a-830">値</span><span class="sxs-lookup"><span data-stu-id="7497a-830">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="7497a-831">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="7497a-831">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="7497a-832">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="7497a-832">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="7497a-833">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="7497a-833">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="7497a-834">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7497a-834">Method isDisplayed</span></span>

<span data-ttu-id="7497a-835">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-835">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="7497a-836">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7497a-836">Return Value - isDisplayed</span></span>

<span data-ttu-id="7497a-837">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7497a-837">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="7497a-838">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7497a-838">Remarks - isDisplayed</span></span>

<span data-ttu-id="7497a-839">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7497a-839">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="7497a-840">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="7497a-840">Method isRestricted</span></span>

<span data-ttu-id="7497a-841">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-841">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="7497a-842">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="7497a-842">Return Value - isRestricted</span></span>

<span data-ttu-id="7497a-843">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7497a-843">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="7497a-844">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7497a-844">Method isUserSetupEnabled</span></span>

<span data-ttu-id="7497a-845">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-845">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="7497a-846">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7497a-846">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="7497a-847">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="7497a-847">neededSetupRights</span></span>  
<span data-ttu-id="7497a-848">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="7497a-848">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="7497a-849">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7497a-849">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="7497a-850">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-850">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="7497a-851">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7497a-851">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="7497a-852">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="7497a-852">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7497a-853">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="7497a-853">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="7497a-854">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="7497a-854">No changes can be made to the control.</span></span> <span data-ttu-id="7497a-855">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-855">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="7497a-856">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="7497a-856">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="7497a-857">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7497a-857">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="7497a-858">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="7497a-858">The user cannot move the control.</span></span>   |
| <span data-ttu-id="7497a-859">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="7497a-859">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="7497a-860">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7497a-860">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="7497a-861">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="7497a-861">The user can also move the control.</span></span> |

<span data-ttu-id="7497a-862">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="7497a-862">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="7497a-863">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="7497a-863">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="7497a-864">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="7497a-864">Parameters - italic</span></span>

<span data-ttu-id="7497a-865">値</span><span class="sxs-lookup"><span data-stu-id="7497a-865">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="7497a-866">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="7497a-866">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="7497a-867">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="7497a-867">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="7497a-868">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="7497a-868">Parameters - keyTip</span></span>

<span data-ttu-id="7497a-869">値</span><span class="sxs-lookup"><span data-stu-id="7497a-869">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="7497a-870">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="7497a-870">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="7497a-871">メソッド left</span><span class="sxs-lookup"><span data-stu-id="7497a-871">Method left</span></span>

<span data-ttu-id="7497a-872">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-872">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="7497a-873">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="7497a-873">Parameters - left</span></span>

<span data-ttu-id="7497a-874">値</span><span class="sxs-lookup"><span data-stu-id="7497a-874">value</span></span>  
<span data-ttu-id="7497a-875">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-875">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7497a-876">モード</span><span class="sxs-lookup"><span data-stu-id="7497a-876">mode</span></span>  
<span data-ttu-id="7497a-877">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-877">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="7497a-878">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="7497a-878">Return Value - left</span></span>

<span data-ttu-id="7497a-879">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="7497a-879">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="7497a-880">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="7497a-880">Method leftMode</span></span>

<span data-ttu-id="7497a-881">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-881">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="7497a-882">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="7497a-882">Parameters - leftMode</span></span>

<span data-ttu-id="7497a-883">値</span><span class="sxs-lookup"><span data-stu-id="7497a-883">value</span></span>  
<span data-ttu-id="7497a-884">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-884">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="7497a-885">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="7497a-885">Return Value - leftMode</span></span>

<span data-ttu-id="7497a-886">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-886">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="7497a-887">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="7497a-887">Method leftValue</span></span>

<span data-ttu-id="7497a-888">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-888">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="7497a-889">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="7497a-889">Parameters - leftValue</span></span>

<span data-ttu-id="7497a-890">値</span><span class="sxs-lookup"><span data-stu-id="7497a-890">value</span></span>  
<span data-ttu-id="7497a-891">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-891">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="7497a-892">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="7497a-892">Return Value - leftValue</span></span>

<span data-ttu-id="7497a-893">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="7497a-893">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="7497a-894">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7497a-894">Method markAsUserAdd</span></span>

<span data-ttu-id="7497a-895">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="7497a-895">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="7497a-896">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7497a-896">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="7497a-897">値</span><span class="sxs-lookup"><span data-stu-id="7497a-897">value</span></span>  
<span data-ttu-id="7497a-898">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-898">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="7497a-899">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7497a-899">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="7497a-900">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-900">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-menufunction"></a><span data-ttu-id="7497a-901">メソッド menufunction</span><span class="sxs-lookup"><span data-stu-id="7497a-901">Method menufunction</span></span>

```xpp
public xMenuFunction menufunction()
```

### <a name="return-value---menufunction"></a><span data-ttu-id="7497a-902">戻り値 - menufunction</span><span class="sxs-lookup"><span data-stu-id="7497a-902">Return Value - menufunction</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="7497a-903">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="7497a-903">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="7497a-904">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="7497a-904">Parameters - menuItemName</span></span>

<span data-ttu-id="7497a-905">値</span><span class="sxs-lookup"><span data-stu-id="7497a-905">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="7497a-906">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="7497a-906">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="7497a-907">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="7497a-907">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="7497a-908">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="7497a-908">Parameters - menuItemType</span></span>

<span data-ttu-id="7497a-909">値</span><span class="sxs-lookup"><span data-stu-id="7497a-909">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="7497a-910">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="7497a-910">Return Value - menuItemType</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="7497a-911">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7497a-911">Method mouseDblClick</span></span>

<span data-ttu-id="7497a-912">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-912">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="7497a-913">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7497a-913">Parameters - mouseDblClick</span></span>

<span data-ttu-id="7497a-914">x</span><span class="sxs-lookup"><span data-stu-id="7497a-914">x</span></span>  
<span data-ttu-id="7497a-915">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-915">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-916">y</span><span class="sxs-lookup"><span data-stu-id="7497a-916">y</span></span>  
<span data-ttu-id="7497a-917">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-917">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-918">ボタン</span><span class="sxs-lookup"><span data-stu-id="7497a-918">button</span></span>  
<span data-ttu-id="7497a-919">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-919">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-920">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7497a-920">Ctrl</span></span>  
<span data-ttu-id="7497a-921">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-921">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-922">シフト</span><span class="sxs-lookup"><span data-stu-id="7497a-922">Shift</span></span>  
<span data-ttu-id="7497a-923">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-923">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="7497a-924">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7497a-924">Return Value - mouseDblClick</span></span>

<span data-ttu-id="7497a-925">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7497a-925">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="7497a-926">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7497a-926">Remarks - mouseDblClick</span></span>

<span data-ttu-id="7497a-927">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-927">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="7497a-928">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="7497a-928">Method mouseDown</span></span>

<span data-ttu-id="7497a-929">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-929">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="7497a-930">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7497a-930">Parameters - mouseDown</span></span>

<span data-ttu-id="7497a-931">x</span><span class="sxs-lookup"><span data-stu-id="7497a-931">x</span></span>  
<span data-ttu-id="7497a-932">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-932">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-933">y</span><span class="sxs-lookup"><span data-stu-id="7497a-933">y</span></span>  
<span data-ttu-id="7497a-934">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-934">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-935">ボタン</span><span class="sxs-lookup"><span data-stu-id="7497a-935">button</span></span>  
<span data-ttu-id="7497a-936">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-936">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-937">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7497a-937">Ctrl</span></span>  
<span data-ttu-id="7497a-938">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-938">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-939">シフト</span><span class="sxs-lookup"><span data-stu-id="7497a-939">Shift</span></span>  
<span data-ttu-id="7497a-940">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-940">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="7497a-941">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7497a-941">Return Value - mouseDown</span></span>

<span data-ttu-id="7497a-942">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7497a-942">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="7497a-943">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7497a-943">Remarks - mouseDown</span></span>

<span data-ttu-id="7497a-944">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-944">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="7497a-945">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-945">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="7497a-946">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="7497a-946">Method mouseMove</span></span>

<span data-ttu-id="7497a-947">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-947">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="7497a-948">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7497a-948">Parameters - mouseMove</span></span>

<span data-ttu-id="7497a-949">x</span><span class="sxs-lookup"><span data-stu-id="7497a-949">x</span></span>  
<span data-ttu-id="7497a-950">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-950">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-951">y</span><span class="sxs-lookup"><span data-stu-id="7497a-951">y</span></span>  
<span data-ttu-id="7497a-952">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-952">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-953">ボタン</span><span class="sxs-lookup"><span data-stu-id="7497a-953">button</span></span>  
<span data-ttu-id="7497a-954">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-954">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-955">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7497a-955">Ctrl</span></span>  
<span data-ttu-id="7497a-956">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-956">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-957">シフト</span><span class="sxs-lookup"><span data-stu-id="7497a-957">Shift</span></span>  
<span data-ttu-id="7497a-958">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-958">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="7497a-959">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7497a-959">Return Value - mouseMove</span></span>

<span data-ttu-id="7497a-960">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7497a-960">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="7497a-961">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7497a-961">Remarks - mouseMove</span></span>

<span data-ttu-id="7497a-962">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-962">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="7497a-963">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="7497a-963">Method mouseUp</span></span>

<span data-ttu-id="7497a-964">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-964">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="7497a-965">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7497a-965">Parameters - mouseUp</span></span>

<span data-ttu-id="7497a-966">x</span><span class="sxs-lookup"><span data-stu-id="7497a-966">x</span></span>  
<span data-ttu-id="7497a-967">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-967">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-968">y</span><span class="sxs-lookup"><span data-stu-id="7497a-968">y</span></span>  
<span data-ttu-id="7497a-969">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-969">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-970">ボタン</span><span class="sxs-lookup"><span data-stu-id="7497a-970">button</span></span>  
<span data-ttu-id="7497a-971">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-971">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-972">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7497a-972">Ctrl</span></span>  
<span data-ttu-id="7497a-973">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-973">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-974">シフト</span><span class="sxs-lookup"><span data-stu-id="7497a-974">Shift</span></span>  
<span data-ttu-id="7497a-975">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-975">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="7497a-976">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7497a-976">Return Value - mouseUp</span></span>

<span data-ttu-id="7497a-977">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7497a-977">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="7497a-978">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7497a-978">Remarks - mouseUp</span></span>

<span data-ttu-id="7497a-979">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-979">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="7497a-980">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-980">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="7497a-981">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="7497a-981">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="7497a-982">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="7497a-982">Parameters - multiSelect</span></span>

<span data-ttu-id="7497a-983">値</span><span class="sxs-lookup"><span data-stu-id="7497a-983">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="7497a-984">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="7497a-984">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="7497a-985">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7497a-985">Method name</span></span>

<span data-ttu-id="7497a-986">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-986">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="7497a-987">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="7497a-987">Parameters - name</span></span>

<span data-ttu-id="7497a-988">値</span><span class="sxs-lookup"><span data-stu-id="7497a-988">value</span></span>  
<span data-ttu-id="7497a-989">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="7497a-989">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="7497a-990">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="7497a-990">Return Value - name</span></span>

<span data-ttu-id="7497a-991">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7497a-991">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="7497a-992">備考 - name</span><span class="sxs-lookup"><span data-stu-id="7497a-992">Remarks - name</span></span>

<span data-ttu-id="7497a-993">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7497a-993">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7497a-994">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7497a-994">It must begin with a letter.</span></span>
-   <span data-ttu-id="7497a-995">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7497a-995">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="7497a-996">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7497a-996">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="7497a-997">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7497a-997">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7497a-998">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7497a-998">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="7497a-999">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="7497a-999">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="7497a-1000">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="7497a-1000">Parameters - neededPermission</span></span>

<span data-ttu-id="7497a-1001">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1001">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="7497a-1002">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="7497a-1002">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="7497a-1003">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="7497a-1003">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="7497a-1004">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="7497a-1004">Parameters - needsRecord</span></span>

<span data-ttu-id="7497a-1005">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1005">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="7497a-1006">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="7497a-1006">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="7497a-1007">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="7497a-1007">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="7497a-1008">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="7497a-1008">Parameters - normalImage</span></span>

<span data-ttu-id="7497a-1009">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1009">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="7497a-1010">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="7497a-1010">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="7497a-1011">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="7497a-1011">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="7497a-1012">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="7497a-1012">Parameters - normalResource</span></span>

<span data-ttu-id="7497a-1013">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1013">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="7497a-1014">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="7497a-1014">Return Value - normalResource</span></span>

## <a name="method-openmode"></a><span data-ttu-id="7497a-1015">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1015">Method openMode</span></span>

```xpp
public int openMode([int value])
```

### <a name="parameters---openmode"></a><span data-ttu-id="7497a-1016">パラメーター - openMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1016">Parameters - openMode</span></span>

<span data-ttu-id="7497a-1017">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1017">value</span></span>  

### <a name="return-value---openmode"></a><span data-ttu-id="7497a-1018">戻り値 - openMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1018">Return Value - openMode</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="7497a-1019">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7497a-1019">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="7497a-1020">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7497a-1020">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parameters"></a><span data-ttu-id="7497a-1021">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="7497a-1021">Method parameters</span></span>

<span data-ttu-id="7497a-1022">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1022">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="7497a-1023">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="7497a-1023">Parameters - parameters</span></span>

<span data-ttu-id="7497a-1024">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1024">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="7497a-1025">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="7497a-1025">Return Value - parameters</span></span>

<span data-ttu-id="7497a-1026">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="7497a-1026">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="7497a-1027">備考 - パラメータ</span><span class="sxs-lookup"><span data-stu-id="7497a-1027">Remarks - parameters</span></span>

<span data-ttu-id="7497a-1028">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="7497a-1028">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="7497a-1029">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1029">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="7497a-1030">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="7497a-1030">Method parentControl</span></span>

<span data-ttu-id="7497a-1031">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1031">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="7497a-1032">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="7497a-1032">Return Value - parentControl</span></span>

<span data-ttu-id="7497a-1033">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="7497a-1033">The parent control for the control.</span></span>

## <a name="method-primary"></a><span data-ttu-id="7497a-1034">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="7497a-1034">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="7497a-1035">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="7497a-1035">Parameters - primary</span></span>

<span data-ttu-id="7497a-1036">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1036">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="7497a-1037">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="7497a-1037">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="7497a-1038">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="7497a-1038">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="7497a-1039">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="7497a-1039">Parameters - saveRecord</span></span>

<span data-ttu-id="7497a-1040">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1040">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="7497a-1041">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="7497a-1041">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="7497a-1042">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="7497a-1042">Method securityKey</span></span>

<span data-ttu-id="7497a-1043">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1043">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="7497a-1044">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="7497a-1044">Parameters - securityKey</span></span>

<span data-ttu-id="7497a-1045">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1045">value</span></span>  
<span data-ttu-id="7497a-1046">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1046">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="7497a-1047">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="7497a-1047">Return Value - securityKey</span></span>

<span data-ttu-id="7497a-1048">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1048">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-sendexternalcontext"></a><span data-ttu-id="7497a-1049">メソッド sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="7497a-1049">Method sendExternalContext</span></span>

```xpp
public boolean sendExternalContext([boolean value])
```

### <a name="parameters---sendexternalcontext"></a><span data-ttu-id="7497a-1050">パラメーター - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="7497a-1050">Parameters - sendExternalContext</span></span>

<span data-ttu-id="7497a-1051">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1051">value</span></span>  

### <a name="return-value---sendexternalcontext"></a><span data-ttu-id="7497a-1052">戻り値 - sendExternalContext</span><span class="sxs-lookup"><span data-stu-id="7497a-1052">Return Value - sendExternalContext</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="7497a-1053">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="7497a-1053">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="7497a-1054">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="7497a-1054">Parameters - shortkey</span></span>

<span data-ttu-id="7497a-1055">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1055">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="7497a-1056">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="7497a-1056">Return Value - shortkey</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="7497a-1057">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7497a-1057">Method showContextMenu</span></span>

<span data-ttu-id="7497a-1058">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1058">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="7497a-1059">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7497a-1059">Parameters - showContextMenu</span></span>

<span data-ttu-id="7497a-1060">menuHandle</span><span class="sxs-lookup"><span data-stu-id="7497a-1060">menuHandle</span></span>  
<span data-ttu-id="7497a-1061">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="7497a-1061">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="7497a-1062">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7497a-1062">Return Value - showContextMenu</span></span>

<span data-ttu-id="7497a-1063">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1063">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="7497a-1064">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="7497a-1064">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="7497a-1065">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="7497a-1065">Parameters - showShortCut</span></span>

<span data-ttu-id="7497a-1066">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1066">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="7497a-1067">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="7497a-1067">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="7497a-1068">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="7497a-1068">Method skip</span></span>

<span data-ttu-id="7497a-1069">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1069">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="7497a-1070">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="7497a-1070">Parameters - skip</span></span>

<span data-ttu-id="7497a-1071">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1071">value</span></span>  
<span data-ttu-id="7497a-1072">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1072">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="7497a-1073">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="7497a-1073">Return Value - skip</span></span>

<span data-ttu-id="7497a-1074">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7497a-1074">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="7497a-1075">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="7497a-1075">Remarks - skip</span></span>

<span data-ttu-id="7497a-1076">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1076">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="7497a-1077">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="7497a-1077">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="7497a-1078">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="7497a-1078">Parameters - sort</span></span>

<span data-ttu-id="7497a-1079">sortDirection</span><span class="sxs-lookup"><span data-stu-id="7497a-1079">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="7497a-1080">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="7497a-1080">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="7497a-1081">メソッド style</span><span class="sxs-lookup"><span data-stu-id="7497a-1081">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="7497a-1082">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="7497a-1082">Parameters - style</span></span>

<span data-ttu-id="7497a-1083">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1083">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="7497a-1084">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="7497a-1084">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="7497a-1085">メソッド text</span><span class="sxs-lookup"><span data-stu-id="7497a-1085">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="7497a-1086">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="7497a-1086">Parameters - text</span></span>

<span data-ttu-id="7497a-1087">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1087">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="7497a-1088">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="7497a-1088">Return Value - text</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="7497a-1089">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="7497a-1089">Method toolTip</span></span>

<span data-ttu-id="7497a-1090">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1090">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="7497a-1091">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="7497a-1091">Return Value - toolTip</span></span>

<span data-ttu-id="7497a-1092">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7497a-1092">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="7497a-1093">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="7497a-1093">Remarks - toolTip</span></span>

<span data-ttu-id="7497a-1094">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1094">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="7497a-1095">メソッド top</span><span class="sxs-lookup"><span data-stu-id="7497a-1095">Method top</span></span>

<span data-ttu-id="7497a-1096">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1096">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="7497a-1097">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="7497a-1097">Parameters - top</span></span>

<span data-ttu-id="7497a-1098">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1098">value</span></span>  
<span data-ttu-id="7497a-1099">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1099">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7497a-1100">モード</span><span class="sxs-lookup"><span data-stu-id="7497a-1100">mode</span></span>  
<span data-ttu-id="7497a-1101">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1101">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="7497a-1102">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="7497a-1102">Return Value - top</span></span>

<span data-ttu-id="7497a-1103">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="7497a-1103">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="7497a-1104">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1104">Method topMode</span></span>

<span data-ttu-id="7497a-1105">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1105">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="7497a-1106">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1106">Parameters - topMode</span></span>

<span data-ttu-id="7497a-1107">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1107">value</span></span>  
<span data-ttu-id="7497a-1108">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1108">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="7497a-1109">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1109">Return Value - topMode</span></span>

<span data-ttu-id="7497a-1110">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-1110">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="7497a-1111">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1111">Method topValue</span></span>

<span data-ttu-id="7497a-1112">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1112">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="7497a-1113">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1113">Parameters - topValue</span></span>

<span data-ttu-id="7497a-1114">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1114">value</span></span>  
<span data-ttu-id="7497a-1115">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1115">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="7497a-1116">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1116">Return Value - topValue</span></span>

<span data-ttu-id="7497a-1117">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="7497a-1117">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="7497a-1118">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="7497a-1118">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="7497a-1119">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="7497a-1119">Parameters - type</span></span>

<span data-ttu-id="7497a-1120">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1120">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="7497a-1121">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="7497a-1121">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="7497a-1122">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="7497a-1122">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="7497a-1123">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="7497a-1123">Parameters - underline</span></span>

<span data-ttu-id="7497a-1124">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1124">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="7497a-1125">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="7497a-1125">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="7497a-1126">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7497a-1126">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="7497a-1127">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7497a-1127">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="7497a-1128">データ</span><span class="sxs-lookup"><span data-stu-id="7497a-1128">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="7497a-1129">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7497a-1129">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="7497a-1130">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="7497a-1130">Method userData</span></span>

<span data-ttu-id="7497a-1131">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1131">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="7497a-1132">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="7497a-1132">Parameters - userData</span></span>

<span data-ttu-id="7497a-1133">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1133">value</span></span>  
<span data-ttu-id="7497a-1134">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1134">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="7497a-1135">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="7497a-1135">Return Value - userData</span></span>

<span data-ttu-id="7497a-1136">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="7497a-1136">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="7497a-1137">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="7497a-1137">Method userDataItem</span></span>

<span data-ttu-id="7497a-1138">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1138">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="7497a-1139">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="7497a-1139">Parameters - userDataItem</span></span>

<span data-ttu-id="7497a-1140">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1140">value</span></span>  
<span data-ttu-id="7497a-1141">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1141">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="7497a-1142">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="7497a-1142">Return Value - userDataItem</span></span>

<span data-ttu-id="7497a-1143">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="7497a-1143">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="7497a-1144">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="7497a-1144">Method userDataItems</span></span>

<span data-ttu-id="7497a-1145">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1145">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="7497a-1146">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="7497a-1146">Parameters - userDataItems</span></span>

<span data-ttu-id="7497a-1147">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1147">value</span></span>  
<span data-ttu-id="7497a-1148">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1148">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="7497a-1149">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="7497a-1149">Return Value - userDataItems</span></span>

<span data-ttu-id="7497a-1150">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="7497a-1150">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="7497a-1151">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="7497a-1151">Method userDisable</span></span>

<span data-ttu-id="7497a-1152">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1152">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="7497a-1153">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="7497a-1153">Parameters - userDisable</span></span>

<span data-ttu-id="7497a-1154">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1154">value</span></span>  
<span data-ttu-id="7497a-1155">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1155">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="7497a-1156">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="7497a-1156">Return Value - userDisable</span></span>

<span data-ttu-id="7497a-1157">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7497a-1157">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="7497a-1158">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="7497a-1158">Method userHeight</span></span>

<span data-ttu-id="7497a-1159">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1159">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="7497a-1160">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="7497a-1160">Parameters - userHeight</span></span>

<span data-ttu-id="7497a-1161">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1161">value</span></span>  
<span data-ttu-id="7497a-1162">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1162">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="7497a-1163">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="7497a-1163">Return Value - userHeight</span></span>

<span data-ttu-id="7497a-1164">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="7497a-1164">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="7497a-1165">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="7497a-1165">Method userHide</span></span>

<span data-ttu-id="7497a-1166">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1166">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="7497a-1167">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="7497a-1167">Parameters - userHide</span></span>

<span data-ttu-id="7497a-1168">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1168">value</span></span>  
<span data-ttu-id="7497a-1169">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1169">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="7497a-1170">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="7497a-1170">Return Value - userHide</span></span>

<span data-ttu-id="7497a-1171">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7497a-1171">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="7497a-1172">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="7497a-1172">Remarks - userHide</span></span>

<span data-ttu-id="7497a-1173">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1173">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="7497a-1174">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1174">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="7497a-1175">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1175">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="7497a-1176">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7497a-1176">Method userOrgContainer</span></span>

<span data-ttu-id="7497a-1177">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1177">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="7497a-1178">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7497a-1178">Parameters - userOrgContainer</span></span>

<span data-ttu-id="7497a-1179">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1179">value</span></span>  
<span data-ttu-id="7497a-1180">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1180">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="7497a-1181">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7497a-1181">Return Value - userOrgContainer</span></span>

<span data-ttu-id="7497a-1182">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="7497a-1182">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="7497a-1183">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7497a-1183">Method userOrgSibling</span></span>

<span data-ttu-id="7497a-1184">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1184">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="7497a-1185">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7497a-1185">Parameters - userOrgSibling</span></span>

<span data-ttu-id="7497a-1186">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1186">value</span></span>  
<span data-ttu-id="7497a-1187">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1187">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="7497a-1188">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7497a-1188">Return Value - userOrgSibling</span></span>

<span data-ttu-id="7497a-1189">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="7497a-1189">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="7497a-1190">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="7497a-1190">Method userPromptText</span></span>

<span data-ttu-id="7497a-1191">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1191">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="7497a-1192">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="7497a-1192">Parameters - userPromptText</span></span>

<span data-ttu-id="7497a-1193">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1193">value</span></span>  
<span data-ttu-id="7497a-1194">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1194">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="7497a-1195">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="7497a-1195">Return Value - userPromptText</span></span>

<span data-ttu-id="7497a-1196">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="7497a-1196">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="7497a-1197">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7497a-1197">Method userSecurityLevel</span></span>

<span data-ttu-id="7497a-1198">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1198">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="7497a-1199">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7497a-1199">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="7497a-1200">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1200">value</span></span>  
<span data-ttu-id="7497a-1201">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1201">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="7497a-1202">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7497a-1202">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="7497a-1203">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="7497a-1203">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="7497a-1204">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="7497a-1204">Method userSkip</span></span>

<span data-ttu-id="7497a-1205">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1205">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="7497a-1206">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="7497a-1206">Parameters - userSkip</span></span>

<span data-ttu-id="7497a-1207">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1207">value</span></span>  
<span data-ttu-id="7497a-1208">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1208">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="7497a-1209">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="7497a-1209">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="7497a-1210">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="7497a-1210">Return Value - userSkip</span></span>

<span data-ttu-id="7497a-1211">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="7497a-1211">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="7497a-1212">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="7497a-1212">Method userWidth</span></span>

<span data-ttu-id="7497a-1213">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1213">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="7497a-1214">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="7497a-1214">Parameters - userWidth</span></span>

<span data-ttu-id="7497a-1215">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1215">value</span></span>  
<span data-ttu-id="7497a-1216">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1216">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="7497a-1217">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="7497a-1217">Return Value - userWidth</span></span>

<span data-ttu-id="7497a-1218">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1218">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="7497a-1219">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="7497a-1219">Remarks - userWidth</span></span>

<span data-ttu-id="7497a-1220">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1220">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="7497a-1221">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="7497a-1221">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="7497a-1222">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1222">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-value"></a><span data-ttu-id="7497a-1223">メソッド value</span><span class="sxs-lookup"><span data-stu-id="7497a-1223">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="7497a-1224">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="7497a-1224">Parameters - value</span></span>

<span data-ttu-id="7497a-1225">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1225">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="7497a-1226">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="7497a-1226">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="7497a-1227">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7497a-1227">Method verticalSpacing</span></span>

<span data-ttu-id="7497a-1228">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1228">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="7497a-1229">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7497a-1229">Parameters - verticalSpacing</span></span>

<span data-ttu-id="7497a-1230">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1230">value</span></span>  
<span data-ttu-id="7497a-1231">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1231">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7497a-1232">モード</span><span class="sxs-lookup"><span data-stu-id="7497a-1232">mode</span></span>  
<span data-ttu-id="7497a-1233">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1233">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="7497a-1234">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7497a-1234">Return Value - verticalSpacing</span></span>

<span data-ttu-id="7497a-1235">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="7497a-1235">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="7497a-1236">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1236">Method verticalSpacingMode</span></span>

<span data-ttu-id="7497a-1237">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1237">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="7497a-1238">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1238">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="7497a-1239">モード</span><span class="sxs-lookup"><span data-stu-id="7497a-1239">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="7497a-1240">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1240">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="7497a-1241">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-1241">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="7497a-1242">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1242">Method verticalSpacingValue</span></span>

<span data-ttu-id="7497a-1243">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1243">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="7497a-1244">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1244">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="7497a-1245">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1245">value</span></span>  
<span data-ttu-id="7497a-1246">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1246">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="7497a-1247">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1247">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="7497a-1248">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="7497a-1248">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="7497a-1249">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="7497a-1249">Method visible</span></span>

<span data-ttu-id="7497a-1250">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1250">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="7497a-1251">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="7497a-1251">Parameters - visible</span></span>

<span data-ttu-id="7497a-1252">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1252">value</span></span>  
<span data-ttu-id="7497a-1253">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1253">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="7497a-1254">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="7497a-1254">Return Value - visible</span></span>

<span data-ttu-id="7497a-1255">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7497a-1255">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="7497a-1256">メソッド width</span><span class="sxs-lookup"><span data-stu-id="7497a-1256">Method width</span></span>

<span data-ttu-id="7497a-1257">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1257">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="7497a-1258">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="7497a-1258">Parameters - width</span></span>

<span data-ttu-id="7497a-1259">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1259">value</span></span>  
<span data-ttu-id="7497a-1260">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1260">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="7497a-1261">モード</span><span class="sxs-lookup"><span data-stu-id="7497a-1261">mode</span></span>  
<span data-ttu-id="7497a-1262">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1262">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="7497a-1263">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="7497a-1263">Return Value - width</span></span>

<span data-ttu-id="7497a-1264">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="7497a-1264">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="7497a-1265">備考 - width</span><span class="sxs-lookup"><span data-stu-id="7497a-1265">Remarks - width</span></span>

<span data-ttu-id="7497a-1266">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1266">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7497a-1267">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="7497a-1267">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="7497a-1268">モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-1268">Mode.</span></span>           | <span data-ttu-id="7497a-1269">幅計算。</span><span class="sxs-lookup"><span data-stu-id="7497a-1269">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7497a-1270">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="7497a-1270">-1 Exact.</span></span>       | <span data-ttu-id="7497a-1271">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1271">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7497a-1272">0 自動。</span><span class="sxs-lookup"><span data-stu-id="7497a-1272">0 Auto.</span></span>         | <span data-ttu-id="7497a-1273">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1273">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7497a-1274">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="7497a-1274">1 Column width.</span></span> | <span data-ttu-id="7497a-1275">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7497a-1275">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7497a-1276">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1276">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="7497a-1277">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1277">Method widthMode</span></span>

<span data-ttu-id="7497a-1278">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1278">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="7497a-1279">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1279">Parameters - widthMode</span></span>

<span data-ttu-id="7497a-1280">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1280">value</span></span>  
<span data-ttu-id="7497a-1281">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7497a-1281">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="7497a-1282">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1282">Return Value - widthMode</span></span>

<span data-ttu-id="7497a-1283">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1283">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="7497a-1284">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1284">Remarks - widthMode</span></span>

<span data-ttu-id="7497a-1285">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="7497a-1285">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="7497a-1286">モード。</span><span class="sxs-lookup"><span data-stu-id="7497a-1286">Mode.</span></span>         | <span data-ttu-id="7497a-1287">幅計算。</span><span class="sxs-lookup"><span data-stu-id="7497a-1287">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7497a-1288">正確。</span><span class="sxs-lookup"><span data-stu-id="7497a-1288">Exact.</span></span>        | <span data-ttu-id="7497a-1289">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1289">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7497a-1290">自動。</span><span class="sxs-lookup"><span data-stu-id="7497a-1290">Auto.</span></span>         | <span data-ttu-id="7497a-1291">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1291">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7497a-1292">列の幅。</span><span class="sxs-lookup"><span data-stu-id="7497a-1292">Column width.</span></span> | <span data-ttu-id="7497a-1293">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7497a-1293">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7497a-1294">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7497a-1294">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="7497a-1295">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1295">Method widthValue</span></span>

<span data-ttu-id="7497a-1296">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1296">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="7497a-1297">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1297">Parameters - widthValue</span></span>

<span data-ttu-id="7497a-1298">値</span><span class="sxs-lookup"><span data-stu-id="7497a-1298">value</span></span>  
<span data-ttu-id="7497a-1299">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1299">An Integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="7497a-1300">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1300">Return Value - widthValue</span></span>

<span data-ttu-id="7497a-1301">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="7497a-1301">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="7497a-1302">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7497a-1302">Remarks - widthValue</span></span>

<span data-ttu-id="7497a-1303">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1303">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-prefcolumnsize"></a><span data-ttu-id="7497a-1304">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="7497a-1304">Method prefColumnSize</span></span>

<span data-ttu-id="7497a-1305">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1305">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="7497a-1306">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="7497a-1306">Parameters - prefColumnSize</span></span>

<span data-ttu-id="7497a-1307">width</span><span class="sxs-lookup"><span data-stu-id="7497a-1307">width</span></span>  
<span data-ttu-id="7497a-1308">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="7497a-1308">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="7497a-1309">height</span><span class="sxs-lookup"><span data-stu-id="7497a-1309">height</span></span>  
<span data-ttu-id="7497a-1310">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="7497a-1310">The preferred height of the control.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="7497a-1311">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="7497a-1311">Method lostFocus</span></span>

<span data-ttu-id="7497a-1312">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1312">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="7497a-1313">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="7497a-1313">Method resetUserSetting</span></span>

<span data-ttu-id="7497a-1314">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7497a-1314">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-context"></a><span data-ttu-id="7497a-1315">メソッド context</span><span class="sxs-lookup"><span data-stu-id="7497a-1315">Method context</span></span>

<span data-ttu-id="7497a-1316">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1316">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-drop"></a><span data-ttu-id="7497a-1317">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="7497a-1317">Method drop</span></span>

<span data-ttu-id="7497a-1318">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1318">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="7497a-1319">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="7497a-1319">Parameters - drop</span></span>

<span data-ttu-id="7497a-1320">dragSource</span><span class="sxs-lookup"><span data-stu-id="7497a-1320">dragSource</span></span>  
<span data-ttu-id="7497a-1321">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1321">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-1322">dragMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1322">dragMode</span></span>  
<span data-ttu-id="7497a-1323">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1323">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-1324">x</span><span class="sxs-lookup"><span data-stu-id="7497a-1324">x</span></span>  
<span data-ttu-id="7497a-1325">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1325">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-1326">y</span><span class="sxs-lookup"><span data-stu-id="7497a-1326">y</span></span>  
<span data-ttu-id="7497a-1327">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1327">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="7497a-1328">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="7497a-1328">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="7497a-1329">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="7497a-1329">Parameters - OnLostFocus</span></span>

<span data-ttu-id="7497a-1330">sender</span><span class="sxs-lookup"><span data-stu-id="7497a-1330">sender</span></span>  

<!-- -->

<span data-ttu-id="7497a-1331">e</span><span class="sxs-lookup"><span data-stu-id="7497a-1331">e</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="7497a-1332">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="7497a-1332">Method gotFocus</span></span>

<span data-ttu-id="7497a-1333">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1333">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="7497a-1334">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="7497a-1334">Method mouseEnter</span></span>

<span data-ttu-id="7497a-1335">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1335">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="7497a-1336">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="7497a-1336">Parameters - mouseEnter</span></span>

<span data-ttu-id="7497a-1337">x</span><span class="sxs-lookup"><span data-stu-id="7497a-1337">x</span></span>  
<span data-ttu-id="7497a-1338">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1338">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-1339">y</span><span class="sxs-lookup"><span data-stu-id="7497a-1339">y</span></span>  
<span data-ttu-id="7497a-1340">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1340">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-1341">ボタン</span><span class="sxs-lookup"><span data-stu-id="7497a-1341">button</span></span>  
<span data-ttu-id="7497a-1342">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1342">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-1343">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7497a-1343">Ctrl</span></span>  
<span data-ttu-id="7497a-1344">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1344">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7497a-1345">シフト</span><span class="sxs-lookup"><span data-stu-id="7497a-1345">Shift</span></span>  
<span data-ttu-id="7497a-1346">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1346">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-paste"></a><span data-ttu-id="7497a-1347">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="7497a-1347">Method paste</span></span>

<span data-ttu-id="7497a-1348">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1348">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="7497a-1349">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="7497a-1349">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="7497a-1350">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="7497a-1350">Parameters - OnGotFocus</span></span>

<span data-ttu-id="7497a-1351">sender</span><span class="sxs-lookup"><span data-stu-id="7497a-1351">sender</span></span>  

<!-- -->

<span data-ttu-id="7497a-1352">e</span><span class="sxs-lookup"><span data-stu-id="7497a-1352">e</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="7497a-1353">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="7497a-1353">Method endDrag</span></span>

<span data-ttu-id="7497a-1354">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1354">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="7497a-1355">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="7497a-1355">Remarks - endDrag</span></span>

<span data-ttu-id="7497a-1356">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="7497a-1356">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="7497a-1357">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1357">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-cut"></a><span data-ttu-id="7497a-1358">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="7497a-1358">Method cut</span></span>

<span data-ttu-id="7497a-1359">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="7497a-1359">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-filter"></a><span data-ttu-id="7497a-1360">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="7497a-1360">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="7497a-1361">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="7497a-1361">Parameters - filter</span></span>

<span data-ttu-id="7497a-1362">filterStr</span><span class="sxs-lookup"><span data-stu-id="7497a-1362">filterStr</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="7497a-1363">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="7497a-1363">Method displayControl</span></span>

<span data-ttu-id="7497a-1364">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1364">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-inputsearch"></a><span data-ttu-id="7497a-1365">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="7497a-1365">Method inputSearch</span></span>

<span data-ttu-id="7497a-1366">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1366">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="7497a-1367">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="7497a-1367">Parameters - inputSearch</span></span>

<span data-ttu-id="7497a-1368">searchStr</span><span class="sxs-lookup"><span data-stu-id="7497a-1368">searchStr</span></span>  
<span data-ttu-id="7497a-1369">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7497a-1369">The string value to use to filter data; optional.</span></span>

## <a name="method-copy"></a><span data-ttu-id="7497a-1370">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="7497a-1370">Method copy</span></span>

<span data-ttu-id="7497a-1371">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7497a-1371">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-clicked"></a><span data-ttu-id="7497a-1372">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="7497a-1372">Method clicked</span></span>

```xpp
public void clicked()
```

## <a name="method-onclicked"></a><span data-ttu-id="7497a-1373">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="7497a-1373">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="7497a-1374">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="7497a-1374">Parameters - OnClicked</span></span>

<span data-ttu-id="7497a-1375">sender</span><span class="sxs-lookup"><span data-stu-id="7497a-1375">sender</span></span>  

<!-- -->

<span data-ttu-id="7497a-1376">e</span><span class="sxs-lookup"><span data-stu-id="7497a-1376">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="7497a-1377">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="7497a-1377">Method dropEx</span></span>

<span data-ttu-id="7497a-1378">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1378">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="7497a-1379">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="7497a-1379">Parameters - dropEx</span></span>

<span data-ttu-id="7497a-1380">dragSource</span><span class="sxs-lookup"><span data-stu-id="7497a-1380">dragSource</span></span>  
<span data-ttu-id="7497a-1381">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1381">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-1382">dragMode</span><span class="sxs-lookup"><span data-stu-id="7497a-1382">dragMode</span></span>  
<span data-ttu-id="7497a-1383">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1383">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-1384">x</span><span class="sxs-lookup"><span data-stu-id="7497a-1384">x</span></span>  
<span data-ttu-id="7497a-1385">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1385">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7497a-1386">y</span><span class="sxs-lookup"><span data-stu-id="7497a-1386">y</span></span>  
<span data-ttu-id="7497a-1387">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7497a-1387">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="7497a-1388">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="7497a-1388">Method mouseLeave</span></span>

<span data-ttu-id="7497a-1389">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1389">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-setfocus"></a><span data-ttu-id="7497a-1390">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="7497a-1390">Method setFocus</span></span>

<span data-ttu-id="7497a-1391">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="7497a-1391">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-dragleave"></a><span data-ttu-id="7497a-1392">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="7497a-1392">Method dragLeave</span></span>

<span data-ttu-id="7497a-1393">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7497a-1393">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-jumpref"></a><span data-ttu-id="7497a-1394">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="7497a-1394">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="7497a-1395">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="7497a-1395">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="7497a-1396">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="7497a-1396">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="7497a-1397">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="7497a-1397">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="7497a-1398">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="7497a-1398">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="7497a-1399">overrideObject</span><span class="sxs-lookup"><span data-stu-id="7497a-1399">overrideObject</span></span>  

