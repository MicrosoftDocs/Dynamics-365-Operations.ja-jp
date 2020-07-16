---
title: FormCommandButtonControl クラス
description: このトピックでは、FormCommandButtonControl クラスについて説明します。
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
ms.openlocfilehash: 02e8fbab965cc0155111ce25af80f077ca353dff
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502949"
---
# <a name="class-formcommandbuttoncontrol"></a><span data-ttu-id="f3f29-103">クラス FormCommandButtonControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-103">Class FormCommandButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormCommandButtonControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="f3f29-104">備考</span><span class="sxs-lookup"><span data-stu-id="f3f29-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f3f29-105">例</span><span class="sxs-lookup"><span data-stu-id="f3f29-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f3f29-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="f3f29-106">Methods</span></span>

| <span data-ttu-id="f3f29-107">方法</span><span class="sxs-lookup"><span data-stu-id="f3f29-107">Method</span></span>                                                                                                      | <span data-ttu-id="f3f29-108">説明</span><span class="sxs-lookup"><span data-stu-id="f3f29-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f29-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="f3f29-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="f3f29-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="f3f29-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="f3f29-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="f3f29-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="f3f29-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="f3f29-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="f3f29-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="f3f29-118">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-118">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="f3f29-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="f3f29-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="f3f29-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="f3f29-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="f3f29-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="f3f29-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="f3f29-125">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-125">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-126">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-126">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="f3f29-127">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-127">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="f3f29-128">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-128">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="f3f29-129">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-129">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="f3f29-130">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-130">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="f3f29-131">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-131">Gets or sets the appearance of the button control.</span></span>                                                                                                                      |
| <span data-ttu-id="f3f29-132">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="f3f29-132">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="f3f29-133">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-133">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="f3f29-134">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-134">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="f3f29-135">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-135">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="f3f29-136">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-136">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="f3f29-137">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-137">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="f3f29-138">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-138">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="f3f29-139">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-139">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="f3f29-140">public int command(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-140">public int command(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-141">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-141">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="f3f29-142">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-142">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="f3f29-143">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="f3f29-143">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="f3f29-144">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-144">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="f3f29-145">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-145">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="f3f29-146">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-146">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="f3f29-147">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-147">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="f3f29-148">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-148">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="f3f29-149">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-149">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="f3f29-150">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-150">Determines whether the button should be the default button in the form.</span></span>                                                                                                 |
| <span data-ttu-id="f3f29-151">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-151">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="f3f29-152">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-152">Gets or sets the disabled image of the button.</span></span>                                                                                                                          |
| <span data-ttu-id="f3f29-153">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-153">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-154">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-154">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="f3f29-155">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-155">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                                          |
| <span data-ttu-id="f3f29-156">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-156">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="f3f29-157">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-157">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="f3f29-158">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-158">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="f3f29-159">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-159">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="f3f29-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="f3f29-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="f3f29-161">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-161">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="f3f29-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="f3f29-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="f3f29-163">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-163">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="f3f29-164">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="f3f29-164">public str dragText()</span></span>                                                                                       | <span data-ttu-id="f3f29-165">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-165">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="f3f29-166">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-166">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="f3f29-167">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-167">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="f3f29-168">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-168">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="f3f29-169">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-169">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="f3f29-170">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-170">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="f3f29-171">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-171">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="f3f29-172">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-172">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-173">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-173">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="f3f29-174">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-174">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="f3f29-175">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-175">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="f3f29-176">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-176">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="f3f29-177">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="f3f29-177">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="f3f29-178">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-178">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="f3f29-179">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-179">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="f3f29-180">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-180">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="f3f29-181">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-181">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="f3f29-182">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-182">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="f3f29-183">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-183">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="f3f29-184">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-184">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="f3f29-185">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="f3f29-185">public str helpField()</span></span>                                                                                      | <span data-ttu-id="f3f29-186">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-186">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="f3f29-187">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-187">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="f3f29-188">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-188">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="f3f29-189">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-189">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="f3f29-190">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-190">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="f3f29-191">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="f3f29-191">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="f3f29-192">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-192">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="f3f29-193">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-193">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-194">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="f3f29-194">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-195">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="f3f29-195">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="f3f29-196">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-196">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="f3f29-197">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="f3f29-197">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="f3f29-198">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-198">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="f3f29-199">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="f3f29-199">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="f3f29-200">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-200">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="f3f29-201">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-201">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-202">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-202">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-203">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-203">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="f3f29-204">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-204">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="f3f29-205">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-205">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="f3f29-206">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-206">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="f3f29-207">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-207">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="f3f29-208">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-208">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="f3f29-209">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-209">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="f3f29-210">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-210">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="f3f29-211">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="f3f29-211">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="f3f29-212">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-212">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="f3f29-213">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="f3f29-213">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="f3f29-214">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-214">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="f3f29-215">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="f3f29-215">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="f3f29-216">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-216">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="f3f29-217">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="f3f29-217">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="f3f29-218">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-218">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="f3f29-219">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-219">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-220">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-220">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="f3f29-221">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-221">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="f3f29-222">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-222">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-223">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-223">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-224">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-224">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-225">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-225">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-226">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="f3f29-226">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-227">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-227">public str parameters(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-228">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="f3f29-228">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="f3f29-229">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-229">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="f3f29-230">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-230">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-231">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-231">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-232">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-232">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="f3f29-233">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-233">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="f3f29-234">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-234">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-235">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="f3f29-235">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="f3f29-236">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-236">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="f3f29-237">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-237">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-238">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-238">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="f3f29-239">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-239">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="f3f29-240">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-240">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-241">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-241">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-242">public int toggleButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-242">public int toggleButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-243">public int toggleValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-243">public int toggleValue(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-244">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="f3f29-244">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="f3f29-245">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-245">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="f3f29-246">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-246">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="f3f29-247">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-247">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="f3f29-248">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-248">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="f3f29-249">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-249">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="f3f29-250">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-250">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="f3f29-251">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-251">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="f3f29-252">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-252">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-253">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-253">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="f3f29-254">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-254">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="f3f29-255">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="f3f29-255">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-256">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-256">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="f3f29-257">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-257">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="f3f29-258">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-258">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="f3f29-259">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-259">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="f3f29-260">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-260">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="f3f29-261">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-261">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="f3f29-262">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-262">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="f3f29-263">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-263">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="f3f29-264">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-264">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="f3f29-265">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-265">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="f3f29-266">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-266">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="f3f29-267">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-267">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="f3f29-268">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-268">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="f3f29-269">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-269">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="f3f29-270">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-270">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="f3f29-271">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-271">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="f3f29-272">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-272">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="f3f29-273">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-273">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="f3f29-274">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-274">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="f3f29-275">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-275">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="f3f29-276">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-276">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="f3f29-277">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-277">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="f3f29-278">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-278">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="f3f29-279">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-279">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="f3f29-280">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-280">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-281">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-281">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="f3f29-282">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-282">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="f3f29-283">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-283">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="f3f29-284">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-284">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="f3f29-285">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-285">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="f3f29-286">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-286">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="f3f29-287">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-287">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="f3f29-288">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-288">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="f3f29-289">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-289">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="f3f29-290">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-290">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="f3f29-291">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-291">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="f3f29-292">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-292">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="f3f29-293">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-293">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="f3f29-294">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-294">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="f3f29-295">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-295">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-296">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="f3f29-296">public void displayControl()</span></span>                                                                                | <span data-ttu-id="f3f29-297">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-297">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="f3f29-298">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="f3f29-298">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="f3f29-299">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-299">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="f3f29-300">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="f3f29-300">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="f3f29-301">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-301">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="f3f29-302">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-302">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-303">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="f3f29-303">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="f3f29-304">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-304">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="f3f29-305">public void cut()</span><span class="sxs-lookup"><span data-stu-id="f3f29-305">public void cut()</span></span>                                                                                           | <span data-ttu-id="f3f29-306">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-306">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="f3f29-307">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="f3f29-307">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="f3f29-308">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-308">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="f3f29-309">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="f3f29-309">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="f3f29-310">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-310">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="f3f29-311">public void paste()</span><span class="sxs-lookup"><span data-stu-id="f3f29-311">public void paste()</span></span>                                                                                         | <span data-ttu-id="f3f29-312">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-312">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="f3f29-313">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="f3f29-313">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="f3f29-314">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-314">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="f3f29-315">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="f3f29-315">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="f3f29-316">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-316">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="f3f29-317">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="f3f29-317">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="f3f29-318">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-318">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="f3f29-319">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="f3f29-319">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="f3f29-320">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-320">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="f3f29-321">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="f3f29-321">public void clicked()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-322">public void copy()</span><span class="sxs-lookup"><span data-stu-id="f3f29-322">public void copy()</span></span>                                                                                          | <span data-ttu-id="f3f29-323">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-323">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="f3f29-324">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="f3f29-324">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="f3f29-325">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-325">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="f3f29-326">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="f3f29-326">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="f3f29-327">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-327">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="f3f29-328">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-328">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="f3f29-329">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="f3f29-329">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="f3f29-330">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-330">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="f3f29-331">public void context()</span><span class="sxs-lookup"><span data-stu-id="f3f29-331">public void context()</span></span>                                                                                       | <span data-ttu-id="f3f29-332">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-332">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="f3f29-333">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="f3f29-333">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="f3f29-334">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-334">Method alignControl</span></span>

<span data-ttu-id="f3f29-335">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-335">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="f3f29-336">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-336">Parameters - alignControl</span></span>

<span data-ttu-id="f3f29-337">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-337">value</span></span>  
<span data-ttu-id="f3f29-338">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-338">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="f3f29-339">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-339">Return Value - alignControl</span></span>

<span data-ttu-id="f3f29-340">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-340">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="f3f29-341">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-341">Remarks - alignControl</span></span>

<span data-ttu-id="f3f29-342">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-342">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="f3f29-343">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="f3f29-343">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="f3f29-344">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="f3f29-344">Parameters - alignment</span></span>

<span data-ttu-id="f3f29-345">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-345">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="f3f29-346">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="f3f29-346">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="f3f29-347">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="f3f29-347">Method allowEdit</span></span>

<span data-ttu-id="f3f29-348">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-348">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="f3f29-349">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="f3f29-349">Parameters - allowEdit</span></span>

<span data-ttu-id="f3f29-350">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-350">value</span></span>  
<span data-ttu-id="f3f29-351">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-351">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="f3f29-352">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="f3f29-352">Return Value - allowEdit</span></span>

<span data-ttu-id="f3f29-353">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-353">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="f3f29-354">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="f3f29-354">Remarks - allowEdit</span></span>

<span data-ttu-id="f3f29-355">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-355">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="f3f29-356">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="f3f29-356">Method allowSysSetup</span></span>

<span data-ttu-id="f3f29-357">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-357">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="f3f29-358">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="f3f29-358">Return Value - allowSysSetup</span></span>

<span data-ttu-id="f3f29-359">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-359">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="f3f29-360">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f3f29-360">Method autoDeclaration</span></span>

<span data-ttu-id="f3f29-361">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-361">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="f3f29-362">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f3f29-362">Parameters - autoDeclaration</span></span>

<span data-ttu-id="f3f29-363">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-363">value</span></span>  
<span data-ttu-id="f3f29-364">指定されている場合、プロパティはこの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-364">If specified, the property is set to this value.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="f3f29-365">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f3f29-365">Return Value - autoDeclaration</span></span>

<span data-ttu-id="f3f29-366">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-366">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="f3f29-367">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f3f29-367">Remarks - autoDeclaration</span></span>

<span data-ttu-id="f3f29-368">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-368">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="f3f29-369">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="f3f29-369">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="f3f29-370">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="f3f29-370">Parameters - autoRefreshData</span></span>

<span data-ttu-id="f3f29-371">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-371">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="f3f29-372">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="f3f29-372">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="f3f29-373">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-373">Method backgroundColor</span></span>

<span data-ttu-id="f3f29-374">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-374">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="f3f29-375">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-375">Parameters - backgroundColor</span></span>

<span data-ttu-id="f3f29-376">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-376">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="f3f29-377">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-377">Return Value - backgroundColor</span></span>

<span data-ttu-id="f3f29-378">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-378">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="f3f29-379">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-379">Remarks - backgroundColor</span></span>

<span data-ttu-id="f3f29-380">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-380">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="f3f29-381">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-381">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="f3f29-382">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-382">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="f3f29-383">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-383">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="f3f29-384">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-384">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="f3f29-385">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-385">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="f3f29-386">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="f3f29-386">Method backStyle</span></span>

<span data-ttu-id="f3f29-387">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-387">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="f3f29-388">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="f3f29-388">Parameters - backStyle</span></span>

<span data-ttu-id="f3f29-389">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-389">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="f3f29-390">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="f3f29-390">Return Value - backStyle</span></span>

<span data-ttu-id="f3f29-391">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-391">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="f3f29-392">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="f3f29-392">Method beginDrag</span></span>

<span data-ttu-id="f3f29-393">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-393">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="f3f29-394">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="f3f29-394">Parameters - beginDrag</span></span>

<span data-ttu-id="f3f29-395">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-395">x</span></span>  
<span data-ttu-id="f3f29-396">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-396">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="f3f29-397">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-397">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="f3f29-398">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-398">y</span></span>  
<span data-ttu-id="f3f29-399">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-399">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="f3f29-400">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-400">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="f3f29-401">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="f3f29-401">Return Value - beginDrag</span></span>

<span data-ttu-id="f3f29-402">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-402">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="f3f29-403">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="f3f29-403">Remarks - beginDrag</span></span>

<span data-ttu-id="f3f29-404">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-404">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="f3f29-405">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-405">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-big"></a><span data-ttu-id="f3f29-406">メソッド big</span><span class="sxs-lookup"><span data-stu-id="f3f29-406">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="f3f29-407">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="f3f29-407">Parameters - big</span></span>

<span data-ttu-id="f3f29-408">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-408">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="f3f29-409">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="f3f29-409">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="f3f29-410">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="f3f29-410">Method bold</span></span>

<span data-ttu-id="f3f29-411">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-411">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="f3f29-412">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="f3f29-412">Parameters - bold</span></span>

<span data-ttu-id="f3f29-413">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-413">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="f3f29-414">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="f3f29-414">Return Value - bold</span></span>

<span data-ttu-id="f3f29-415">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-415">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="f3f29-416">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="f3f29-416">Remarks - bold</span></span>

<span data-ttu-id="f3f29-417">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-417">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="f3f29-418">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-418">0 Use the default font weight.</span></span>
-   <span data-ttu-id="f3f29-419">1 シン。</span><span class="sxs-lookup"><span data-stu-id="f3f29-419">1 Thin.</span></span>
-   <span data-ttu-id="f3f29-420">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="f3f29-420">2 Extra-light.</span></span>
-   <span data-ttu-id="f3f29-421">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="f3f29-421">3 Light.</span></span>
-   <span data-ttu-id="f3f29-422">4 標準。</span><span class="sxs-lookup"><span data-stu-id="f3f29-422">4 Normal.</span></span>
-   <span data-ttu-id="f3f29-423">5 中。</span><span class="sxs-lookup"><span data-stu-id="f3f29-423">5 Medium.</span></span>
-   <span data-ttu-id="f3f29-424">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="f3f29-424">6 Semibold.</span></span>
-   <span data-ttu-id="f3f29-425">7 太字。</span><span class="sxs-lookup"><span data-stu-id="f3f29-425">7 Bold.</span></span>
-   <span data-ttu-id="f3f29-426">8 極太。</span><span class="sxs-lookup"><span data-stu-id="f3f29-426">8 Extra-bold.</span></span>
-   <span data-ttu-id="f3f29-427">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="f3f29-427">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="f3f29-428">メソッド border</span><span class="sxs-lookup"><span data-stu-id="f3f29-428">Method border</span></span>

<span data-ttu-id="f3f29-429">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-429">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="f3f29-430">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="f3f29-430">Parameters - border</span></span>

<span data-ttu-id="f3f29-431">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-431">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="f3f29-432">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="f3f29-432">Return Value - border</span></span>

<span data-ttu-id="f3f29-433">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-433">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="f3f29-434">備考 - border</span><span class="sxs-lookup"><span data-stu-id="f3f29-434">Remarks - border</span></span>

<span data-ttu-id="f3f29-435">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-435">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="f3f29-436">値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-436">Value.</span></span> | <span data-ttu-id="f3f29-437">説明。</span><span class="sxs-lookup"><span data-stu-id="f3f29-437">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="f3f29-438">0</span><span class="sxs-lookup"><span data-stu-id="f3f29-438">0</span></span>      | <span data-ttu-id="f3f29-439">自動。</span><span class="sxs-lookup"><span data-stu-id="f3f29-439">Auto.</span></span>        |
| <span data-ttu-id="f3f29-440">1</span><span class="sxs-lookup"><span data-stu-id="f3f29-440">1</span></span>      | <span data-ttu-id="f3f29-441">3D。</span><span class="sxs-lookup"><span data-stu-id="f3f29-441">3D.</span></span>          |
| <span data-ttu-id="f3f29-442">2</span><span class="sxs-lookup"><span data-stu-id="f3f29-442">2</span></span>      | <span data-ttu-id="f3f29-443">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="f3f29-443">Single line.</span></span> |
| <span data-ttu-id="f3f29-444">3</span><span class="sxs-lookup"><span data-stu-id="f3f29-444">3</span></span>      | <span data-ttu-id="f3f29-445">均一。</span><span class="sxs-lookup"><span data-stu-id="f3f29-445">Flat.</span></span>        |
| <span data-ttu-id="f3f29-446">4</span><span class="sxs-lookup"><span data-stu-id="f3f29-446">4</span></span>      | <span data-ttu-id="f3f29-447">なし。</span><span class="sxs-lookup"><span data-stu-id="f3f29-447">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="f3f29-448">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="f3f29-448">Method buttonDisplay</span></span>

<span data-ttu-id="f3f29-449">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-449">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="f3f29-450">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="f3f29-450">Parameters - buttonDisplay</span></span>

<span data-ttu-id="f3f29-451">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-451">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="f3f29-452">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="f3f29-452">Return Value - buttonDisplay</span></span>

<span data-ttu-id="f3f29-453">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-453">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="f3f29-454">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="f3f29-454">Remarks - buttonDisplay</span></span>

<span data-ttu-id="f3f29-455">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-455">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="f3f29-456">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-456">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="f3f29-457">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-457">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="f3f29-458">値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-458">Value.</span></span> | <span data-ttu-id="f3f29-459">説明。</span><span class="sxs-lookup"><span data-stu-id="f3f29-459">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="f3f29-460">0</span><span class="sxs-lookup"><span data-stu-id="f3f29-460">0</span></span>      | <span data-ttu-id="f3f29-461">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-461">Text only.</span></span>                                                       |
| <span data-ttu-id="f3f29-462">1</span><span class="sxs-lookup"><span data-stu-id="f3f29-462">1</span></span>      | <span data-ttu-id="f3f29-463">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-463">Image Only.</span></span>                                                      |
| <span data-ttu-id="f3f29-464">2</span><span class="sxs-lookup"><span data-stu-id="f3f29-464">2</span></span>      | <span data-ttu-id="f3f29-465">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-465">Text and image; the image is displayed below the text.</span></span>           |
| <span data-ttu-id="f3f29-466">3</span><span class="sxs-lookup"><span data-stu-id="f3f29-466">3</span></span>      | <span data-ttu-id="f3f29-467">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-467">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="f3f29-468">4</span><span class="sxs-lookup"><span data-stu-id="f3f29-468">4</span></span>      | <span data-ttu-id="f3f29-469">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-469">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="f3f29-470">5</span><span class="sxs-lookup"><span data-stu-id="f3f29-470">5</span></span>      | <span data-ttu-id="f3f29-471">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-471">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-calccontrolsize"></a><span data-ttu-id="f3f29-472">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-472">Method calcControlSize</span></span>

<span data-ttu-id="f3f29-473">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-473">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="f3f29-474">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-474">Parameters - calcControlSize</span></span>

<span data-ttu-id="f3f29-475">chars</span><span class="sxs-lookup"><span data-stu-id="f3f29-475">chars</span></span>  
<span data-ttu-id="f3f29-476">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-476">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="f3f29-477">明細行</span><span class="sxs-lookup"><span data-stu-id="f3f29-477">lines</span></span>  
<span data-ttu-id="f3f29-478">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-478">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="f3f29-479">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-479">Return Value - calcControlSize</span></span>

<span data-ttu-id="f3f29-480">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="f3f29-480">The container that holds the width and height.</span></span>

## <a name="method-caption"></a><span data-ttu-id="f3f29-481">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="f3f29-481">Method caption</span></span>

<span data-ttu-id="f3f29-482">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-482">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="f3f29-483">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="f3f29-483">Parameters - caption</span></span>

<span data-ttu-id="f3f29-484">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-484">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="f3f29-485">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="f3f29-485">Return Value - caption</span></span>

<span data-ttu-id="f3f29-486">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="f3f29-486">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="f3f29-487">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="f3f29-487">Method characterSet</span></span>

<span data-ttu-id="f3f29-488">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-488">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="f3f29-489">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="f3f29-489">Parameters - characterSet</span></span>

<span data-ttu-id="f3f29-490">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-490">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="f3f29-491">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="f3f29-491">Return Value - characterSet</span></span>

<span data-ttu-id="f3f29-492">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-492">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="f3f29-493">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="f3f29-493">Remarks - characterSet</span></span>

<span data-ttu-id="f3f29-494">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-494">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="f3f29-495">値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-495">Value.</span></span> | <span data-ttu-id="f3f29-496">説明。</span><span class="sxs-lookup"><span data-stu-id="f3f29-496">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="f3f29-497">0</span><span class="sxs-lookup"><span data-stu-id="f3f29-497">0</span></span>      | <span data-ttu-id="f3f29-498">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-498">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="f3f29-499">1</span><span class="sxs-lookup"><span data-stu-id="f3f29-499">1</span></span>      | <span data-ttu-id="f3f29-500">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-500">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="f3f29-501">2</span><span class="sxs-lookup"><span data-stu-id="f3f29-501">2</span></span>      | <span data-ttu-id="f3f29-502">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-502">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="f3f29-503">77</span><span class="sxs-lookup"><span data-stu-id="f3f29-503">77</span></span>     | <span data-ttu-id="f3f29-504">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-504">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="f3f29-505">128</span><span class="sxs-lookup"><span data-stu-id="f3f29-505">128</span></span>    | <span data-ttu-id="f3f29-506">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-506">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="f3f29-507">129</span><span class="sxs-lookup"><span data-stu-id="f3f29-507">129</span></span>    | <span data-ttu-id="f3f29-508">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-508">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="f3f29-509">134</span><span class="sxs-lookup"><span data-stu-id="f3f29-509">134</span></span>    | <span data-ttu-id="f3f29-510">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-510">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="f3f29-511">136</span><span class="sxs-lookup"><span data-stu-id="f3f29-511">136</span></span>    | <span data-ttu-id="f3f29-512">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-512">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="f3f29-513">161</span><span class="sxs-lookup"><span data-stu-id="f3f29-513">161</span></span>    | <span data-ttu-id="f3f29-514">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-514">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="f3f29-515">162</span><span class="sxs-lookup"><span data-stu-id="f3f29-515">162</span></span>    | <span data-ttu-id="f3f29-516">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-516">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="f3f29-517">163</span><span class="sxs-lookup"><span data-stu-id="f3f29-517">163</span></span>    | <span data-ttu-id="f3f29-518">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-518">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="f3f29-519">186</span><span class="sxs-lookup"><span data-stu-id="f3f29-519">186</span></span>    | <span data-ttu-id="f3f29-520">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-520">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="f3f29-521">204</span><span class="sxs-lookup"><span data-stu-id="f3f29-521">204</span></span>    | <span data-ttu-id="f3f29-522">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-522">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="f3f29-523">238</span><span class="sxs-lookup"><span data-stu-id="f3f29-523">238</span></span>    | <span data-ttu-id="f3f29-524">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-524">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="f3f29-525">255</span><span class="sxs-lookup"><span data-stu-id="f3f29-525">255</span></span>    | <span data-ttu-id="f3f29-526">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-526">OEM\_CHARSET</span></span>         |

<span data-ttu-id="f3f29-527">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-527">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="f3f29-528">値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-528">Value.</span></span> | <span data-ttu-id="f3f29-529">説明。</span><span class="sxs-lookup"><span data-stu-id="f3f29-529">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="f3f29-530">130</span><span class="sxs-lookup"><span data-stu-id="f3f29-530">130</span></span>    | <span data-ttu-id="f3f29-531">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-531">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="f3f29-532">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-532">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="f3f29-533">値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-533">Value.</span></span> | <span data-ttu-id="f3f29-534">説明。</span><span class="sxs-lookup"><span data-stu-id="f3f29-534">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="f3f29-535">177</span><span class="sxs-lookup"><span data-stu-id="f3f29-535">177</span></span>    | <span data-ttu-id="f3f29-536">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-536">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="f3f29-537">178</span><span class="sxs-lookup"><span data-stu-id="f3f29-537">178</span></span>    | <span data-ttu-id="f3f29-538">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-538">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="f3f29-539">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-539">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="f3f29-540">値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-540">Value.</span></span> | <span data-ttu-id="f3f29-541">説明。</span><span class="sxs-lookup"><span data-stu-id="f3f29-541">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="f3f29-542">222</span><span class="sxs-lookup"><span data-stu-id="f3f29-542">222</span></span>    | <span data-ttu-id="f3f29-543">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f3f29-543">THAI\_CHARSET</span></span> |

<span data-ttu-id="f3f29-544">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-544">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="f3f29-545">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-545">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="f3f29-546">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3f29-546">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="f3f29-547">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="f3f29-547">Method colorScheme</span></span>

<span data-ttu-id="f3f29-548">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-548">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="f3f29-549">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f3f29-549">Parameters - colorScheme</span></span>

<span data-ttu-id="f3f29-550">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-550">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="f3f29-551">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f3f29-551">Return Value - colorScheme</span></span>

<span data-ttu-id="f3f29-552">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-552">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="f3f29-553">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f3f29-553">Remarks - colorScheme</span></span>

<span data-ttu-id="f3f29-554">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-554">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="f3f29-555">値です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-555">Value.</span></span> | <span data-ttu-id="f3f29-556">スタイル。</span><span class="sxs-lookup"><span data-stu-id="f3f29-556">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="f3f29-557">0</span><span class="sxs-lookup"><span data-stu-id="f3f29-557">0</span></span>      | <span data-ttu-id="f3f29-558">既定。</span><span class="sxs-lookup"><span data-stu-id="f3f29-558">Default.</span></span>                       |
| <span data-ttu-id="f3f29-559">1</span><span class="sxs-lookup"><span data-stu-id="f3f29-559">1</span></span>      | <span data-ttu-id="f3f29-560">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="f3f29-560">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="f3f29-561">2</span><span class="sxs-lookup"><span data-stu-id="f3f29-561">2</span></span>      | <span data-ttu-id="f3f29-562">真の配色。</span><span class="sxs-lookup"><span data-stu-id="f3f29-562">The true-color scheme.</span></span>         |

## <a name="method-command"></a><span data-ttu-id="f3f29-563">メソッド command</span><span class="sxs-lookup"><span data-stu-id="f3f29-563">Method command</span></span>

```xpp
public int command([int value])
```

### <a name="parameters---command"></a><span data-ttu-id="f3f29-564">パラメーター - command</span><span class="sxs-lookup"><span data-stu-id="f3f29-564">Parameters - command</span></span>

<span data-ttu-id="f3f29-565">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-565">value</span></span>  

### <a name="return-value---command"></a><span data-ttu-id="f3f29-566">戻り値 - command</span><span class="sxs-lookup"><span data-stu-id="f3f29-566">Return Value - command</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="f3f29-567">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="f3f29-567">Method configurationKey</span></span>

<span data-ttu-id="f3f29-568">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-568">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="f3f29-569">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f3f29-569">Parameters - configurationKey</span></span>

<span data-ttu-id="f3f29-570">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-570">value</span></span>  
<span data-ttu-id="f3f29-571">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-571">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="f3f29-572">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f3f29-572">Return Value - configurationKey</span></span>

<span data-ttu-id="f3f29-573">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="f3f29-573">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="f3f29-574">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f3f29-574">Remarks - configurationKey</span></span>

<span data-ttu-id="f3f29-575">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-575">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="f3f29-576">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-576">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="f3f29-577">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-577">Method configurationKeyEx</span></span>

<span data-ttu-id="f3f29-578">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-578">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="f3f29-579">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-579">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="f3f29-580">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="f3f29-580">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="f3f29-581">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-581">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="f3f29-582">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-582">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="f3f29-583">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-583">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="f3f29-584">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-584">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="f3f29-585">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f3f29-585">Method countryRegionCodes</span></span>

<span data-ttu-id="f3f29-586">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-586">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="f3f29-587">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f3f29-587">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="f3f29-588">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-588">value</span></span>  
<span data-ttu-id="f3f29-589">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-589">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="f3f29-590">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f3f29-590">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="f3f29-591">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="f3f29-591">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="f3f29-592">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="f3f29-592">Method dataRelationPath</span></span>

<span data-ttu-id="f3f29-593">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-593">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="f3f29-594">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="f3f29-594">Parameters - dataRelationPath</span></span>

<span data-ttu-id="f3f29-595">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-595">value</span></span>  
<span data-ttu-id="f3f29-596">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-596">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="f3f29-597">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="f3f29-597">Return Value - dataRelationPath</span></span>

<span data-ttu-id="f3f29-598">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="f3f29-598">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="f3f29-599">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="f3f29-599">Remarks - dataRelationPath</span></span>

<span data-ttu-id="f3f29-600">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-600">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="f3f29-601">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="f3f29-601">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="f3f29-602">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="f3f29-602">Method defaultButton</span></span>

<span data-ttu-id="f3f29-603">ボタンをフォームの既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-603">Determines whether the button should be the default button in the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="f3f29-604">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="f3f29-604">Parameters - defaultButton</span></span>

<span data-ttu-id="f3f29-605">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-605">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="f3f29-606">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="f3f29-606">Return Value - defaultButton</span></span>

<span data-ttu-id="f3f29-607">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-607">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="f3f29-608">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="f3f29-608">Method disabledImage</span></span>

<span data-ttu-id="f3f29-609">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-609">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="f3f29-610">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="f3f29-610">Parameters - disabledImage</span></span>

<span data-ttu-id="f3f29-611">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-611">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="f3f29-612">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="f3f29-612">Return Value - disabledImage</span></span>

<span data-ttu-id="f3f29-613">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="f3f29-613">The full name of an image file.</span></span> <span data-ttu-id="f3f29-614">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-614">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="f3f29-615">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="f3f29-615">Remarks - disabledImage</span></span>

<span data-ttu-id="f3f29-616">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-616">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="f3f29-617">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-617">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="f3f29-618">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="f3f29-618">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="f3f29-619">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="f3f29-619">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="f3f29-620">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-620">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="f3f29-621">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="f3f29-621">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="f3f29-622">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="f3f29-622">Method disabledResource</span></span>

<span data-ttu-id="f3f29-623">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-623">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="f3f29-624">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="f3f29-624">Parameters - disabledResource</span></span>

<span data-ttu-id="f3f29-625">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-625">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="f3f29-626">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="f3f29-626">Return Value - disabledResource</span></span>

<span data-ttu-id="f3f29-627">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="f3f29-627">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="f3f29-628">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-628">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="f3f29-629">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="f3f29-629">Method displayTarget</span></span>

<span data-ttu-id="f3f29-630">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-630">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="f3f29-631">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="f3f29-631">Parameters - displayTarget</span></span>

<span data-ttu-id="f3f29-632">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-632">value</span></span>  
<span data-ttu-id="f3f29-633">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-633">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="f3f29-634">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="f3f29-634">Return Value - displayTarget</span></span>

<span data-ttu-id="f3f29-635">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-635">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="f3f29-636">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="f3f29-636">Method dragDrop</span></span>

<span data-ttu-id="f3f29-637">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-637">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="f3f29-638">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="f3f29-638">Parameters - dragDrop</span></span>

<span data-ttu-id="f3f29-639">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-639">value</span></span>  
<span data-ttu-id="f3f29-640">ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-640">An Integer data type that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="f3f29-641">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="f3f29-641">Return Value - dragDrop</span></span>

<span data-ttu-id="f3f29-642">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-642">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="f3f29-643">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="f3f29-643">Remarks - dragDrop</span></span>

<span data-ttu-id="f3f29-644">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-644">Use the dragLeave, the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="f3f29-645">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="f3f29-645">Method dragOver</span></span>

<span data-ttu-id="f3f29-646">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-646">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="f3f29-647">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="f3f29-647">Parameters - dragOver</span></span>

<span data-ttu-id="f3f29-648">dragSource</span><span class="sxs-lookup"><span data-stu-id="f3f29-648">dragSource</span></span>  
<span data-ttu-id="f3f29-649">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-649">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-650">dragMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-650">dragMode</span></span>  
<span data-ttu-id="f3f29-651">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-651">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-652">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-652">x</span></span>  
<span data-ttu-id="f3f29-653">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-653">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-654">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-654">y</span></span>  
<span data-ttu-id="f3f29-655">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-655">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="f3f29-656">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="f3f29-656">Return Value - dragOver</span></span>

<span data-ttu-id="f3f29-657">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-657">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="f3f29-658">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-658">Method dragOverEx</span></span>

<span data-ttu-id="f3f29-659">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-659">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="f3f29-660">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-660">Parameters - dragOverEx</span></span>

<span data-ttu-id="f3f29-661">dragSource</span><span class="sxs-lookup"><span data-stu-id="f3f29-661">dragSource</span></span>  
<span data-ttu-id="f3f29-662">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-662">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-663">dragMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-663">dragMode</span></span>  
<span data-ttu-id="f3f29-664">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-664">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-665">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-665">x</span></span>  
<span data-ttu-id="f3f29-666">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-666">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-667">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-667">y</span></span>  
<span data-ttu-id="f3f29-668">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-668">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="f3f29-669">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-669">Return Value - dragOverEx</span></span>

<span data-ttu-id="f3f29-670">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-670">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="f3f29-671">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="f3f29-671">Method dragText</span></span>

<span data-ttu-id="f3f29-672">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-672">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="f3f29-673">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="f3f29-673">Return Value - dragText</span></span>

<span data-ttu-id="f3f29-674">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="f3f29-674">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="f3f29-675">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-675">Method enabled</span></span>

<span data-ttu-id="f3f29-676">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-676">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="f3f29-677">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-677">Parameters - enabled</span></span>

<span data-ttu-id="f3f29-678">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-678">value</span></span>  
<span data-ttu-id="f3f29-679">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-679">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="f3f29-680">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-680">Return Value - enabled</span></span>

<span data-ttu-id="f3f29-681">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-681">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="f3f29-682">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-682">Remarks - enabled</span></span>

<span data-ttu-id="f3f29-683">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-683">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="f3f29-684">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-684">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="f3f29-685">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-685">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="f3f29-686">メソッド font</span><span class="sxs-lookup"><span data-stu-id="f3f29-686">Method font</span></span>

<span data-ttu-id="f3f29-687">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-687">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="f3f29-688">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="f3f29-688">Parameters - font</span></span>

<span data-ttu-id="f3f29-689">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-689">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="f3f29-690">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="f3f29-690">Return Value - font</span></span>

<span data-ttu-id="f3f29-691">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="f3f29-691">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="f3f29-692">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-692">Method fontSize</span></span>

<span data-ttu-id="f3f29-693">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-693">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="f3f29-694">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-694">Parameters - fontSize</span></span>

<span data-ttu-id="f3f29-695">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-695">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="f3f29-696">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-696">Return Value - fontSize</span></span>

<span data-ttu-id="f3f29-697">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-697">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="f3f29-698">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="f3f29-698">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="f3f29-699">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="f3f29-699">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="f3f29-700">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-700">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="f3f29-701">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="f3f29-701">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="f3f29-702">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-702">Method foregroundColor</span></span>

<span data-ttu-id="f3f29-703">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-703">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="f3f29-704">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-704">Parameters - foregroundColor</span></span>

<span data-ttu-id="f3f29-705">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-705">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="f3f29-706">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-706">Return Value - foregroundColor</span></span>

<span data-ttu-id="f3f29-707">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-707">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="f3f29-708">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f3f29-708">Remarks - foregroundColor</span></span>

<span data-ttu-id="f3f29-709">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-709">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="f3f29-710">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-710">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="f3f29-711">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-711">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="f3f29-712">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f3f29-712">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="f3f29-713">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-713">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="f3f29-714">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-714">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="f3f29-715">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="f3f29-715">Method hasChanged</span></span>

<span data-ttu-id="f3f29-716">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-716">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="f3f29-717">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="f3f29-717">Parameters - hasChanged</span></span>

<span data-ttu-id="f3f29-718">val</span><span class="sxs-lookup"><span data-stu-id="f3f29-718">val</span></span>  
<span data-ttu-id="f3f29-719">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-719">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="f3f29-720">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="f3f29-720">Return Value - hasChanged</span></span>

<span data-ttu-id="f3f29-721">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-721">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="f3f29-722">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="f3f29-722">Method hasUserSetting</span></span>

<span data-ttu-id="f3f29-723">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-723">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="f3f29-724">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="f3f29-724">Return Value - hasUserSetting</span></span>

<span data-ttu-id="f3f29-725">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-725">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="f3f29-726">メソッド height</span><span class="sxs-lookup"><span data-stu-id="f3f29-726">Method height</span></span>

<span data-ttu-id="f3f29-727">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-727">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="f3f29-728">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="f3f29-728">Parameters - height</span></span>

<span data-ttu-id="f3f29-729">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-729">value</span></span>  
<span data-ttu-id="f3f29-730">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="f3f29-730">An Integer data type that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="f3f29-731">モード</span><span class="sxs-lookup"><span data-stu-id="f3f29-731">mode</span></span>  
<span data-ttu-id="f3f29-732">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="f3f29-732">An Integer data type that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="f3f29-733">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="f3f29-733">Return Value - height</span></span>

<span data-ttu-id="f3f29-734">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-734">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="f3f29-735">備考 - height</span><span class="sxs-lookup"><span data-stu-id="f3f29-735">Remarks - height</span></span>

<span data-ttu-id="f3f29-736">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-736">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="f3f29-737">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="f3f29-737">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="f3f29-738">モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-738">Mode.</span></span>            | <span data-ttu-id="f3f29-739">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="f3f29-739">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f29-740">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="f3f29-740">-1 Exact.</span></span>        | <span data-ttu-id="f3f29-741">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-741">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f3f29-742">0 自動。</span><span class="sxs-lookup"><span data-stu-id="f3f29-742">0 Auto.</span></span>          | <span data-ttu-id="f3f29-743">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-743">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f3f29-744">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-744">1 Column height.</span></span> | <span data-ttu-id="f3f29-745">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-745">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="f3f29-746">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-746">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="f3f29-747">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-747">Method heightMode</span></span>

<span data-ttu-id="f3f29-748">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-748">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="f3f29-749">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-749">Parameters - heightMode</span></span>

<span data-ttu-id="f3f29-750">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-750">value</span></span>  
<span data-ttu-id="f3f29-751">コントロールの高さの計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-751">An Integer data type value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="f3f29-752">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-752">Return Value - heightMode</span></span>

<span data-ttu-id="f3f29-753">計算モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-753">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="f3f29-754">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-754">Remarks - heightMode</span></span>

<span data-ttu-id="f3f29-755">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="f3f29-755">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="f3f29-756">モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-756">Mode.</span></span>          | <span data-ttu-id="f3f29-757">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="f3f29-757">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f29-758">正確。</span><span class="sxs-lookup"><span data-stu-id="f3f29-758">Exact.</span></span>         | <span data-ttu-id="f3f29-759">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-759">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f3f29-760">自動。</span><span class="sxs-lookup"><span data-stu-id="f3f29-760">Auto.</span></span>          | <span data-ttu-id="f3f29-761">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-761">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f3f29-762">列の高さ</span><span class="sxs-lookup"><span data-stu-id="f3f29-762">Column height.</span></span> | <span data-ttu-id="f3f29-763">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-763">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="f3f29-764">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-764">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="f3f29-765">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-765">Method heightValue</span></span>

<span data-ttu-id="f3f29-766">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-766">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="f3f29-767">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-767">Parameters - heightValue</span></span>

<span data-ttu-id="f3f29-768">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-768">value</span></span>  
<span data-ttu-id="f3f29-769">高さをピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-769">An Integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="f3f29-770">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-770">Return Value - heightValue</span></span>

<span data-ttu-id="f3f29-771">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-771">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="f3f29-772">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-772">Remarks - heightValue</span></span>

<span data-ttu-id="f3f29-773">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-773">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="f3f29-774">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="f3f29-774">Method helpField</span></span>

<span data-ttu-id="f3f29-775">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-775">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="f3f29-776">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="f3f29-776">Return Value - helpField</span></span>

<span data-ttu-id="f3f29-777">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="f3f29-777">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="f3f29-778">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="f3f29-778">Remarks - helpField</span></span>

<span data-ttu-id="f3f29-779">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-779">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="f3f29-780">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-780">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="f3f29-781">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="f3f29-781">Method helpText</span></span>

<span data-ttu-id="f3f29-782">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-782">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="f3f29-783">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="f3f29-783">Parameters - helpText</span></span>

<span data-ttu-id="f3f29-784">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-784">value</span></span>  
<span data-ttu-id="f3f29-785">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-785">The value to assign as the help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="f3f29-786">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="f3f29-786">Return Value - helpText</span></span>

<span data-ttu-id="f3f29-787">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="f3f29-787">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="f3f29-788">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="f3f29-788">Remarks - helpText</span></span>

<span data-ttu-id="f3f29-789">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-789">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="f3f29-790">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-790">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="f3f29-791">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="f3f29-791">Method hierarchyParent</span></span>

<span data-ttu-id="f3f29-792">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-792">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="f3f29-793">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="f3f29-793">Parameters - hierarchyParent</span></span>

<span data-ttu-id="f3f29-794">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-794">value</span></span>  
<span data-ttu-id="f3f29-795">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-795">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="f3f29-796">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="f3f29-796">Return Value - hierarchyParent</span></span>

<span data-ttu-id="f3f29-797">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-797">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="f3f29-798">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="f3f29-798">Method hWnd</span></span>

<span data-ttu-id="f3f29-799">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-799">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="f3f29-800">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="f3f29-800">Return Value - hWnd</span></span>

<span data-ttu-id="f3f29-801">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="f3f29-801">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="f3f29-802">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="f3f29-802">Remarks - hWnd</span></span>

<span data-ttu-id="f3f29-803">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-803">The handle can be used with the Windows API.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="f3f29-804">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="f3f29-804">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="f3f29-805">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="f3f29-805">Parameters - imageLocation</span></span>

<span data-ttu-id="f3f29-806">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-806">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="f3f29-807">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="f3f29-807">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="f3f29-808">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="f3f29-808">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="f3f29-809">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="f3f29-809">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="f3f29-810">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="f3f29-810">Method isDisplayed</span></span>

<span data-ttu-id="f3f29-811">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-811">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="f3f29-812">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="f3f29-812">Return Value - isDisplayed</span></span>

<span data-ttu-id="f3f29-813">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-813">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="f3f29-814">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="f3f29-814">Remarks - isDisplayed</span></span>

<span data-ttu-id="f3f29-815">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-815">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="f3f29-816">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="f3f29-816">Method isRestricted</span></span>

<span data-ttu-id="f3f29-817">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-817">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="f3f29-818">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="f3f29-818">Return Value - isRestricted</span></span>

<span data-ttu-id="f3f29-819">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-819">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="f3f29-820">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-820">Method isUserSetupEnabled</span></span>

<span data-ttu-id="f3f29-821">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-821">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="f3f29-822">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-822">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="f3f29-823">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="f3f29-823">neededSetupRights</span></span>  
<span data-ttu-id="f3f29-824">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-824">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="f3f29-825">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-825">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="f3f29-826">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-826">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="f3f29-827">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="f3f29-827">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="f3f29-828">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-828">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f29-829">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="f3f29-829">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="f3f29-830">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-830">No changes can be made to the control.</span></span> <span data-ttu-id="f3f29-831">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-831">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="f3f29-832">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="f3f29-832">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="f3f29-833">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-833">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="f3f29-834">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-834">The user cannot move the control.</span></span>   |
| <span data-ttu-id="f3f29-835">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="f3f29-835">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="f3f29-836">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-836">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="f3f29-837">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-837">The user can also move the control.</span></span> |

<span data-ttu-id="f3f29-838">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-838">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="f3f29-839">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="f3f29-839">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="f3f29-840">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="f3f29-840">Parameters - italic</span></span>

<span data-ttu-id="f3f29-841">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-841">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="f3f29-842">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="f3f29-842">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="f3f29-843">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="f3f29-843">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="f3f29-844">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="f3f29-844">Parameters - keyTip</span></span>

<span data-ttu-id="f3f29-845">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-845">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="f3f29-846">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="f3f29-846">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="f3f29-847">メソッド left</span><span class="sxs-lookup"><span data-stu-id="f3f29-847">Method left</span></span>

<span data-ttu-id="f3f29-848">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-848">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="f3f29-849">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="f3f29-849">Parameters - left</span></span>

<span data-ttu-id="f3f29-850">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-850">value</span></span>  
<span data-ttu-id="f3f29-851">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-851">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="f3f29-852">モード</span><span class="sxs-lookup"><span data-stu-id="f3f29-852">mode</span></span>  
<span data-ttu-id="f3f29-853">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-853">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="f3f29-854">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="f3f29-854">Return Value - left</span></span>

<span data-ttu-id="f3f29-855">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="f3f29-855">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="f3f29-856">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-856">Method leftMode</span></span>

<span data-ttu-id="f3f29-857">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-857">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="f3f29-858">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-858">Parameters - leftMode</span></span>

<span data-ttu-id="f3f29-859">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-859">value</span></span>  
<span data-ttu-id="f3f29-860">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-860">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="f3f29-861">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-861">Return Value - leftMode</span></span>

<span data-ttu-id="f3f29-862">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-862">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="f3f29-863">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-863">Method leftValue</span></span>

<span data-ttu-id="f3f29-864">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-864">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="f3f29-865">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-865">Parameters - leftValue</span></span>

<span data-ttu-id="f3f29-866">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-866">value</span></span>  
<span data-ttu-id="f3f29-867">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-867">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="f3f29-868">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-868">Return Value - leftValue</span></span>

<span data-ttu-id="f3f29-869">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="f3f29-869">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="f3f29-870">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="f3f29-870">Method markAsUserAdd</span></span>

<span data-ttu-id="f3f29-871">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-871">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="f3f29-872">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="f3f29-872">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="f3f29-873">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-873">value</span></span>  
<span data-ttu-id="f3f29-874">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-874">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="f3f29-875">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="f3f29-875">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="f3f29-876">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-876">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="f3f29-877">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="f3f29-877">Method mouseDblClick</span></span>

<span data-ttu-id="f3f29-878">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-878">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="f3f29-879">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="f3f29-879">Parameters - mouseDblClick</span></span>

<span data-ttu-id="f3f29-880">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-880">x</span></span>  
<span data-ttu-id="f3f29-881">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-881">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-882">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-882">y</span></span>  
<span data-ttu-id="f3f29-883">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-883">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-884">ボタン</span><span class="sxs-lookup"><span data-stu-id="f3f29-884">button</span></span>  
<span data-ttu-id="f3f29-885">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-885">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-886">Ctrl</span><span class="sxs-lookup"><span data-stu-id="f3f29-886">Ctrl</span></span>  
<span data-ttu-id="f3f29-887">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-887">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-888">シフト</span><span class="sxs-lookup"><span data-stu-id="f3f29-888">Shift</span></span>  
<span data-ttu-id="f3f29-889">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-889">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="f3f29-890">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="f3f29-890">Return Value - mouseDblClick</span></span>

<span data-ttu-id="f3f29-891">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-891">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="f3f29-892">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="f3f29-892">Remarks - mouseDblClick</span></span>

<span data-ttu-id="f3f29-893">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-893">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="f3f29-894">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="f3f29-894">Method mouseDown</span></span>

<span data-ttu-id="f3f29-895">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-895">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="f3f29-896">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="f3f29-896">Parameters - mouseDown</span></span>

<span data-ttu-id="f3f29-897">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-897">x</span></span>  
<span data-ttu-id="f3f29-898">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-898">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-899">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-899">y</span></span>  
<span data-ttu-id="f3f29-900">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-900">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-901">ボタン</span><span class="sxs-lookup"><span data-stu-id="f3f29-901">button</span></span>  
<span data-ttu-id="f3f29-902">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-902">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-903">Ctrl</span><span class="sxs-lookup"><span data-stu-id="f3f29-903">Ctrl</span></span>  
<span data-ttu-id="f3f29-904">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-904">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-905">シフト</span><span class="sxs-lookup"><span data-stu-id="f3f29-905">Shift</span></span>  
<span data-ttu-id="f3f29-906">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-906">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="f3f29-907">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="f3f29-907">Return Value - mouseDown</span></span>

<span data-ttu-id="f3f29-908">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-908">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="f3f29-909">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="f3f29-909">Remarks - mouseDown</span></span>

<span data-ttu-id="f3f29-910">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-910">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="f3f29-911">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-911">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="f3f29-912">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="f3f29-912">Method mouseMove</span></span>

<span data-ttu-id="f3f29-913">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-913">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="f3f29-914">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="f3f29-914">Parameters - mouseMove</span></span>

<span data-ttu-id="f3f29-915">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-915">x</span></span>  
<span data-ttu-id="f3f29-916">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-916">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-917">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-917">y</span></span>  
<span data-ttu-id="f3f29-918">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-918">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-919">ボタン</span><span class="sxs-lookup"><span data-stu-id="f3f29-919">button</span></span>  
<span data-ttu-id="f3f29-920">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-920">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-921">Ctrl</span><span class="sxs-lookup"><span data-stu-id="f3f29-921">Ctrl</span></span>  
<span data-ttu-id="f3f29-922">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-922">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-923">シフト</span><span class="sxs-lookup"><span data-stu-id="f3f29-923">Shift</span></span>  
<span data-ttu-id="f3f29-924">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-924">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="f3f29-925">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="f3f29-925">Return Value - mouseMove</span></span>

<span data-ttu-id="f3f29-926">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-926">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="f3f29-927">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="f3f29-927">Remarks - mouseMove</span></span>

<span data-ttu-id="f3f29-928">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-928">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="f3f29-929">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="f3f29-929">Method mouseUp</span></span>

<span data-ttu-id="f3f29-930">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-930">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="f3f29-931">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="f3f29-931">Parameters - mouseUp</span></span>

<span data-ttu-id="f3f29-932">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-932">x</span></span>  
<span data-ttu-id="f3f29-933">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-933">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-934">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-934">y</span></span>  
<span data-ttu-id="f3f29-935">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-935">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-936">ボタン</span><span class="sxs-lookup"><span data-stu-id="f3f29-936">button</span></span>  
<span data-ttu-id="f3f29-937">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-937">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-938">Ctrl</span><span class="sxs-lookup"><span data-stu-id="f3f29-938">Ctrl</span></span>  
<span data-ttu-id="f3f29-939">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-939">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-940">シフト</span><span class="sxs-lookup"><span data-stu-id="f3f29-940">Shift</span></span>  
<span data-ttu-id="f3f29-941">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-941">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="f3f29-942">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="f3f29-942">Return Value - mouseUp</span></span>

<span data-ttu-id="f3f29-943">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-943">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="f3f29-944">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="f3f29-944">Remarks - mouseUp</span></span>

<span data-ttu-id="f3f29-945">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-945">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="f3f29-946">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-946">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="f3f29-947">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="f3f29-947">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="f3f29-948">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="f3f29-948">Parameters - multiSelect</span></span>

<span data-ttu-id="f3f29-949">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-949">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="f3f29-950">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="f3f29-950">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="f3f29-951">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f3f29-951">Method name</span></span>

<span data-ttu-id="f3f29-952">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-952">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="f3f29-953">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="f3f29-953">Parameters - name</span></span>

<span data-ttu-id="f3f29-954">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-954">value</span></span>  
<span data-ttu-id="f3f29-955">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-955">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="f3f29-956">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="f3f29-956">Return Value - name</span></span>

<span data-ttu-id="f3f29-957">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f3f29-957">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="f3f29-958">備考 - name</span><span class="sxs-lookup"><span data-stu-id="f3f29-958">Remarks - name</span></span>

<span data-ttu-id="f3f29-959">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-959">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f3f29-960">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-960">It must start with a letter.</span></span>
-   <span data-ttu-id="f3f29-961">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-961">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="f3f29-962">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-962">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="f3f29-963">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-963">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f3f29-964">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-964">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="f3f29-965">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="f3f29-965">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="f3f29-966">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="f3f29-966">Parameters - neededPermission</span></span>

<span data-ttu-id="f3f29-967">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-967">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="f3f29-968">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="f3f29-968">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="f3f29-969">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="f3f29-969">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="f3f29-970">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="f3f29-970">Parameters - needsRecord</span></span>

<span data-ttu-id="f3f29-971">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-971">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="f3f29-972">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="f3f29-972">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="f3f29-973">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="f3f29-973">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="f3f29-974">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="f3f29-974">Parameters - normalImage</span></span>

<span data-ttu-id="f3f29-975">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-975">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="f3f29-976">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="f3f29-976">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="f3f29-977">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="f3f29-977">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="f3f29-978">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="f3f29-978">Parameters - normalResource</span></span>

<span data-ttu-id="f3f29-979">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-979">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="f3f29-980">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="f3f29-980">Return Value - normalResource</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="f3f29-981">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="f3f29-981">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="f3f29-982">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="f3f29-982">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parameters"></a><span data-ttu-id="f3f29-983">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="f3f29-983">Method parameters</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="f3f29-984">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="f3f29-984">Parameters - parameters</span></span>

<span data-ttu-id="f3f29-985">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-985">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="f3f29-986">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="f3f29-986">Return Value - parameters</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="f3f29-987">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-987">Method parentControl</span></span>

<span data-ttu-id="f3f29-988">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-988">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="f3f29-989">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-989">Return Value - parentControl</span></span>

<span data-ttu-id="f3f29-990">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="f3f29-990">The parent control for the control.</span></span>

## <a name="method-primary"></a><span data-ttu-id="f3f29-991">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="f3f29-991">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="f3f29-992">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="f3f29-992">Parameters - primary</span></span>

<span data-ttu-id="f3f29-993">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-993">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="f3f29-994">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="f3f29-994">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="f3f29-995">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="f3f29-995">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="f3f29-996">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="f3f29-996">Parameters - saveRecord</span></span>

<span data-ttu-id="f3f29-997">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-997">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="f3f29-998">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="f3f29-998">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="f3f29-999">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="f3f29-999">Method securityKey</span></span>

<span data-ttu-id="f3f29-1000">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1000">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="f3f29-1001">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="f3f29-1001">Parameters - securityKey</span></span>

<span data-ttu-id="f3f29-1002">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1002">value</span></span>  
<span data-ttu-id="f3f29-1003">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1003">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="f3f29-1004">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="f3f29-1004">Return Value - securityKey</span></span>

<span data-ttu-id="f3f29-1005">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1005">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="f3f29-1006">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="f3f29-1006">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="f3f29-1007">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="f3f29-1007">Parameters - shortkey</span></span>

<span data-ttu-id="f3f29-1008">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1008">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="f3f29-1009">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="f3f29-1009">Return Value - shortkey</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="f3f29-1010">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="f3f29-1010">Method showContextMenu</span></span>

<span data-ttu-id="f3f29-1011">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1011">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="f3f29-1012">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="f3f29-1012">Parameters - showContextMenu</span></span>

<span data-ttu-id="f3f29-1013">menuHandle</span><span class="sxs-lookup"><span data-stu-id="f3f29-1013">menuHandle</span></span>  
<span data-ttu-id="f3f29-1014">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1014">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="f3f29-1015">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="f3f29-1015">Return Value - showContextMenu</span></span>

<span data-ttu-id="f3f29-1016">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1016">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="f3f29-1017">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="f3f29-1017">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="f3f29-1018">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="f3f29-1018">Parameters - showShortCut</span></span>

<span data-ttu-id="f3f29-1019">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1019">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="f3f29-1020">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="f3f29-1020">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="f3f29-1021">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1021">Method skip</span></span>

<span data-ttu-id="f3f29-1022">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1022">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="f3f29-1023">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1023">Parameters - skip</span></span>

<span data-ttu-id="f3f29-1024">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1024">value</span></span>  
<span data-ttu-id="f3f29-1025">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1025">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="f3f29-1026">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1026">Return Value - skip</span></span>

<span data-ttu-id="f3f29-1027">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1027">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="f3f29-1028">メソッド style</span><span class="sxs-lookup"><span data-stu-id="f3f29-1028">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="f3f29-1029">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="f3f29-1029">Parameters - style</span></span>

<span data-ttu-id="f3f29-1030">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1030">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="f3f29-1031">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="f3f29-1031">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="f3f29-1032">メソッド text</span><span class="sxs-lookup"><span data-stu-id="f3f29-1032">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="f3f29-1033">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="f3f29-1033">Parameters - text</span></span>

<span data-ttu-id="f3f29-1034">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1034">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="f3f29-1035">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="f3f29-1035">Return Value - text</span></span>

## <a name="method-togglebutton"></a><span data-ttu-id="f3f29-1036">メソッド toggleButton</span><span class="sxs-lookup"><span data-stu-id="f3f29-1036">Method toggleButton</span></span>

```xpp
public int toggleButton([int value])
```

### <a name="parameters---togglebutton"></a><span data-ttu-id="f3f29-1037">パラメーター - toggleButton</span><span class="sxs-lookup"><span data-stu-id="f3f29-1037">Parameters - toggleButton</span></span>

<span data-ttu-id="f3f29-1038">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1038">value</span></span>  

### <a name="return-value---togglebutton"></a><span data-ttu-id="f3f29-1039">戻り値 - toggleButton</span><span class="sxs-lookup"><span data-stu-id="f3f29-1039">Return Value - toggleButton</span></span>

## <a name="method-togglevalue"></a><span data-ttu-id="f3f29-1040">メソッド toggleValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1040">Method toggleValue</span></span>

```xpp
public int toggleValue([int value])
```

### <a name="parameters---togglevalue"></a><span data-ttu-id="f3f29-1041">パラメーター - toggleValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1041">Parameters - toggleValue</span></span>

<span data-ttu-id="f3f29-1042">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1042">value</span></span>  

### <a name="return-value---togglevalue"></a><span data-ttu-id="f3f29-1043">戻り値 - toggleValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1043">Return Value - toggleValue</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="f3f29-1044">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1044">Method toolTip</span></span>

<span data-ttu-id="f3f29-1045">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1045">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="f3f29-1046">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1046">Return Value - toolTip</span></span>

<span data-ttu-id="f3f29-1047">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1047">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="f3f29-1048">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1048">Remarks - toolTip</span></span>

<span data-ttu-id="f3f29-1049">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1049">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="f3f29-1050">メソッド top</span><span class="sxs-lookup"><span data-stu-id="f3f29-1050">Method top</span></span>

<span data-ttu-id="f3f29-1051">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1051">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="f3f29-1052">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="f3f29-1052">Parameters - top</span></span>

<span data-ttu-id="f3f29-1053">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1053">value</span></span>  
<span data-ttu-id="f3f29-1054">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1054">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1055">モード</span><span class="sxs-lookup"><span data-stu-id="f3f29-1055">mode</span></span>  
<span data-ttu-id="f3f29-1056">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1056">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="f3f29-1057">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="f3f29-1057">Return Value - top</span></span>

<span data-ttu-id="f3f29-1058">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1058">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="f3f29-1059">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1059">Method topMode</span></span>

<span data-ttu-id="f3f29-1060">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1060">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="f3f29-1061">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1061">Parameters - topMode</span></span>

<span data-ttu-id="f3f29-1062">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1062">value</span></span>  
<span data-ttu-id="f3f29-1063">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1063">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="f3f29-1064">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1064">Return Value - topMode</span></span>

<span data-ttu-id="f3f29-1065">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1065">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="f3f29-1066">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1066">Method topValue</span></span>

<span data-ttu-id="f3f29-1067">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1067">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="f3f29-1068">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1068">Parameters - topValue</span></span>

<span data-ttu-id="f3f29-1069">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1069">value</span></span>  
<span data-ttu-id="f3f29-1070">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1070">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="f3f29-1071">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1071">Return Value - topValue</span></span>

<span data-ttu-id="f3f29-1072">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1072">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="f3f29-1073">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="f3f29-1073">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="f3f29-1074">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="f3f29-1074">Parameters - type</span></span>

<span data-ttu-id="f3f29-1075">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1075">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="f3f29-1076">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="f3f29-1076">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="f3f29-1077">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="f3f29-1077">Method underline</span></span>

<span data-ttu-id="f3f29-1078">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1078">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="f3f29-1079">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="f3f29-1079">Parameters - underline</span></span>

<span data-ttu-id="f3f29-1080">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1080">value</span></span>  
<span data-ttu-id="f3f29-1081">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1081">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="f3f29-1082">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="f3f29-1082">Return Value - underline</span></span>

<span data-ttu-id="f3f29-1083">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1083">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="f3f29-1084">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="f3f29-1084">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="f3f29-1085">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="f3f29-1085">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="f3f29-1086">データ</span><span class="sxs-lookup"><span data-stu-id="f3f29-1086">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="f3f29-1087">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="f3f29-1087">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="f3f29-1088">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="f3f29-1088">Method userData</span></span>

<span data-ttu-id="f3f29-1089">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1089">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="f3f29-1090">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="f3f29-1090">Parameters - userData</span></span>

<span data-ttu-id="f3f29-1091">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1091">value</span></span>  
<span data-ttu-id="f3f29-1092">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1092">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="f3f29-1093">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="f3f29-1093">Return Value - userData</span></span>

<span data-ttu-id="f3f29-1094">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1094">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="f3f29-1095">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="f3f29-1095">Method userDataItem</span></span>

<span data-ttu-id="f3f29-1096">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1096">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="f3f29-1097">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="f3f29-1097">Parameters - userDataItem</span></span>

<span data-ttu-id="f3f29-1098">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1098">value</span></span>  
<span data-ttu-id="f3f29-1099">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1099">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="f3f29-1100">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="f3f29-1100">Return Value - userDataItem</span></span>

<span data-ttu-id="f3f29-1101">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1101">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="f3f29-1102">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="f3f29-1102">Method userDataItems</span></span>

<span data-ttu-id="f3f29-1103">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1103">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="f3f29-1104">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="f3f29-1104">Parameters - userDataItems</span></span>

<span data-ttu-id="f3f29-1105">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1105">value</span></span>  
<span data-ttu-id="f3f29-1106">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1106">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="f3f29-1107">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="f3f29-1107">Return Value - userDataItems</span></span>

<span data-ttu-id="f3f29-1108">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1108">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="f3f29-1109">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="f3f29-1109">Method userDisable</span></span>

<span data-ttu-id="f3f29-1110">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1110">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="f3f29-1111">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="f3f29-1111">Parameters - userDisable</span></span>

<span data-ttu-id="f3f29-1112">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1112">value</span></span>  
<span data-ttu-id="f3f29-1113">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1113">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="f3f29-1114">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="f3f29-1114">Return Value - userDisable</span></span>

<span data-ttu-id="f3f29-1115">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1115">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="f3f29-1116">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="f3f29-1116">Method userHeight</span></span>

<span data-ttu-id="f3f29-1117">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1117">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="f3f29-1118">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="f3f29-1118">Parameters - userHeight</span></span>

<span data-ttu-id="f3f29-1119">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1119">value</span></span>  
<span data-ttu-id="f3f29-1120">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1120">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="f3f29-1121">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="f3f29-1121">Return Value - userHeight</span></span>

<span data-ttu-id="f3f29-1122">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1122">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="f3f29-1123">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="f3f29-1123">Method userHide</span></span>

<span data-ttu-id="f3f29-1124">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1124">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="f3f29-1125">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="f3f29-1125">Parameters - userHide</span></span>

<span data-ttu-id="f3f29-1126">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1126">value</span></span>  
<span data-ttu-id="f3f29-1127">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1127">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="f3f29-1128">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="f3f29-1128">Return Value - userHide</span></span>

<span data-ttu-id="f3f29-1129">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1129">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="f3f29-1130">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="f3f29-1130">Remarks - userHide</span></span>

<span data-ttu-id="f3f29-1131">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1131">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="f3f29-1132">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1132">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="f3f29-1133">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1133">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="f3f29-1134">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="f3f29-1134">Method userOrgContainer</span></span>

<span data-ttu-id="f3f29-1135">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1135">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="f3f29-1136">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="f3f29-1136">Parameters - userOrgContainer</span></span>

<span data-ttu-id="f3f29-1137">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1137">value</span></span>  
<span data-ttu-id="f3f29-1138">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1138">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="f3f29-1139">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="f3f29-1139">Return Value - userOrgContainer</span></span>

<span data-ttu-id="f3f29-1140">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1140">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="f3f29-1141">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="f3f29-1141">Method userOrgSibling</span></span>

<span data-ttu-id="f3f29-1142">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1142">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="f3f29-1143">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="f3f29-1143">Parameters - userOrgSibling</span></span>

<span data-ttu-id="f3f29-1144">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1144">value</span></span>  
<span data-ttu-id="f3f29-1145">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1145">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="f3f29-1146">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="f3f29-1146">Return Value - userOrgSibling</span></span>

<span data-ttu-id="f3f29-1147">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1147">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="f3f29-1148">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="f3f29-1148">Method userPromptText</span></span>

<span data-ttu-id="f3f29-1149">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1149">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="f3f29-1150">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="f3f29-1150">Parameters - userPromptText</span></span>

<span data-ttu-id="f3f29-1151">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1151">value</span></span>  
<span data-ttu-id="f3f29-1152">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1152">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="f3f29-1153">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="f3f29-1153">Return Value - userPromptText</span></span>

<span data-ttu-id="f3f29-1154">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1154">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="f3f29-1155">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="f3f29-1155">Method userSecurityLevel</span></span>

<span data-ttu-id="f3f29-1156">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1156">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="f3f29-1157">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="f3f29-1157">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="f3f29-1158">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1158">value</span></span>  
<span data-ttu-id="f3f29-1159">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1159">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="f3f29-1160">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="f3f29-1160">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="f3f29-1161">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1161">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="f3f29-1162">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1162">Method userSkip</span></span>

<span data-ttu-id="f3f29-1163">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1163">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="f3f29-1164">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1164">Parameters - userSkip</span></span>

<span data-ttu-id="f3f29-1165">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1165">value</span></span>  
<span data-ttu-id="f3f29-1166">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1166">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="f3f29-1167">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1167">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="f3f29-1168">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="f3f29-1168">Return Value - userSkip</span></span>

<span data-ttu-id="f3f29-1169">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1169">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="f3f29-1170">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="f3f29-1170">Method userWidth</span></span>

<span data-ttu-id="f3f29-1171">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1171">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="f3f29-1172">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="f3f29-1172">Parameters - userWidth</span></span>

<span data-ttu-id="f3f29-1173">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1173">value</span></span>  
<span data-ttu-id="f3f29-1174">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1174">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="f3f29-1175">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="f3f29-1175">Return Value - userWidth</span></span>

<span data-ttu-id="f3f29-1176">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1176">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="f3f29-1177">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="f3f29-1177">Remarks - userWidth</span></span>

<span data-ttu-id="f3f29-1178">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1178">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="f3f29-1179">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1179">For example, if the user has specified 30 characters as the width for the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="f3f29-1180">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1180">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-value"></a><span data-ttu-id="f3f29-1181">メソッド value</span><span class="sxs-lookup"><span data-stu-id="f3f29-1181">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="f3f29-1182">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="f3f29-1182">Parameters - value</span></span>

<span data-ttu-id="f3f29-1183">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1183">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="f3f29-1184">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="f3f29-1184">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="f3f29-1185">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="f3f29-1185">Method verticalSpacing</span></span>

<span data-ttu-id="f3f29-1186">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1186">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="f3f29-1187">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="f3f29-1187">Parameters - verticalSpacing</span></span>

<span data-ttu-id="f3f29-1188">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1188">value</span></span>  
<span data-ttu-id="f3f29-1189">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1189">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1190">モード</span><span class="sxs-lookup"><span data-stu-id="f3f29-1190">mode</span></span>  
<span data-ttu-id="f3f29-1191">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1191">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="f3f29-1192">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="f3f29-1192">Return Value - verticalSpacing</span></span>

<span data-ttu-id="f3f29-1193">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1193">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="f3f29-1194">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1194">Method verticalSpacingMode</span></span>

<span data-ttu-id="f3f29-1195">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1195">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="f3f29-1196">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1196">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="f3f29-1197">モード</span><span class="sxs-lookup"><span data-stu-id="f3f29-1197">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="f3f29-1198">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1198">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="f3f29-1199">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1199">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="f3f29-1200">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1200">Method verticalSpacingValue</span></span>

<span data-ttu-id="f3f29-1201">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1201">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="f3f29-1202">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1202">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="f3f29-1203">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1203">value</span></span>  
<span data-ttu-id="f3f29-1204">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1204">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="f3f29-1205">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1205">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="f3f29-1206">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1206">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="f3f29-1207">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="f3f29-1207">Method visible</span></span>

<span data-ttu-id="f3f29-1208">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1208">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="f3f29-1209">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="f3f29-1209">Parameters - visible</span></span>

<span data-ttu-id="f3f29-1210">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1210">value</span></span>  
<span data-ttu-id="f3f29-1211">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1211">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="f3f29-1212">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="f3f29-1212">Return Value - visible</span></span>

<span data-ttu-id="f3f29-1213">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1213">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="f3f29-1214">メソッド width</span><span class="sxs-lookup"><span data-stu-id="f3f29-1214">Method width</span></span>

<span data-ttu-id="f3f29-1215">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1215">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="f3f29-1216">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="f3f29-1216">Parameters - width</span></span>

<span data-ttu-id="f3f29-1217">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1217">value</span></span>  
<span data-ttu-id="f3f29-1218">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1218">An Integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1219">モード</span><span class="sxs-lookup"><span data-stu-id="f3f29-1219">mode</span></span>  
<span data-ttu-id="f3f29-1220">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1220">An Integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="f3f29-1221">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="f3f29-1221">Return Value - width</span></span>

<span data-ttu-id="f3f29-1222">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1222">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="f3f29-1223">備考 - width</span><span class="sxs-lookup"><span data-stu-id="f3f29-1223">Remarks - width</span></span>

<span data-ttu-id="f3f29-1224">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1224">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="f3f29-1225">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="f3f29-1225">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="f3f29-1226">モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1226">Mode.</span></span>           | <span data-ttu-id="f3f29-1227">幅計算。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1227">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f29-1228">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1228">-1 Exact.</span></span>       | <span data-ttu-id="f3f29-1229">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1229">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f3f29-1230">0 自動。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1230">0 Auto.</span></span>         | <span data-ttu-id="f3f29-1231">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1231">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f3f29-1232">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1232">1 Column width.</span></span> | <span data-ttu-id="f3f29-1233">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1233">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="f3f29-1234">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1234">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="f3f29-1235">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1235">Method widthMode</span></span>

<span data-ttu-id="f3f29-1236">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1236">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="f3f29-1237">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1237">Parameters - widthMode</span></span>

<span data-ttu-id="f3f29-1238">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1238">value</span></span>  
<span data-ttu-id="f3f29-1239">コントロールの幅の計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1239">An Integer data type value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="f3f29-1240">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1240">Return Value - widthMode</span></span>

<span data-ttu-id="f3f29-1241">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1241">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="f3f29-1242">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1242">Remarks - widthMode</span></span>

<span data-ttu-id="f3f29-1243">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="f3f29-1243">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="f3f29-1244">モード。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1244">Mode.</span></span>         | <span data-ttu-id="f3f29-1245">幅計算。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1245">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f29-1246">正確。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1246">Exact.</span></span>        | <span data-ttu-id="f3f29-1247">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1247">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f3f29-1248">自動。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1248">Auto.</span></span>         | <span data-ttu-id="f3f29-1249">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1249">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f3f29-1250">列の幅。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1250">Column width.</span></span> | <span data-ttu-id="f3f29-1251">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1251">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="f3f29-1252">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1252">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="f3f29-1253">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1253">Method widthValue</span></span>

<span data-ttu-id="f3f29-1254">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1254">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="f3f29-1255">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1255">Parameters - widthValue</span></span>

<span data-ttu-id="f3f29-1256">値</span><span class="sxs-lookup"><span data-stu-id="f3f29-1256">value</span></span>  
<span data-ttu-id="f3f29-1257">幅をピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1257">An Integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="f3f29-1258">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1258">Return Value - widthValue</span></span>

<span data-ttu-id="f3f29-1259">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1259">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="f3f29-1260">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="f3f29-1260">Remarks - widthValue</span></span>

<span data-ttu-id="f3f29-1261">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1261">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-onclicked"></a><span data-ttu-id="f3f29-1262">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="f3f29-1262">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="f3f29-1263">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="f3f29-1263">Parameters - OnClicked</span></span>

<span data-ttu-id="f3f29-1264">sender</span><span class="sxs-lookup"><span data-stu-id="f3f29-1264">sender</span></span>  

<!-- -->

<span data-ttu-id="f3f29-1265">e</span><span class="sxs-lookup"><span data-stu-id="f3f29-1265">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="f3f29-1266">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="f3f29-1266">Method displayControl</span></span>

<span data-ttu-id="f3f29-1267">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1267">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-drop"></a><span data-ttu-id="f3f29-1268">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="f3f29-1268">Method drop</span></span>

<span data-ttu-id="f3f29-1269">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1269">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="f3f29-1270">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="f3f29-1270">Parameters - drop</span></span>

<span data-ttu-id="f3f29-1271">dragSource</span><span class="sxs-lookup"><span data-stu-id="f3f29-1271">dragSource</span></span>  
<span data-ttu-id="f3f29-1272">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1272">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1273">dragMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1273">dragMode</span></span>  
<span data-ttu-id="f3f29-1274">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1274">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1275">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-1275">x</span></span>  
<span data-ttu-id="f3f29-1276">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1276">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1277">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-1277">y</span></span>  
<span data-ttu-id="f3f29-1278">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1278">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-inputsearch"></a><span data-ttu-id="f3f29-1279">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="f3f29-1279">Method inputSearch</span></span>

<span data-ttu-id="f3f29-1280">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1280">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="f3f29-1281">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="f3f29-1281">Parameters - inputSearch</span></span>

<span data-ttu-id="f3f29-1282">searchStr</span><span class="sxs-lookup"><span data-stu-id="f3f29-1282">searchStr</span></span>  
<span data-ttu-id="f3f29-1283">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1283">The string value to use to filter data; optional.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="f3f29-1284">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="f3f29-1284">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="f3f29-1285">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="f3f29-1285">Parameters - OnLostFocus</span></span>

<span data-ttu-id="f3f29-1286">sender</span><span class="sxs-lookup"><span data-stu-id="f3f29-1286">sender</span></span>  

<!-- -->

<span data-ttu-id="f3f29-1287">e</span><span class="sxs-lookup"><span data-stu-id="f3f29-1287">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="f3f29-1288">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-1288">Method dropEx</span></span>

<span data-ttu-id="f3f29-1289">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1289">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="f3f29-1290">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="f3f29-1290">Parameters - dropEx</span></span>

<span data-ttu-id="f3f29-1291">dragSource</span><span class="sxs-lookup"><span data-stu-id="f3f29-1291">dragSource</span></span>  
<span data-ttu-id="f3f29-1292">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1292">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1293">dragMode</span><span class="sxs-lookup"><span data-stu-id="f3f29-1293">dragMode</span></span>  
<span data-ttu-id="f3f29-1294">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1294">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1295">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-1295">x</span></span>  
<span data-ttu-id="f3f29-1296">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1296">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1297">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-1297">y</span></span>  
<span data-ttu-id="f3f29-1298">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1298">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-cut"></a><span data-ttu-id="f3f29-1299">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="f3f29-1299">Method cut</span></span>

<span data-ttu-id="f3f29-1300">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1300">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-mouseenter"></a><span data-ttu-id="f3f29-1301">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="f3f29-1301">Method mouseEnter</span></span>

<span data-ttu-id="f3f29-1302">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1302">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="f3f29-1303">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="f3f29-1303">Parameters - mouseEnter</span></span>

<span data-ttu-id="f3f29-1304">x</span><span class="sxs-lookup"><span data-stu-id="f3f29-1304">x</span></span>  
<span data-ttu-id="f3f29-1305">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1305">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1306">y</span><span class="sxs-lookup"><span data-stu-id="f3f29-1306">y</span></span>  
<span data-ttu-id="f3f29-1307">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1307">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1308">ボタン</span><span class="sxs-lookup"><span data-stu-id="f3f29-1308">button</span></span>  
<span data-ttu-id="f3f29-1309">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1309">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1310">Ctrl</span><span class="sxs-lookup"><span data-stu-id="f3f29-1310">Ctrl</span></span>  
<span data-ttu-id="f3f29-1311">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1311">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1312">シフト</span><span class="sxs-lookup"><span data-stu-id="f3f29-1312">Shift</span></span>  
<span data-ttu-id="f3f29-1313">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1313">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="f3f29-1314">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="f3f29-1314">Method setFocus</span></span>

<span data-ttu-id="f3f29-1315">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1315">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-paste"></a><span data-ttu-id="f3f29-1316">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="f3f29-1316">Method paste</span></span>

<span data-ttu-id="f3f29-1317">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1317">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-gotfocus"></a><span data-ttu-id="f3f29-1318">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="f3f29-1318">Method gotFocus</span></span>

<span data-ttu-id="f3f29-1319">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1319">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="f3f29-1320">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="f3f29-1320">Method resetUserSetting</span></span>

<span data-ttu-id="f3f29-1321">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1321">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-lostfocus"></a><span data-ttu-id="f3f29-1322">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="f3f29-1322">Method lostFocus</span></span>

<span data-ttu-id="f3f29-1323">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1323">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="f3f29-1324">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-1324">Method prefColumnSize</span></span>

<span data-ttu-id="f3f29-1325">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1325">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="f3f29-1326">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="f3f29-1326">Parameters - prefColumnSize</span></span>

<span data-ttu-id="f3f29-1327">width</span><span class="sxs-lookup"><span data-stu-id="f3f29-1327">width</span></span>  
<span data-ttu-id="f3f29-1328">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1328">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="f3f29-1329">height</span><span class="sxs-lookup"><span data-stu-id="f3f29-1329">height</span></span>  
<span data-ttu-id="f3f29-1330">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1330">The preferred height of the control.</span></span>

## <a name="method-clicked"></a><span data-ttu-id="f3f29-1331">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="f3f29-1331">Method clicked</span></span>

```xpp
public void clicked()
```

## <a name="method-copy"></a><span data-ttu-id="f3f29-1332">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="f3f29-1332">Method copy</span></span>

<span data-ttu-id="f3f29-1333">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1333">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-dragleave"></a><span data-ttu-id="f3f29-1334">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="f3f29-1334">Method dragLeave</span></span>

<span data-ttu-id="f3f29-1335">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1335">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-mouseleave"></a><span data-ttu-id="f3f29-1336">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="f3f29-1336">Method mouseLeave</span></span>

<span data-ttu-id="f3f29-1337">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1337">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="f3f29-1338">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="f3f29-1338">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="f3f29-1339">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="f3f29-1339">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="f3f29-1340">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="f3f29-1340">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="f3f29-1341">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="f3f29-1341">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="f3f29-1342">overrideObject</span><span class="sxs-lookup"><span data-stu-id="f3f29-1342">overrideObject</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="f3f29-1343">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="f3f29-1343">Method endDrag</span></span>

<span data-ttu-id="f3f29-1344">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1344">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="f3f29-1345">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="f3f29-1345">Remarks - endDrag</span></span>

<span data-ttu-id="f3f29-1346">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1346">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="f3f29-1347">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1347">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-context"></a><span data-ttu-id="f3f29-1348">メソッド context</span><span class="sxs-lookup"><span data-stu-id="f3f29-1348">Method context</span></span>

<span data-ttu-id="f3f29-1349">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="f3f29-1349">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="f3f29-1350">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="f3f29-1350">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="f3f29-1351">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="f3f29-1351">Parameters - OnGotFocus</span></span>

<span data-ttu-id="f3f29-1352">sender</span><span class="sxs-lookup"><span data-stu-id="f3f29-1352">sender</span></span>  

<!-- -->

<span data-ttu-id="f3f29-1353">e</span><span class="sxs-lookup"><span data-stu-id="f3f29-1353">e</span></span>  

