---
title: FormButtonControl クラス
description: このトピックでは、FormButtonControl クラスについて説明します。
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
ms.openlocfilehash: 85d07cb1c8d418551629c7943656d53280ff5699
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502955"
---
# <a name="class-formbuttoncontrol"></a><span data-ttu-id="2e774-103">クラス FormButtonControl</span><span class="sxs-lookup"><span data-stu-id="2e774-103">Class FormButtonControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormButtonControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="2e774-104">備考</span><span class="sxs-lookup"><span data-stu-id="2e774-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="2e774-105">例</span><span class="sxs-lookup"><span data-stu-id="2e774-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2e774-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="2e774-106">Methods</span></span>

| <span data-ttu-id="2e774-107">方法</span><span class="sxs-lookup"><span data-stu-id="2e774-107">Method</span></span>                                                                                                      | <span data-ttu-id="2e774-108">説明</span><span class="sxs-lookup"><span data-stu-id="2e774-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e774-109">public int acquireFocus(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-109">public int acquireFocus(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="2e774-110">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-110">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="2e774-111">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-111">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2e774-112">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-112">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="2e774-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="2e774-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-114">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="2e774-115">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="2e774-115">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="2e774-116">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-116">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="2e774-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="2e774-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="2e774-119">public boolean autoRefreshData(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-119">public boolean autoRefreshData(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="2e774-120">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-120">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="2e774-121">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-121">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="2e774-122">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-122">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="2e774-123">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-123">Determines whether the control background can be transparent.</span></span>                                                                                                           |
| <span data-ttu-id="2e774-124">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2e774-124">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="2e774-125">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-125">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="2e774-126">public boolean big(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-126">public boolean big(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2e774-127">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-127">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="2e774-128">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-128">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                                             |
| <span data-ttu-id="2e774-129">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-129">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="2e774-130">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-130">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="2e774-131">public int buttonDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-131">public int buttonDisplay(\[int value\])</span></span>                                                                     | <span data-ttu-id="2e774-132">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-132">Gets or sets the appearance of the button control.</span></span>                                                                                                                      |
| <span data-ttu-id="2e774-133">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="2e774-133">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="2e774-134">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-134">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="2e774-135">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-135">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="2e774-136">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-136">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="2e774-137">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-137">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="2e774-138">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-138">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="2e774-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="2e774-140">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-140">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="2e774-141">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="2e774-141">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="2e774-142">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-142">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="2e774-143">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-143">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="2e774-144">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-144">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="2e774-145">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-145">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="2e774-146">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-146">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="2e774-147">public boolean defaultButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-147">public boolean defaultButton(\[boolean value\])</span></span>                                                             | <span data-ttu-id="2e774-148">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-148">Determines whether the button should be the default button on the form.</span></span>                                                                                                 |
| <span data-ttu-id="2e774-149">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-149">public str disabledImage(\[str value\])</span></span>                                                                     | <span data-ttu-id="2e774-150">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-150">Gets or sets the disabled image of the button.</span></span>                                                                                                                          |
| <span data-ttu-id="2e774-151">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-151">public int disabledImageLocation(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2e774-152">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-152">public int disabledResource(\[int value\])</span></span>                                                                  | <span data-ttu-id="2e774-153">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-153">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                                                          |
| <span data-ttu-id="2e774-154">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-154">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="2e774-155">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-155">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="2e774-156">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-156">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="2e774-157">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-157">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="2e774-158">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2e774-158">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="2e774-159">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-159">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="2e774-160">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2e774-160">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="2e774-161">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-161">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="2e774-162">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="2e774-162">public str dragText()</span></span>                                                                                       | <span data-ttu-id="2e774-163">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-163">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="2e774-164">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-164">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="2e774-165">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-165">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="2e774-166">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-166">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="2e774-167">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-167">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="2e774-168">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-168">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="2e774-169">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-169">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="2e774-170">public boolean forcedToOverflow(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-170">public boolean forcedToOverflow(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="2e774-171">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-171">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="2e774-172">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-172">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="2e774-173">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="2e774-173">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="2e774-174">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-174">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="2e774-175">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="2e774-175">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="2e774-176">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-176">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="2e774-177">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2e774-177">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="2e774-178">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-178">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="2e774-179">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-179">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="2e774-180">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-180">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="2e774-181">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-181">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="2e774-182">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-182">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="2e774-183">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="2e774-183">public str helpField()</span></span>                                                                                      | <span data-ttu-id="2e774-184">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-184">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2e774-185">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-185">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="2e774-186">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-186">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="2e774-187">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-187">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="2e774-188">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-188">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="2e774-189">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="2e774-189">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="2e774-190">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-190">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="2e774-191">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-191">public int imageLocation(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2e774-192">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="2e774-192">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2e774-193">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="2e774-193">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="2e774-194">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-194">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="2e774-195">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="2e774-195">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="2e774-196">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-196">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="2e774-197">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="2e774-197">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="2e774-198">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-198">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="2e774-199">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-199">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="2e774-200">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-200">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="2e774-201">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2e774-201">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="2e774-202">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-202">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="2e774-203">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-203">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="2e774-204">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-204">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2e774-205">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-205">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="2e774-206">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-206">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="2e774-207">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-207">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="2e774-208">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="2e774-208">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="2e774-209">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2e774-209">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="2e774-210">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-210">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="2e774-211">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2e774-211">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="2e774-212">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-212">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="2e774-213">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2e774-213">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="2e774-214">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-214">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="2e774-215">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2e774-215">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="2e774-216">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-216">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="2e774-217">public int multiSelect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-217">public int multiSelect(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2e774-218">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-218">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="2e774-219">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-219">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>                           |
| <span data-ttu-id="2e774-220">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-220">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="2e774-221">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-221">public int needsRecord(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2e774-222">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-222">public str normalImage(\[str value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2e774-223">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-223">public int normalResource(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="2e774-224">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="2e774-224">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2e774-225">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="2e774-225">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="2e774-226">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-226">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="2e774-227">public boolean primary(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-227">public boolean primary(\[boolean value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="2e774-228">public boolean saveRecord(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-228">public boolean saveRecord(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2e774-229">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-229">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="2e774-230">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-230">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="2e774-231">public int shortkey(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-231">public int shortkey(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="2e774-232">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="2e774-232">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="2e774-233">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-233">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2e774-234">public boolean showShortCut(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-234">public boolean showShortCut(\[boolean value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2e774-235">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-235">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="2e774-236">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-236">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="2e774-237">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-237">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2e774-238">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-238">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2e774-239">public int toggleButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-239">public int toggleButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="2e774-240">public int toggleValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-240">public int toggleValue(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2e774-241">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="2e774-241">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="2e774-242">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-242">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="2e774-243">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2e774-243">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="2e774-244">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-244">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="2e774-245">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-245">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="2e774-246">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-246">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="2e774-247">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-247">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="2e774-248">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-248">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="2e774-249">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-249">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2e774-250">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-250">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="2e774-251">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="2e774-251">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="2e774-252">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-252">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="2e774-253">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-253">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="2e774-254">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-254">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="2e774-255">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-255">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="2e774-256">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-256">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="2e774-257">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-257">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="2e774-258">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-258">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="2e774-259">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-259">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="2e774-260">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-260">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="2e774-261">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-261">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="2e774-262">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-262">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="2e774-263">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-263">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="2e774-264">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-264">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="2e774-265">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-265">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="2e774-266">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-266">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="2e774-267">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-267">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="2e774-268">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-268">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="2e774-269">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-269">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="2e774-270">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-270">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="2e774-271">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-271">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="2e774-272">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-272">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="2e774-273">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-273">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="2e774-274">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-274">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="2e774-275">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-275">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="2e774-276">public boolean value(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-276">public boolean value(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2e774-277">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2e774-277">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="2e774-278">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-278">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2e774-279">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2e774-279">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="2e774-280">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-280">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="2e774-281">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-281">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="2e774-282">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-282">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2e774-283">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-283">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="2e774-284">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-284">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="2e774-285">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2e774-285">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="2e774-286">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-286">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="2e774-287">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-287">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="2e774-288">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-288">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="2e774-289">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2e774-289">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="2e774-290">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-290">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="2e774-291">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="2e774-291">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="2e774-292">public void copy()</span><span class="sxs-lookup"><span data-stu-id="2e774-292">public void copy()</span></span>                                                                                          | <span data-ttu-id="2e774-293">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="2e774-293">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="2e774-294">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2e774-294">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="2e774-295">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="2e774-295">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="2e774-296">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-296">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="2e774-297">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="2e774-297">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="2e774-298">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-298">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="2e774-299">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="2e774-299">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="2e774-300">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-300">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="2e774-301">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2e774-301">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="2e774-302">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-302">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="2e774-303">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="2e774-303">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="2e774-304">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-304">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="2e774-305">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="2e774-305">public void clicked()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2e774-306">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2e774-306">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="2e774-307">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="2e774-307">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="2e774-308">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-308">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="2e774-309">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="2e774-309">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="2e774-310">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-310">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="2e774-311">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="2e774-311">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="2e774-312">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="2e774-312">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="2e774-313">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2e774-313">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="2e774-314">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-314">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="2e774-315">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2e774-315">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="2e774-316">public void cut()</span><span class="sxs-lookup"><span data-stu-id="2e774-316">public void cut()</span></span>                                                                                           | <span data-ttu-id="2e774-317">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="2e774-317">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="2e774-318">public void context()</span><span class="sxs-lookup"><span data-stu-id="2e774-318">public void context()</span></span>                                                                                       | <span data-ttu-id="2e774-319">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-319">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2e774-320">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="2e774-320">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="2e774-321">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-321">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="2e774-322">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2e774-322">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="2e774-323">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-323">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="2e774-324">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="2e774-324">public void displayControl()</span></span>                                                                                | <span data-ttu-id="2e774-325">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-325">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="2e774-326">public void paste()</span><span class="sxs-lookup"><span data-stu-id="2e774-326">public void paste()</span></span>                                                                                         | <span data-ttu-id="2e774-327">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2e774-327">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="2e774-328">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="2e774-328">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="2e774-329">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="2e774-329">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |

## <a name="method-acquirefocus"></a><span data-ttu-id="2e774-330">メソッド acquireFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-330">Method acquireFocus</span></span>

```xpp
public int acquireFocus([int value])
```

### <a name="parameters---acquirefocus"></a><span data-ttu-id="2e774-331">パラメーター - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-331">Parameters - acquireFocus</span></span>

<span data-ttu-id="2e774-332">値</span><span class="sxs-lookup"><span data-stu-id="2e774-332">value</span></span>  

### <a name="return-value---acquirefocus"></a><span data-ttu-id="2e774-333">戻り値 - acquireFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-333">Return Value - acquireFocus</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="2e774-334">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="2e774-334">Method alignControl</span></span>

<span data-ttu-id="2e774-335">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-335">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="2e774-336">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="2e774-336">Parameters - alignControl</span></span>

<span data-ttu-id="2e774-337">値</span><span class="sxs-lookup"><span data-stu-id="2e774-337">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="2e774-338">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2e774-338">Return Value - alignControl</span></span>

<span data-ttu-id="2e774-339">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2e774-339">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="2e774-340">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2e774-340">Remarks - alignControl</span></span>

<span data-ttu-id="2e774-341">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-341">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="2e774-342">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="2e774-342">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="2e774-343">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="2e774-343">Parameters - alignment</span></span>

<span data-ttu-id="2e774-344">値</span><span class="sxs-lookup"><span data-stu-id="2e774-344">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="2e774-345">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="2e774-345">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="2e774-346">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="2e774-346">Method allowEdit</span></span>

<span data-ttu-id="2e774-347">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-347">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="2e774-348">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2e774-348">Parameters - allowEdit</span></span>

<span data-ttu-id="2e774-349">値</span><span class="sxs-lookup"><span data-stu-id="2e774-349">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="2e774-350">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2e774-350">Return Value - allowEdit</span></span>

<span data-ttu-id="2e774-351">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-351">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="2e774-352">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2e774-352">Remarks - allowEdit</span></span>

<span data-ttu-id="2e774-353">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="2e774-353">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="2e774-354">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="2e774-354">Method allowSysSetup</span></span>

<span data-ttu-id="2e774-355">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-355">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="2e774-356">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="2e774-356">Return Value - allowSysSetup</span></span>

<span data-ttu-id="2e774-357">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-357">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="2e774-358">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2e774-358">Method autoDeclaration</span></span>

<span data-ttu-id="2e774-359">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-359">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="2e774-360">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2e774-360">Parameters - autoDeclaration</span></span>

<span data-ttu-id="2e774-361">値</span><span class="sxs-lookup"><span data-stu-id="2e774-361">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="2e774-362">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2e774-362">Return Value - autoDeclaration</span></span>

<span data-ttu-id="2e774-363">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-363">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="2e774-364">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2e774-364">Remarks - autoDeclaration</span></span>

<span data-ttu-id="2e774-365">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="2e774-365">Controls cannot have identical names.</span></span>

## <a name="method-autorefreshdata"></a><span data-ttu-id="2e774-366">メソッド autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="2e774-366">Method autoRefreshData</span></span>

```xpp
public boolean autoRefreshData([boolean value])
```

### <a name="parameters---autorefreshdata"></a><span data-ttu-id="2e774-367">パラメーター - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="2e774-367">Parameters - autoRefreshData</span></span>

<span data-ttu-id="2e774-368">値</span><span class="sxs-lookup"><span data-stu-id="2e774-368">value</span></span>  

### <a name="return-value---autorefreshdata"></a><span data-ttu-id="2e774-369">戻り値 - autoRefreshData</span><span class="sxs-lookup"><span data-stu-id="2e774-369">Return Value - autoRefreshData</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="2e774-370">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-370">Method backgroundColor</span></span>

<span data-ttu-id="2e774-371">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-371">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="2e774-372">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-372">Parameters - backgroundColor</span></span>

<span data-ttu-id="2e774-373">値</span><span class="sxs-lookup"><span data-stu-id="2e774-373">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="2e774-374">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-374">Return Value - backgroundColor</span></span>

<span data-ttu-id="2e774-375">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="2e774-375">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="2e774-376">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-376">Remarks - backgroundColor</span></span>

<span data-ttu-id="2e774-377">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e774-377">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="2e774-378">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e774-378">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="2e774-379">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2e774-379">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="2e774-380">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2e774-380">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="2e774-381">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2e774-381">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="2e774-382">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="2e774-382">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="2e774-383">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="2e774-383">Method backStyle</span></span>

<span data-ttu-id="2e774-384">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-384">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="2e774-385">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="2e774-385">Parameters - backStyle</span></span>

<span data-ttu-id="2e774-386">値</span><span class="sxs-lookup"><span data-stu-id="2e774-386">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="2e774-387">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="2e774-387">Return Value - backStyle</span></span>

<span data-ttu-id="2e774-388">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="2e774-388">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="2e774-389">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="2e774-389">Method beginDrag</span></span>

<span data-ttu-id="2e774-390">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-390">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="2e774-391">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="2e774-391">Parameters - beginDrag</span></span>

<span data-ttu-id="2e774-392">x</span><span class="sxs-lookup"><span data-stu-id="2e774-392">x</span></span>  
<span data-ttu-id="2e774-393">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-393">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="2e774-394">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="2e774-394">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="2e774-395">y</span><span class="sxs-lookup"><span data-stu-id="2e774-395">y</span></span>  
<span data-ttu-id="2e774-396">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-396">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="2e774-397">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="2e774-397">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="2e774-398">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="2e774-398">Return Value - beginDrag</span></span>

<span data-ttu-id="2e774-399">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2e774-399">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="2e774-400">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="2e774-400">Remarks - beginDrag</span></span>

<span data-ttu-id="2e774-401">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="2e774-401">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="2e774-402">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="2e774-402">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-big"></a><span data-ttu-id="2e774-403">メソッド big</span><span class="sxs-lookup"><span data-stu-id="2e774-403">Method big</span></span>

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a><span data-ttu-id="2e774-404">パラメーター - big</span><span class="sxs-lookup"><span data-stu-id="2e774-404">Parameters - big</span></span>

<span data-ttu-id="2e774-405">値</span><span class="sxs-lookup"><span data-stu-id="2e774-405">value</span></span>  

### <a name="return-value---big"></a><span data-ttu-id="2e774-406">戻り値 - big</span><span class="sxs-lookup"><span data-stu-id="2e774-406">Return Value - big</span></span>

## <a name="method-bold"></a><span data-ttu-id="2e774-407">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="2e774-407">Method bold</span></span>

<span data-ttu-id="2e774-408">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-408">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="2e774-409">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="2e774-409">Parameters - bold</span></span>

<span data-ttu-id="2e774-410">値</span><span class="sxs-lookup"><span data-stu-id="2e774-410">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="2e774-411">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="2e774-411">Return Value - bold</span></span>

<span data-ttu-id="2e774-412">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-412">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="2e774-413">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="2e774-413">Remarks - bold</span></span>

<span data-ttu-id="2e774-414">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e774-414">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="2e774-415">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="2e774-415">0 Use the default font weight.</span></span>
-   <span data-ttu-id="2e774-416">1 シン。</span><span class="sxs-lookup"><span data-stu-id="2e774-416">1 Thin.</span></span>
-   <span data-ttu-id="2e774-417">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="2e774-417">2 Extra-light.</span></span>
-   <span data-ttu-id="2e774-418">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="2e774-418">3 Light.</span></span>
-   <span data-ttu-id="2e774-419">4 標準。</span><span class="sxs-lookup"><span data-stu-id="2e774-419">4 Normal.</span></span>
-   <span data-ttu-id="2e774-420">5 中。</span><span class="sxs-lookup"><span data-stu-id="2e774-420">5 Medium.</span></span>
-   <span data-ttu-id="2e774-421">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="2e774-421">6 Semibold.</span></span>
-   <span data-ttu-id="2e774-422">7 太字。</span><span class="sxs-lookup"><span data-stu-id="2e774-422">7 Bold.</span></span>
-   <span data-ttu-id="2e774-423">8 極太。</span><span class="sxs-lookup"><span data-stu-id="2e774-423">8 Extra-bold.</span></span>
-   <span data-ttu-id="2e774-424">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="2e774-424">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="2e774-425">メソッド border</span><span class="sxs-lookup"><span data-stu-id="2e774-425">Method border</span></span>

<span data-ttu-id="2e774-426">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-426">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="2e774-427">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="2e774-427">Parameters - border</span></span>

<span data-ttu-id="2e774-428">値</span><span class="sxs-lookup"><span data-stu-id="2e774-428">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="2e774-429">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="2e774-429">Return Value - border</span></span>

<span data-ttu-id="2e774-430">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="2e774-430">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="2e774-431">備考 - border</span><span class="sxs-lookup"><span data-stu-id="2e774-431">Remarks - border</span></span>

<span data-ttu-id="2e774-432">返される整数値には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e774-432">The Integer value that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="2e774-433">値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-433">Value.</span></span> | <span data-ttu-id="2e774-434">説明。</span><span class="sxs-lookup"><span data-stu-id="2e774-434">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="2e774-435">0</span><span class="sxs-lookup"><span data-stu-id="2e774-435">0</span></span>      | <span data-ttu-id="2e774-436">自動。</span><span class="sxs-lookup"><span data-stu-id="2e774-436">Auto.</span></span>        |
| <span data-ttu-id="2e774-437">1</span><span class="sxs-lookup"><span data-stu-id="2e774-437">1</span></span>      | <span data-ttu-id="2e774-438">3D。</span><span class="sxs-lookup"><span data-stu-id="2e774-438">3D.</span></span>          |
| <span data-ttu-id="2e774-439">2</span><span class="sxs-lookup"><span data-stu-id="2e774-439">2</span></span>      | <span data-ttu-id="2e774-440">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="2e774-440">Single line.</span></span> |
| <span data-ttu-id="2e774-441">3</span><span class="sxs-lookup"><span data-stu-id="2e774-441">3</span></span>      | <span data-ttu-id="2e774-442">均一。</span><span class="sxs-lookup"><span data-stu-id="2e774-442">Flat.</span></span>        |
| <span data-ttu-id="2e774-443">4</span><span class="sxs-lookup"><span data-stu-id="2e774-443">4</span></span>      | <span data-ttu-id="2e774-444">なし。</span><span class="sxs-lookup"><span data-stu-id="2e774-444">None.</span></span>        |

## <a name="method-buttondisplay"></a><span data-ttu-id="2e774-445">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="2e774-445">Method buttonDisplay</span></span>

<span data-ttu-id="2e774-446">ボタン コントロールの外観を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-446">Gets or sets the appearance of the button control.</span></span>

```xpp
public int buttonDisplay([int value])
```

### <a name="parameters---buttondisplay"></a><span data-ttu-id="2e774-447">パラメーター - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="2e774-447">Parameters - buttonDisplay</span></span>

<span data-ttu-id="2e774-448">値</span><span class="sxs-lookup"><span data-stu-id="2e774-448">value</span></span>  

### <a name="return-value---buttondisplay"></a><span data-ttu-id="2e774-449">戻り値 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="2e774-449">Return Value - buttonDisplay</span></span>

<span data-ttu-id="2e774-450">ゼロから 5 までの整数。</span><span class="sxs-lookup"><span data-stu-id="2e774-450">An integer between zero and five, inclusive.</span></span>

### <a name="remarks---buttondisplay"></a><span data-ttu-id="2e774-451">備考 - buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="2e774-451">Remarks - buttonDisplay</span></span>

<span data-ttu-id="2e774-452">プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="2e774-452">The value of the property defines whether the text, the image, or both should be displayed on the button.</span></span> <span data-ttu-id="2e774-453">このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。</span><span class="sxs-lookup"><span data-stu-id="2e774-453">This property also controls relative positions of text and image if both are displayed.</span></span> <span data-ttu-id="2e774-454">返される整数値には、次のようなボタン コントロールの外観が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e774-454">The integer value that is returned contains the appearance of the button control as follows:</span></span>

| <span data-ttu-id="2e774-455">値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-455">Value.</span></span> | <span data-ttu-id="2e774-456">説明。</span><span class="sxs-lookup"><span data-stu-id="2e774-456">Description.</span></span>                                                     |
|--------|------------------------------------------------------------------|
| <span data-ttu-id="2e774-457">0</span><span class="sxs-lookup"><span data-stu-id="2e774-457">0</span></span>      | <span data-ttu-id="2e774-458">テキストのみ。</span><span class="sxs-lookup"><span data-stu-id="2e774-458">Text only.</span></span>                                                       |
| <span data-ttu-id="2e774-459">1</span><span class="sxs-lookup"><span data-stu-id="2e774-459">1</span></span>      | <span data-ttu-id="2e774-460">イメージのみ。</span><span class="sxs-lookup"><span data-stu-id="2e774-460">Image Only.</span></span>                                                      |
| <span data-ttu-id="2e774-461">2</span><span class="sxs-lookup"><span data-stu-id="2e774-461">2</span></span>      | <span data-ttu-id="2e774-462">テキストと画像。画像はテキストの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-462">Text and image; the image is displayed under the text.</span></span>           |
| <span data-ttu-id="2e774-463">3</span><span class="sxs-lookup"><span data-stu-id="2e774-463">3</span></span>      | <span data-ttu-id="2e774-464">テキストと画像。画像はテキストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-464">Text and image; the image is displayed above the text.</span></span>           |
| <span data-ttu-id="2e774-465">4</span><span class="sxs-lookup"><span data-stu-id="2e774-465">4</span></span>      | <span data-ttu-id="2e774-466">テキストと画像。画像はテキストの左に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-466">Text and image; the image is displayed to the left of the text.</span></span>  |
| <span data-ttu-id="2e774-467">5</span><span class="sxs-lookup"><span data-stu-id="2e774-467">5</span></span>      | <span data-ttu-id="2e774-468">テキストと画像。画像はテキストの右に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-468">Text and image; the image is displayed to the right of the text.</span></span> |

## <a name="method-calccontrolsize"></a><span data-ttu-id="2e774-469">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="2e774-469">Method calcControlSize</span></span>

<span data-ttu-id="2e774-470">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-470">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="2e774-471">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="2e774-471">Parameters - calcControlSize</span></span>

<span data-ttu-id="2e774-472">chars</span><span class="sxs-lookup"><span data-stu-id="2e774-472">chars</span></span>  
<span data-ttu-id="2e774-473">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="2e774-473">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="2e774-474">明細行</span><span class="sxs-lookup"><span data-stu-id="2e774-474">lines</span></span>  
<span data-ttu-id="2e774-475">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="2e774-475">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="2e774-476">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="2e774-476">Return Value - calcControlSize</span></span>

<span data-ttu-id="2e774-477">幅と高さのあるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="2e774-477">The container that has the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="2e774-478">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="2e774-478">Method characterSet</span></span>

<span data-ttu-id="2e774-479">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-479">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="2e774-480">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="2e774-480">Parameters - characterSet</span></span>

<span data-ttu-id="2e774-481">値</span><span class="sxs-lookup"><span data-stu-id="2e774-481">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="2e774-482">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="2e774-482">Return Value - characterSet</span></span>

<span data-ttu-id="2e774-483">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-483">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="2e774-484">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="2e774-484">Remarks - characterSet</span></span>

<span data-ttu-id="2e774-485">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-485">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="2e774-486">値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-486">Value.</span></span> | <span data-ttu-id="2e774-487">説明。</span><span class="sxs-lookup"><span data-stu-id="2e774-487">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="2e774-488">0</span><span class="sxs-lookup"><span data-stu-id="2e774-488">0</span></span>      | <span data-ttu-id="2e774-489">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-489">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="2e774-490">1</span><span class="sxs-lookup"><span data-stu-id="2e774-490">1</span></span>      | <span data-ttu-id="2e774-491">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-491">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="2e774-492">2</span><span class="sxs-lookup"><span data-stu-id="2e774-492">2</span></span>      | <span data-ttu-id="2e774-493">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-493">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="2e774-494">77</span><span class="sxs-lookup"><span data-stu-id="2e774-494">77</span></span>     | <span data-ttu-id="2e774-495">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-495">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="2e774-496">128</span><span class="sxs-lookup"><span data-stu-id="2e774-496">128</span></span>    | <span data-ttu-id="2e774-497">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-497">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="2e774-498">129</span><span class="sxs-lookup"><span data-stu-id="2e774-498">129</span></span>    | <span data-ttu-id="2e774-499">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-499">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="2e774-500">134</span><span class="sxs-lookup"><span data-stu-id="2e774-500">134</span></span>    | <span data-ttu-id="2e774-501">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-501">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="2e774-502">136</span><span class="sxs-lookup"><span data-stu-id="2e774-502">136</span></span>    | <span data-ttu-id="2e774-503">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-503">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="2e774-504">161</span><span class="sxs-lookup"><span data-stu-id="2e774-504">161</span></span>    | <span data-ttu-id="2e774-505">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-505">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="2e774-506">162</span><span class="sxs-lookup"><span data-stu-id="2e774-506">162</span></span>    | <span data-ttu-id="2e774-507">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-507">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="2e774-508">163</span><span class="sxs-lookup"><span data-stu-id="2e774-508">163</span></span>    | <span data-ttu-id="2e774-509">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-509">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="2e774-510">186</span><span class="sxs-lookup"><span data-stu-id="2e774-510">186</span></span>    | <span data-ttu-id="2e774-511">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-511">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="2e774-512">204</span><span class="sxs-lookup"><span data-stu-id="2e774-512">204</span></span>    | <span data-ttu-id="2e774-513">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-513">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="2e774-514">238</span><span class="sxs-lookup"><span data-stu-id="2e774-514">238</span></span>    | <span data-ttu-id="2e774-515">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-515">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="2e774-516">255</span><span class="sxs-lookup"><span data-stu-id="2e774-516">255</span></span>    | <span data-ttu-id="2e774-517">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-517">OEM\_CHARSET</span></span>         |

<span data-ttu-id="2e774-518">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-518">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="2e774-519">値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-519">Value.</span></span> | <span data-ttu-id="2e774-520">説明。</span><span class="sxs-lookup"><span data-stu-id="2e774-520">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="2e774-521">130</span><span class="sxs-lookup"><span data-stu-id="2e774-521">130</span></span>    | <span data-ttu-id="2e774-522">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-522">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="2e774-523">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-523">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="2e774-524">値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-524">Value.</span></span> | <span data-ttu-id="2e774-525">説明。</span><span class="sxs-lookup"><span data-stu-id="2e774-525">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="2e774-526">177</span><span class="sxs-lookup"><span data-stu-id="2e774-526">177</span></span>    | <span data-ttu-id="2e774-527">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-527">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="2e774-528">178</span><span class="sxs-lookup"><span data-stu-id="2e774-528">178</span></span>    | <span data-ttu-id="2e774-529">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-529">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="2e774-530">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-530">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="2e774-531">値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-531">Value.</span></span> | <span data-ttu-id="2e774-532">説明。</span><span class="sxs-lookup"><span data-stu-id="2e774-532">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="2e774-533">222</span><span class="sxs-lookup"><span data-stu-id="2e774-533">222</span></span>    | <span data-ttu-id="2e774-534">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2e774-534">THAI\_CHARSET</span></span> |

<span data-ttu-id="2e774-535">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-535">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="2e774-536">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-536">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="2e774-537">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e774-537">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="2e774-538">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="2e774-538">Method colorScheme</span></span>

<span data-ttu-id="2e774-539">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-539">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="2e774-540">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2e774-540">Parameters - colorScheme</span></span>

<span data-ttu-id="2e774-541">値</span><span class="sxs-lookup"><span data-stu-id="2e774-541">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="2e774-542">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2e774-542">Return Value - colorScheme</span></span>

<span data-ttu-id="2e774-543">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="2e774-543">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="2e774-544">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2e774-544">Remarks - colorScheme</span></span>

<span data-ttu-id="2e774-545">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-545">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="2e774-546">値です。</span><span class="sxs-lookup"><span data-stu-id="2e774-546">Value.</span></span> | <span data-ttu-id="2e774-547">スタイル。</span><span class="sxs-lookup"><span data-stu-id="2e774-547">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="2e774-548">0</span><span class="sxs-lookup"><span data-stu-id="2e774-548">0</span></span>      | <span data-ttu-id="2e774-549">既定。</span><span class="sxs-lookup"><span data-stu-id="2e774-549">Default.</span></span>                      |
| <span data-ttu-id="2e774-550">1</span><span class="sxs-lookup"><span data-stu-id="2e774-550">1</span></span>      | <span data-ttu-id="2e774-551">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="2e774-551">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="2e774-552">2</span><span class="sxs-lookup"><span data-stu-id="2e774-552">2</span></span>      | <span data-ttu-id="2e774-553">真の配色。</span><span class="sxs-lookup"><span data-stu-id="2e774-553">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="2e774-554">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="2e774-554">Method configurationKey</span></span>

<span data-ttu-id="2e774-555">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-555">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="2e774-556">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2e774-556">Parameters - configurationKey</span></span>

<span data-ttu-id="2e774-557">値</span><span class="sxs-lookup"><span data-stu-id="2e774-557">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="2e774-558">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2e774-558">Return Value - configurationKey</span></span>

<span data-ttu-id="2e774-559">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="2e774-559">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="2e774-560">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2e774-560">Remarks - configurationKey</span></span>

<span data-ttu-id="2e774-561">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-561">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="2e774-562">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="2e774-562">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="2e774-563">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="2e774-563">Method configurationKeyEx</span></span>

<span data-ttu-id="2e774-564">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-564">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="2e774-565">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="2e774-565">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="2e774-566">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="2e774-566">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="2e774-567">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="2e774-567">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="2e774-568">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="2e774-568">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="2e774-569">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e774-569">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="2e774-570">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e774-570">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="2e774-571">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2e774-571">Method countryRegionCodes</span></span>

<span data-ttu-id="2e774-572">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-572">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="2e774-573">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2e774-573">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="2e774-574">値</span><span class="sxs-lookup"><span data-stu-id="2e774-574">value</span></span>  
<span data-ttu-id="2e774-575">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-575">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="2e774-576">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2e774-576">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="2e774-577">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="2e774-577">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="2e774-578">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2e774-578">Method dataRelationPath</span></span>

<span data-ttu-id="2e774-579">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-579">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="2e774-580">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2e774-580">Parameters - dataRelationPath</span></span>

<span data-ttu-id="2e774-581">値</span><span class="sxs-lookup"><span data-stu-id="2e774-581">value</span></span>  
<span data-ttu-id="2e774-582">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-582">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="2e774-583">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2e774-583">Return Value - dataRelationPath</span></span>

<span data-ttu-id="2e774-584">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="2e774-584">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="2e774-585">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2e774-585">Remarks - dataRelationPath</span></span>

<span data-ttu-id="2e774-586">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="2e774-586">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="2e774-587">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="2e774-587">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-defaultbutton"></a><span data-ttu-id="2e774-588">メソッド defaultButton</span><span class="sxs-lookup"><span data-stu-id="2e774-588">Method defaultButton</span></span>

<span data-ttu-id="2e774-589">ボタンをフォーム上の既定のボタンにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-589">Determines whether the button should be the default button on the form.</span></span>

```xpp
public boolean defaultButton([boolean value])
```

### <a name="parameters---defaultbutton"></a><span data-ttu-id="2e774-590">パラメーター - defaultButton</span><span class="sxs-lookup"><span data-stu-id="2e774-590">Parameters - defaultButton</span></span>

<span data-ttu-id="2e774-591">値</span><span class="sxs-lookup"><span data-stu-id="2e774-591">value</span></span>  

### <a name="return-value---defaultbutton"></a><span data-ttu-id="2e774-592">戻り値 - defaultButton</span><span class="sxs-lookup"><span data-stu-id="2e774-592">Return Value - defaultButton</span></span>

<span data-ttu-id="2e774-593">ボタンが既定のボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-593">true if the button should be the default button; otherwise, false.</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="2e774-594">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="2e774-594">Method disabledImage</span></span>

<span data-ttu-id="2e774-595">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-595">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="2e774-596">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="2e774-596">Parameters - disabledImage</span></span>

<span data-ttu-id="2e774-597">値</span><span class="sxs-lookup"><span data-stu-id="2e774-597">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="2e774-598">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="2e774-598">Return Value - disabledImage</span></span>

<span data-ttu-id="2e774-599">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="2e774-599">The full name of an image file.</span></span> <span data-ttu-id="2e774-600">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2e774-600">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="2e774-601">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="2e774-601">Remarks - disabledImage</span></span>

<span data-ttu-id="2e774-602">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="2e774-602">This property has precedence over the disabledResource property.</span></span> <span data-ttu-id="2e774-603">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-603">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="2e774-604">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="2e774-604">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="2e774-605">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="2e774-605">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="2e774-606">値</span><span class="sxs-lookup"><span data-stu-id="2e774-606">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="2e774-607">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="2e774-607">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="2e774-608">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="2e774-608">Method disabledResource</span></span>

<span data-ttu-id="2e774-609">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-609">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="2e774-610">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="2e774-610">Parameters - disabledResource</span></span>

<span data-ttu-id="2e774-611">値</span><span class="sxs-lookup"><span data-stu-id="2e774-611">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="2e774-612">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="2e774-612">Return Value - disabledResource</span></span>

<span data-ttu-id="2e774-613">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="2e774-613">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="2e774-614">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2e774-614">Both icon and bitmap images are supported.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="2e774-615">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="2e774-615">Method displayTarget</span></span>

<span data-ttu-id="2e774-616">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-616">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="2e774-617">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2e774-617">Parameters - displayTarget</span></span>

<span data-ttu-id="2e774-618">値</span><span class="sxs-lookup"><span data-stu-id="2e774-618">value</span></span>  
<span data-ttu-id="2e774-619">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-619">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="2e774-620">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2e774-620">Return Value - displayTarget</span></span>

<span data-ttu-id="2e774-621">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値</span><span class="sxs-lookup"><span data-stu-id="2e774-621">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="2e774-622">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="2e774-622">Method dragDrop</span></span>

<span data-ttu-id="2e774-623">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-623">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="2e774-624">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2e774-624">Parameters - dragDrop</span></span>

<span data-ttu-id="2e774-625">値</span><span class="sxs-lookup"><span data-stu-id="2e774-625">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="2e774-626">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2e774-626">Return Value - dragDrop</span></span>

<span data-ttu-id="2e774-627">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="2e774-627">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="2e774-628">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="2e774-628">Method dragOver</span></span>

<span data-ttu-id="2e774-629">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-629">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="2e774-630">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="2e774-630">Parameters - dragOver</span></span>

<span data-ttu-id="2e774-631">dragSource</span><span class="sxs-lookup"><span data-stu-id="2e774-631">dragSource</span></span>  
<span data-ttu-id="2e774-632">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-632">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-633">dragMode</span><span class="sxs-lookup"><span data-stu-id="2e774-633">dragMode</span></span>  
<span data-ttu-id="2e774-634">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-634">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-635">x</span><span class="sxs-lookup"><span data-stu-id="2e774-635">x</span></span>  
<span data-ttu-id="2e774-636">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-636">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-637">y</span><span class="sxs-lookup"><span data-stu-id="2e774-637">y</span></span>  
<span data-ttu-id="2e774-638">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-638">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="2e774-639">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="2e774-639">Return Value - dragOver</span></span>

<span data-ttu-id="2e774-640">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="2e774-640">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="2e774-641">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="2e774-641">Method dragOverEx</span></span>

<span data-ttu-id="2e774-642">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-642">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="2e774-643">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="2e774-643">Parameters - dragOverEx</span></span>

<span data-ttu-id="2e774-644">dragSource</span><span class="sxs-lookup"><span data-stu-id="2e774-644">dragSource</span></span>  
<span data-ttu-id="2e774-645">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-645">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-646">dragMode</span><span class="sxs-lookup"><span data-stu-id="2e774-646">dragMode</span></span>  
<span data-ttu-id="2e774-647">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-647">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-648">x</span><span class="sxs-lookup"><span data-stu-id="2e774-648">x</span></span>  
<span data-ttu-id="2e774-649">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-649">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-650">y</span><span class="sxs-lookup"><span data-stu-id="2e774-650">y</span></span>  
<span data-ttu-id="2e774-651">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-651">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="2e774-652">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="2e774-652">Return Value - dragOverEx</span></span>

<span data-ttu-id="2e774-653">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="2e774-653">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="2e774-654">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="2e774-654">Method dragText</span></span>

<span data-ttu-id="2e774-655">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-655">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="2e774-656">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="2e774-656">Return Value - dragText</span></span>

<span data-ttu-id="2e774-657">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="2e774-657">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="2e774-658">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="2e774-658">Method enabled</span></span>

<span data-ttu-id="2e774-659">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-659">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="2e774-660">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="2e774-660">Parameters - enabled</span></span>

<span data-ttu-id="2e774-661">値</span><span class="sxs-lookup"><span data-stu-id="2e774-661">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="2e774-662">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="2e774-662">Return Value - enabled</span></span>

<span data-ttu-id="2e774-663">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-663">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="2e774-664">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="2e774-664">Remarks - enabled</span></span>

<span data-ttu-id="2e774-665">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="2e774-665">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="2e774-666">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2e774-666">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="2e774-667">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="2e774-667">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="2e774-668">メソッド font</span><span class="sxs-lookup"><span data-stu-id="2e774-668">Method font</span></span>

<span data-ttu-id="2e774-669">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-669">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="2e774-670">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="2e774-670">Parameters - font</span></span>

<span data-ttu-id="2e774-671">値</span><span class="sxs-lookup"><span data-stu-id="2e774-671">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="2e774-672">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="2e774-672">Return Value - font</span></span>

<span data-ttu-id="2e774-673">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="2e774-673">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="2e774-674">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="2e774-674">Method fontSize</span></span>

<span data-ttu-id="2e774-675">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-675">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="2e774-676">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="2e774-676">Parameters - fontSize</span></span>

<span data-ttu-id="2e774-677">値</span><span class="sxs-lookup"><span data-stu-id="2e774-677">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="2e774-678">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="2e774-678">Return Value - fontSize</span></span>

<span data-ttu-id="2e774-679">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="2e774-679">The height of the font in points.</span></span>

## <a name="method-forcedtooverflow"></a><span data-ttu-id="2e774-680">メソッド forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="2e774-680">Method forcedToOverflow</span></span>

```xpp
public boolean forcedToOverflow([boolean value])
```

### <a name="parameters---forcedtooverflow"></a><span data-ttu-id="2e774-681">パラメーター - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="2e774-681">Parameters - forcedToOverflow</span></span>

<span data-ttu-id="2e774-682">値</span><span class="sxs-lookup"><span data-stu-id="2e774-682">value</span></span>  

### <a name="return-value---forcedtooverflow"></a><span data-ttu-id="2e774-683">戻り値 - forcedToOverflow</span><span class="sxs-lookup"><span data-stu-id="2e774-683">Return Value - forcedToOverflow</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="2e774-684">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-684">Method foregroundColor</span></span>

<span data-ttu-id="2e774-685">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-685">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="2e774-686">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-686">Parameters - foregroundColor</span></span>

<span data-ttu-id="2e774-687">値</span><span class="sxs-lookup"><span data-stu-id="2e774-687">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="2e774-688">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-688">Return Value - foregroundColor</span></span>

<span data-ttu-id="2e774-689">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="2e774-689">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="2e774-690">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="2e774-690">Remarks - foregroundColor</span></span>

<span data-ttu-id="2e774-691">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e774-691">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="2e774-692">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e774-692">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="2e774-693">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2e774-693">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="2e774-694">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2e774-694">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="2e774-695">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2e774-695">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="2e774-696">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="2e774-696">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="2e774-697">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="2e774-697">Method hasChanged</span></span>

<span data-ttu-id="2e774-698">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-698">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="2e774-699">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="2e774-699">Parameters - hasChanged</span></span>

<span data-ttu-id="2e774-700">val</span><span class="sxs-lookup"><span data-stu-id="2e774-700">val</span></span>  
<span data-ttu-id="2e774-701">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-701">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="2e774-702">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="2e774-702">Return Value - hasChanged</span></span>

<span data-ttu-id="2e774-703">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-703">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="2e774-704">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="2e774-704">Method hasUserSetting</span></span>

<span data-ttu-id="2e774-705">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-705">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="2e774-706">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="2e774-706">Return Value - hasUserSetting</span></span>

<span data-ttu-id="2e774-707">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-707">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="2e774-708">メソッド height</span><span class="sxs-lookup"><span data-stu-id="2e774-708">Method height</span></span>

<span data-ttu-id="2e774-709">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-709">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="2e774-710">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="2e774-710">Parameters - height</span></span>

<span data-ttu-id="2e774-711">値</span><span class="sxs-lookup"><span data-stu-id="2e774-711">value</span></span>  

<!-- -->

<span data-ttu-id="2e774-712">モード</span><span class="sxs-lookup"><span data-stu-id="2e774-712">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="2e774-713">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="2e774-713">Return Value - height</span></span>

<span data-ttu-id="2e774-714">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="2e774-714">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="2e774-715">備考 - height</span><span class="sxs-lookup"><span data-stu-id="2e774-715">Remarks - height</span></span>

<span data-ttu-id="2e774-716">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-716">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2e774-717">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="2e774-717">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="2e774-718">モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-718">Mode.</span></span>            | <span data-ttu-id="2e774-719">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="2e774-719">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e774-720">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="2e774-720">-1 Exact.</span></span>        | <span data-ttu-id="2e774-721">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-721">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2e774-722">0 自動。</span><span class="sxs-lookup"><span data-stu-id="2e774-722">0 Auto.</span></span>          | <span data-ttu-id="2e774-723">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-723">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2e774-724">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="2e774-724">1 Column height.</span></span> | <span data-ttu-id="2e774-725">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2e774-725">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2e774-726">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2e774-726">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="2e774-727">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="2e774-727">Method heightMode</span></span>

<span data-ttu-id="2e774-728">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-728">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="2e774-729">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="2e774-729">Parameters - heightMode</span></span>

<span data-ttu-id="2e774-730">値</span><span class="sxs-lookup"><span data-stu-id="2e774-730">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="2e774-731">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2e774-731">Return Value - heightMode</span></span>

<span data-ttu-id="2e774-732">計算モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-732">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="2e774-733">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2e774-733">Remarks - heightMode</span></span>

<span data-ttu-id="2e774-734">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="2e774-734">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="2e774-735">モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-735">Mode.</span></span>          | <span data-ttu-id="2e774-736">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="2e774-736">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e774-737">正確。</span><span class="sxs-lookup"><span data-stu-id="2e774-737">Exact.</span></span>         | <span data-ttu-id="2e774-738">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-738">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2e774-739">自動。</span><span class="sxs-lookup"><span data-stu-id="2e774-739">Auto.</span></span>          | <span data-ttu-id="2e774-740">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-740">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2e774-741">列の高さ</span><span class="sxs-lookup"><span data-stu-id="2e774-741">Column height.</span></span> | <span data-ttu-id="2e774-742">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2e774-742">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2e774-743">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2e774-743">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="2e774-744">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="2e774-744">Method heightValue</span></span>

<span data-ttu-id="2e774-745">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-745">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="2e774-746">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="2e774-746">Parameters - heightValue</span></span>

<span data-ttu-id="2e774-747">値</span><span class="sxs-lookup"><span data-stu-id="2e774-747">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="2e774-748">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2e774-748">Return Value - heightValue</span></span>

<span data-ttu-id="2e774-749">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="2e774-749">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="2e774-750">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2e774-750">Remarks - heightValue</span></span>

<span data-ttu-id="2e774-751">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="2e774-751">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="2e774-752">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="2e774-752">Method helpField</span></span>

<span data-ttu-id="2e774-753">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-753">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="2e774-754">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="2e774-754">Return Value - helpField</span></span>

<span data-ttu-id="2e774-755">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="2e774-755">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="2e774-756">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="2e774-756">Remarks - helpField</span></span>

<span data-ttu-id="2e774-757">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="2e774-757">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="2e774-758">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e774-758">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="2e774-759">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="2e774-759">Method helpText</span></span>

<span data-ttu-id="2e774-760">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-760">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="2e774-761">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="2e774-761">Parameters - helpText</span></span>

<span data-ttu-id="2e774-762">値</span><span class="sxs-lookup"><span data-stu-id="2e774-762">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="2e774-763">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="2e774-763">Return Value - helpText</span></span>

<span data-ttu-id="2e774-764">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="2e774-764">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="2e774-765">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="2e774-765">Remarks - helpText</span></span>

<span data-ttu-id="2e774-766">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-766">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="2e774-767">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="2e774-767">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="2e774-768">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2e774-768">Method hierarchyParent</span></span>

<span data-ttu-id="2e774-769">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-769">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="2e774-770">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2e774-770">Parameters - hierarchyParent</span></span>

<span data-ttu-id="2e774-771">値</span><span class="sxs-lookup"><span data-stu-id="2e774-771">value</span></span>  
<span data-ttu-id="2e774-772">コントロールの HierarchyParent 値として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="2e774-772">The value to assign as the HierarchyParent value of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="2e774-773">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2e774-773">Return Value - hierarchyParent</span></span>

<span data-ttu-id="2e774-774">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="2e774-774">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="2e774-775">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="2e774-775">Method hWnd</span></span>

<span data-ttu-id="2e774-776">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-776">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="2e774-777">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="2e774-777">Return Value - hWnd</span></span>

<span data-ttu-id="2e774-778">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="2e774-778">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="2e774-779">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="2e774-779">Remarks - hWnd</span></span>

<span data-ttu-id="2e774-780">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e774-780">The handle can be used with the Windows API.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="2e774-781">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="2e774-781">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="2e774-782">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="2e774-782">Parameters - imageLocation</span></span>

<span data-ttu-id="2e774-783">値</span><span class="sxs-lookup"><span data-stu-id="2e774-783">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="2e774-784">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="2e774-784">Return Value - imageLocation</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="2e774-785">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="2e774-785">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="2e774-786">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="2e774-786">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="2e774-787">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="2e774-787">Method isDisplayed</span></span>

<span data-ttu-id="2e774-788">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-788">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="2e774-789">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="2e774-789">Return Value - isDisplayed</span></span>

<span data-ttu-id="2e774-790">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2e774-790">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="2e774-791">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="2e774-791">Remarks - isDisplayed</span></span>

<span data-ttu-id="2e774-792">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e774-792">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="2e774-793">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="2e774-793">Method isRestricted</span></span>

<span data-ttu-id="2e774-794">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-794">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="2e774-795">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="2e774-795">Return Value - isRestricted</span></span>

<span data-ttu-id="2e774-796">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2e774-796">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="2e774-797">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2e774-797">Method isUserSetupEnabled</span></span>

<span data-ttu-id="2e774-798">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-798">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="2e774-799">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2e774-799">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="2e774-800">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="2e774-800">neededSetupRights</span></span>  
<span data-ttu-id="2e774-801">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="2e774-801">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="2e774-802">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2e774-802">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="2e774-803">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-803">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="2e774-804">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2e774-804">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="2e774-805">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e774-805">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                   |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e774-806">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="2e774-806">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="2e774-807">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="2e774-807">No changes can be made to the control.</span></span> <span data-ttu-id="2e774-808">この値が neededSetupRights パラメーターで使用されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-808">If this value is used for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="2e774-809">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="2e774-809">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="2e774-810">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="2e774-810">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="2e774-811">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="2e774-811">The user cannot move the control.</span></span>    |
| <span data-ttu-id="2e774-812">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="2e774-812">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="2e774-813">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="2e774-813">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="2e774-814">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="2e774-814">The user can also move the control.</span></span>  |

<span data-ttu-id="2e774-815">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e774-815">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="2e774-816">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="2e774-816">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="2e774-817">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="2e774-817">Parameters - italic</span></span>

<span data-ttu-id="2e774-818">値</span><span class="sxs-lookup"><span data-stu-id="2e774-818">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="2e774-819">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="2e774-819">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="2e774-820">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="2e774-820">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="2e774-821">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="2e774-821">Parameters - keyTip</span></span>

<span data-ttu-id="2e774-822">値</span><span class="sxs-lookup"><span data-stu-id="2e774-822">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="2e774-823">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="2e774-823">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="2e774-824">メソッド left</span><span class="sxs-lookup"><span data-stu-id="2e774-824">Method left</span></span>

<span data-ttu-id="2e774-825">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-825">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="2e774-826">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="2e774-826">Parameters - left</span></span>

<span data-ttu-id="2e774-827">値</span><span class="sxs-lookup"><span data-stu-id="2e774-827">value</span></span>  
<span data-ttu-id="2e774-828">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-828">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2e774-829">モード</span><span class="sxs-lookup"><span data-stu-id="2e774-829">mode</span></span>  
<span data-ttu-id="2e774-830">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-830">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="2e774-831">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="2e774-831">Return Value - left</span></span>

<span data-ttu-id="2e774-832">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="2e774-832">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="2e774-833">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="2e774-833">Method leftMode</span></span>

<span data-ttu-id="2e774-834">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-834">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="2e774-835">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="2e774-835">Parameters - leftMode</span></span>

<span data-ttu-id="2e774-836">値</span><span class="sxs-lookup"><span data-stu-id="2e774-836">value</span></span>  
<span data-ttu-id="2e774-837">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-837">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="2e774-838">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="2e774-838">Return Value - leftMode</span></span>

<span data-ttu-id="2e774-839">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-839">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="2e774-840">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="2e774-840">Method leftValue</span></span>

<span data-ttu-id="2e774-841">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-841">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="2e774-842">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="2e774-842">Parameters - leftValue</span></span>

<span data-ttu-id="2e774-843">値</span><span class="sxs-lookup"><span data-stu-id="2e774-843">value</span></span>  
<span data-ttu-id="2e774-844">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-844">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="2e774-845">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="2e774-845">Return Value - leftValue</span></span>

<span data-ttu-id="2e774-846">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="2e774-846">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="2e774-847">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="2e774-847">Method markAsUserAdd</span></span>

<span data-ttu-id="2e774-848">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="2e774-848">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="2e774-849">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="2e774-849">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="2e774-850">値</span><span class="sxs-lookup"><span data-stu-id="2e774-850">value</span></span>  
<span data-ttu-id="2e774-851">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-851">A Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="2e774-852">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="2e774-852">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="2e774-853">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-853">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="2e774-854">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2e774-854">Method mouseDblClick</span></span>

<span data-ttu-id="2e774-855">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-855">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="2e774-856">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2e774-856">Parameters - mouseDblClick</span></span>

<span data-ttu-id="2e774-857">x</span><span class="sxs-lookup"><span data-stu-id="2e774-857">x</span></span>  
<span data-ttu-id="2e774-858">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-858">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-859">y</span><span class="sxs-lookup"><span data-stu-id="2e774-859">y</span></span>  
<span data-ttu-id="2e774-860">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-860">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-861">ボタン</span><span class="sxs-lookup"><span data-stu-id="2e774-861">button</span></span>  
<span data-ttu-id="2e774-862">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-862">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-863">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2e774-863">Ctrl</span></span>  
<span data-ttu-id="2e774-864">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-864">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-865">シフト</span><span class="sxs-lookup"><span data-stu-id="2e774-865">Shift</span></span>  
<span data-ttu-id="2e774-866">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-866">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="2e774-867">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2e774-867">Return Value - mouseDblClick</span></span>

<span data-ttu-id="2e774-868">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2e774-868">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="2e774-869">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2e774-869">Remarks - mouseDblClick</span></span>

<span data-ttu-id="2e774-870">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-870">Typically, when this method is overridden, the return value from a call to super is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="2e774-871">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="2e774-871">Method mouseDown</span></span>

<span data-ttu-id="2e774-872">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-872">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="2e774-873">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="2e774-873">Parameters - mouseDown</span></span>

<span data-ttu-id="2e774-874">x</span><span class="sxs-lookup"><span data-stu-id="2e774-874">x</span></span>  
<span data-ttu-id="2e774-875">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-875">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-876">y</span><span class="sxs-lookup"><span data-stu-id="2e774-876">y</span></span>  
<span data-ttu-id="2e774-877">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-877">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-878">ボタン</span><span class="sxs-lookup"><span data-stu-id="2e774-878">button</span></span>  
<span data-ttu-id="2e774-879">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-879">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-880">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2e774-880">Ctrl</span></span>  
<span data-ttu-id="2e774-881">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-881">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-882">シフト</span><span class="sxs-lookup"><span data-stu-id="2e774-882">Shift</span></span>  
<span data-ttu-id="2e774-883">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-883">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="2e774-884">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="2e774-884">Return Value - mouseDown</span></span>

<span data-ttu-id="2e774-885">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2e774-885">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="2e774-886">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="2e774-886">Remarks - mouseDown</span></span>

<span data-ttu-id="2e774-887">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-887">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="2e774-888">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-888">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="2e774-889">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="2e774-889">Method mouseMove</span></span>

<span data-ttu-id="2e774-890">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-890">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="2e774-891">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="2e774-891">Parameters - mouseMove</span></span>

<span data-ttu-id="2e774-892">x</span><span class="sxs-lookup"><span data-stu-id="2e774-892">x</span></span>  
<span data-ttu-id="2e774-893">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-893">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-894">y</span><span class="sxs-lookup"><span data-stu-id="2e774-894">y</span></span>  
<span data-ttu-id="2e774-895">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-895">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-896">ボタン</span><span class="sxs-lookup"><span data-stu-id="2e774-896">button</span></span>  
<span data-ttu-id="2e774-897">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-897">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-898">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2e774-898">Ctrl</span></span>  
<span data-ttu-id="2e774-899">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-899">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-900">シフト</span><span class="sxs-lookup"><span data-stu-id="2e774-900">Shift</span></span>  
<span data-ttu-id="2e774-901">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-901">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="2e774-902">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="2e774-902">Return Value - mouseMove</span></span>

<span data-ttu-id="2e774-903">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2e774-903">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="2e774-904">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="2e774-904">Remarks - mouseMove</span></span>

<span data-ttu-id="2e774-905">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-905">Typically, when this method is overridden, the return value from a call to super is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="2e774-906">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="2e774-906">Method mouseUp</span></span>

<span data-ttu-id="2e774-907">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-907">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="2e774-908">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="2e774-908">Parameters - mouseUp</span></span>

<span data-ttu-id="2e774-909">x</span><span class="sxs-lookup"><span data-stu-id="2e774-909">x</span></span>  
<span data-ttu-id="2e774-910">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-910">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-911">y</span><span class="sxs-lookup"><span data-stu-id="2e774-911">y</span></span>  
<span data-ttu-id="2e774-912">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-912">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-913">ボタン</span><span class="sxs-lookup"><span data-stu-id="2e774-913">button</span></span>  
<span data-ttu-id="2e774-914">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-914">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-915">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2e774-915">Ctrl</span></span>  
<span data-ttu-id="2e774-916">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-916">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-917">シフト</span><span class="sxs-lookup"><span data-stu-id="2e774-917">Shift</span></span>  
<span data-ttu-id="2e774-918">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-918">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="2e774-919">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="2e774-919">Return Value - mouseUp</span></span>

<span data-ttu-id="2e774-920">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2e774-920">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="2e774-921">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="2e774-921">Remarks - mouseUp</span></span>

<span data-ttu-id="2e774-922">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-922">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="2e774-923">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-923">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="2e774-924">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="2e774-924">Method multiSelect</span></span>

```xpp
public int multiSelect([int value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="2e774-925">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="2e774-925">Parameters - multiSelect</span></span>

<span data-ttu-id="2e774-926">値</span><span class="sxs-lookup"><span data-stu-id="2e774-926">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="2e774-927">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="2e774-927">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="2e774-928">メソッド名</span><span class="sxs-lookup"><span data-stu-id="2e774-928">Method name</span></span>

<span data-ttu-id="2e774-929">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-929">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="2e774-930">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="2e774-930">Parameters - name</span></span>

<span data-ttu-id="2e774-931">値</span><span class="sxs-lookup"><span data-stu-id="2e774-931">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="2e774-932">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="2e774-932">Return Value - name</span></span>

<span data-ttu-id="2e774-933">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="2e774-933">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="2e774-934">備考 - name</span><span class="sxs-lookup"><span data-stu-id="2e774-934">Remarks - name</span></span>

<span data-ttu-id="2e774-935">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e774-935">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="2e774-936">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="2e774-936">Begins with a letter.</span></span>
-   <span data-ttu-id="2e774-937">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="2e774-937">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="2e774-938">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2e774-938">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="2e774-939">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="2e774-939">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="2e774-940">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="2e774-940">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="2e774-941">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="2e774-941">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="2e774-942">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2e774-942">Parameters - neededPermission</span></span>

<span data-ttu-id="2e774-943">値</span><span class="sxs-lookup"><span data-stu-id="2e774-943">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="2e774-944">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2e774-944">Return Value - neededPermission</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="2e774-945">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="2e774-945">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="2e774-946">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="2e774-946">Parameters - needsRecord</span></span>

<span data-ttu-id="2e774-947">値</span><span class="sxs-lookup"><span data-stu-id="2e774-947">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="2e774-948">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="2e774-948">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="2e774-949">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="2e774-949">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="2e774-950">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="2e774-950">Parameters - normalImage</span></span>

<span data-ttu-id="2e774-951">値</span><span class="sxs-lookup"><span data-stu-id="2e774-951">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="2e774-952">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="2e774-952">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="2e774-953">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="2e774-953">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="2e774-954">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="2e774-954">Parameters - normalResource</span></span>

<span data-ttu-id="2e774-955">値</span><span class="sxs-lookup"><span data-stu-id="2e774-955">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="2e774-956">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="2e774-956">Return Value - normalResource</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="2e774-957">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2e774-957">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="2e774-958">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2e774-958">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="2e774-959">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="2e774-959">Method parentControl</span></span>

<span data-ttu-id="2e774-960">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-960">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="2e774-961">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="2e774-961">Return Value - parentControl</span></span>

<span data-ttu-id="2e774-962">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="2e774-962">The parent control for the control.</span></span>

## <a name="method-primary"></a><span data-ttu-id="2e774-963">メソッド primary</span><span class="sxs-lookup"><span data-stu-id="2e774-963">Method primary</span></span>

```xpp
public boolean primary([boolean value])
```

### <a name="parameters---primary"></a><span data-ttu-id="2e774-964">パラメーター - primary</span><span class="sxs-lookup"><span data-stu-id="2e774-964">Parameters - primary</span></span>

<span data-ttu-id="2e774-965">値</span><span class="sxs-lookup"><span data-stu-id="2e774-965">value</span></span>  

### <a name="return-value---primary"></a><span data-ttu-id="2e774-966">戻り値 - primary</span><span class="sxs-lookup"><span data-stu-id="2e774-966">Return Value - primary</span></span>

## <a name="method-saverecord"></a><span data-ttu-id="2e774-967">メソッド saveRecord</span><span class="sxs-lookup"><span data-stu-id="2e774-967">Method saveRecord</span></span>

```xpp
public boolean saveRecord([boolean value])
```

### <a name="parameters---saverecord"></a><span data-ttu-id="2e774-968">パラメーター - saveRecord</span><span class="sxs-lookup"><span data-stu-id="2e774-968">Parameters - saveRecord</span></span>

<span data-ttu-id="2e774-969">値</span><span class="sxs-lookup"><span data-stu-id="2e774-969">value</span></span>  

### <a name="return-value---saverecord"></a><span data-ttu-id="2e774-970">戻り値 - saveRecord</span><span class="sxs-lookup"><span data-stu-id="2e774-970">Return Value - saveRecord</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="2e774-971">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="2e774-971">Method securityKey</span></span>

<span data-ttu-id="2e774-972">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-972">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="2e774-973">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="2e774-973">Parameters - securityKey</span></span>

<span data-ttu-id="2e774-974">値</span><span class="sxs-lookup"><span data-stu-id="2e774-974">value</span></span>  
<span data-ttu-id="2e774-975">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-975">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="2e774-976">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="2e774-976">Return Value - securityKey</span></span>

<span data-ttu-id="2e774-977">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="2e774-977">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-shortkey"></a><span data-ttu-id="2e774-978">メソッド shortkey</span><span class="sxs-lookup"><span data-stu-id="2e774-978">Method shortkey</span></span>

```xpp
public int shortkey([int value])
```

### <a name="parameters---shortkey"></a><span data-ttu-id="2e774-979">パラメーター - shortkey</span><span class="sxs-lookup"><span data-stu-id="2e774-979">Parameters - shortkey</span></span>

<span data-ttu-id="2e774-980">値</span><span class="sxs-lookup"><span data-stu-id="2e774-980">value</span></span>  

### <a name="return-value---shortkey"></a><span data-ttu-id="2e774-981">戻り値 - shortkey</span><span class="sxs-lookup"><span data-stu-id="2e774-981">Return Value - shortkey</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="2e774-982">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="2e774-982">Method showContextMenu</span></span>

<span data-ttu-id="2e774-983">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-983">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="2e774-984">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="2e774-984">Parameters - showContextMenu</span></span>

<span data-ttu-id="2e774-985">menuHandle</span><span class="sxs-lookup"><span data-stu-id="2e774-985">menuHandle</span></span>  
<span data-ttu-id="2e774-986">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="2e774-986">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="2e774-987">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="2e774-987">Return Value - showContextMenu</span></span>

<span data-ttu-id="2e774-988">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-988">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showshortcut"></a><span data-ttu-id="2e774-989">メソッド showShortCut</span><span class="sxs-lookup"><span data-stu-id="2e774-989">Method showShortCut</span></span>

```xpp
public boolean showShortCut([boolean value])
```

### <a name="parameters---showshortcut"></a><span data-ttu-id="2e774-990">パラメーター - showShortCut</span><span class="sxs-lookup"><span data-stu-id="2e774-990">Parameters - showShortCut</span></span>

<span data-ttu-id="2e774-991">値</span><span class="sxs-lookup"><span data-stu-id="2e774-991">value</span></span>  

### <a name="return-value---showshortcut"></a><span data-ttu-id="2e774-992">戻り値 - showShortCut</span><span class="sxs-lookup"><span data-stu-id="2e774-992">Return Value - showShortCut</span></span>

## <a name="method-skip"></a><span data-ttu-id="2e774-993">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="2e774-993">Method skip</span></span>

<span data-ttu-id="2e774-994">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-994">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="2e774-995">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="2e774-995">Parameters - skip</span></span>

<span data-ttu-id="2e774-996">値</span><span class="sxs-lookup"><span data-stu-id="2e774-996">value</span></span>  
<span data-ttu-id="2e774-997">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-997">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="2e774-998">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="2e774-998">Return Value - skip</span></span>

<span data-ttu-id="2e774-999">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e774-999">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="2e774-1000">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="2e774-1000">Remarks - skip</span></span>

<span data-ttu-id="2e774-1001">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1001">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-style"></a><span data-ttu-id="2e774-1002">メソッド style</span><span class="sxs-lookup"><span data-stu-id="2e774-1002">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="2e774-1003">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="2e774-1003">Parameters - style</span></span>

<span data-ttu-id="2e774-1004">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1004">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="2e774-1005">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="2e774-1005">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="2e774-1006">メソッド text</span><span class="sxs-lookup"><span data-stu-id="2e774-1006">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="2e774-1007">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="2e774-1007">Parameters - text</span></span>

<span data-ttu-id="2e774-1008">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1008">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="2e774-1009">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="2e774-1009">Return Value - text</span></span>

## <a name="method-togglebutton"></a><span data-ttu-id="2e774-1010">メソッド toggleButton</span><span class="sxs-lookup"><span data-stu-id="2e774-1010">Method toggleButton</span></span>

```xpp
public int toggleButton([int value])
```

### <a name="parameters---togglebutton"></a><span data-ttu-id="2e774-1011">パラメーター - toggleButton</span><span class="sxs-lookup"><span data-stu-id="2e774-1011">Parameters - toggleButton</span></span>

<span data-ttu-id="2e774-1012">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1012">value</span></span>  

### <a name="return-value---togglebutton"></a><span data-ttu-id="2e774-1013">戻り値 - toggleButton</span><span class="sxs-lookup"><span data-stu-id="2e774-1013">Return Value - toggleButton</span></span>

## <a name="method-togglevalue"></a><span data-ttu-id="2e774-1014">メソッド toggleValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1014">Method toggleValue</span></span>

```xpp
public int toggleValue([int value])
```

### <a name="parameters---togglevalue"></a><span data-ttu-id="2e774-1015">パラメーター - toggleValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1015">Parameters - toggleValue</span></span>

<span data-ttu-id="2e774-1016">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1016">value</span></span>  

### <a name="return-value---togglevalue"></a><span data-ttu-id="2e774-1017">戻り値 - toggleValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1017">Return Value - toggleValue</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="2e774-1018">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="2e774-1018">Method toolTip</span></span>

<span data-ttu-id="2e774-1019">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1019">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="2e774-1020">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="2e774-1020">Return Value - toolTip</span></span>

<span data-ttu-id="2e774-1021">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="2e774-1021">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="2e774-1022">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="2e774-1022">Remarks - toolTip</span></span>

<span data-ttu-id="2e774-1023">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1023">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="2e774-1024">メソッド top</span><span class="sxs-lookup"><span data-stu-id="2e774-1024">Method top</span></span>

<span data-ttu-id="2e774-1025">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1025">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="2e774-1026">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="2e774-1026">Parameters - top</span></span>

<span data-ttu-id="2e774-1027">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1027">value</span></span>  
<span data-ttu-id="2e774-1028">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1028">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2e774-1029">モード</span><span class="sxs-lookup"><span data-stu-id="2e774-1029">mode</span></span>  
<span data-ttu-id="2e774-1030">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1030">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="2e774-1031">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="2e774-1031">Return Value - top</span></span>

<span data-ttu-id="2e774-1032">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="2e774-1032">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="2e774-1033">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1033">Method topMode</span></span>

<span data-ttu-id="2e774-1034">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1034">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="2e774-1035">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1035">Parameters - topMode</span></span>

<span data-ttu-id="2e774-1036">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1036">value</span></span>  
<span data-ttu-id="2e774-1037">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1037">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="2e774-1038">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1038">Return Value - topMode</span></span>

<span data-ttu-id="2e774-1039">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-1039">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="2e774-1040">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1040">Method topValue</span></span>

<span data-ttu-id="2e774-1041">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1041">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="2e774-1042">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1042">Parameters - topValue</span></span>

<span data-ttu-id="2e774-1043">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1043">value</span></span>  
<span data-ttu-id="2e774-1044">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1044">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="2e774-1045">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1045">Return Value - topValue</span></span>

<span data-ttu-id="2e774-1046">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="2e774-1046">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="2e774-1047">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="2e774-1047">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="2e774-1048">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="2e774-1048">Parameters - type</span></span>

<span data-ttu-id="2e774-1049">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1049">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="2e774-1050">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="2e774-1050">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="2e774-1051">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="2e774-1051">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="2e774-1052">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="2e774-1052">Parameters - underline</span></span>

<span data-ttu-id="2e774-1053">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1053">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="2e774-1054">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="2e774-1054">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="2e774-1055">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2e774-1055">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="2e774-1056">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2e774-1056">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="2e774-1057">データ</span><span class="sxs-lookup"><span data-stu-id="2e774-1057">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="2e774-1058">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2e774-1058">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="2e774-1059">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="2e774-1059">Method userData</span></span>

<span data-ttu-id="2e774-1060">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1060">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="2e774-1061">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="2e774-1061">Parameters - userData</span></span>

<span data-ttu-id="2e774-1062">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1062">value</span></span>  
<span data-ttu-id="2e774-1063">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1063">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="2e774-1064">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="2e774-1064">Return Value - userData</span></span>

<span data-ttu-id="2e774-1065">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="2e774-1065">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="2e774-1066">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="2e774-1066">Method userDataItem</span></span>

<span data-ttu-id="2e774-1067">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1067">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="2e774-1068">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2e774-1068">Parameters - userDataItem</span></span>

<span data-ttu-id="2e774-1069">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1069">value</span></span>  
<span data-ttu-id="2e774-1070">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1070">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="2e774-1071">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2e774-1071">Return Value - userDataItem</span></span>

<span data-ttu-id="2e774-1072">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="2e774-1072">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="2e774-1073">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="2e774-1073">Method userDataItems</span></span>

<span data-ttu-id="2e774-1074">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1074">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="2e774-1075">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2e774-1075">Parameters - userDataItems</span></span>

<span data-ttu-id="2e774-1076">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1076">value</span></span>  
<span data-ttu-id="2e774-1077">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1077">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="2e774-1078">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2e774-1078">Return Value - userDataItems</span></span>

<span data-ttu-id="2e774-1079">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="2e774-1079">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="2e774-1080">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="2e774-1080">Method userDisable</span></span>

<span data-ttu-id="2e774-1081">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1081">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="2e774-1082">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="2e774-1082">Parameters - userDisable</span></span>

<span data-ttu-id="2e774-1083">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1083">value</span></span>  
<span data-ttu-id="2e774-1084">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1084">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="2e774-1085">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="2e774-1085">Return Value - userDisable</span></span>

<span data-ttu-id="2e774-1086">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="2e774-1086">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="2e774-1087">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="2e774-1087">Method userHeight</span></span>

<span data-ttu-id="2e774-1088">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1088">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="2e774-1089">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="2e774-1089">Parameters - userHeight</span></span>

<span data-ttu-id="2e774-1090">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1090">value</span></span>  
<span data-ttu-id="2e774-1091">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1091">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="2e774-1092">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="2e774-1092">Return Value - userHeight</span></span>

<span data-ttu-id="2e774-1093">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="2e774-1093">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="2e774-1094">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="2e774-1094">Method userHide</span></span>

<span data-ttu-id="2e774-1095">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1095">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="2e774-1096">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="2e774-1096">Parameters - userHide</span></span>

<span data-ttu-id="2e774-1097">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1097">value</span></span>  
<span data-ttu-id="2e774-1098">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1098">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="2e774-1099">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="2e774-1099">Return Value - userHide</span></span>

<span data-ttu-id="2e774-1100">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="2e774-1100">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="2e774-1101">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="2e774-1101">Remarks - userHide</span></span>

<span data-ttu-id="2e774-1102">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1102">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="2e774-1103">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1103">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="2e774-1104">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1104">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="2e774-1105">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="2e774-1105">Method userOrgContainer</span></span>

<span data-ttu-id="2e774-1106">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1106">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="2e774-1107">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="2e774-1107">Parameters - userOrgContainer</span></span>

<span data-ttu-id="2e774-1108">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1108">value</span></span>  
<span data-ttu-id="2e774-1109">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1109">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="2e774-1110">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="2e774-1110">Return Value - userOrgContainer</span></span>

<span data-ttu-id="2e774-1111">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="2e774-1111">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="2e774-1112">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="2e774-1112">Method userOrgSibling</span></span>

<span data-ttu-id="2e774-1113">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1113">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="2e774-1114">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="2e774-1114">Parameters - userOrgSibling</span></span>

<span data-ttu-id="2e774-1115">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1115">value</span></span>  
<span data-ttu-id="2e774-1116">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1116">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="2e774-1117">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="2e774-1117">Return Value - userOrgSibling</span></span>

<span data-ttu-id="2e774-1118">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="2e774-1118">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="2e774-1119">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="2e774-1119">Method userPromptText</span></span>

<span data-ttu-id="2e774-1120">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1120">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="2e774-1121">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="2e774-1121">Parameters - userPromptText</span></span>

<span data-ttu-id="2e774-1122">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1122">value</span></span>  
<span data-ttu-id="2e774-1123">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1123">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="2e774-1124">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="2e774-1124">Return Value - userPromptText</span></span>

<span data-ttu-id="2e774-1125">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="2e774-1125">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="2e774-1126">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="2e774-1126">Method userSecurityLevel</span></span>

<span data-ttu-id="2e774-1127">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1127">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="2e774-1128">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="2e774-1128">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="2e774-1129">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1129">value</span></span>  
<span data-ttu-id="2e774-1130">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1130">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="2e774-1131">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="2e774-1131">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="2e774-1132">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="2e774-1132">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="2e774-1133">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="2e774-1133">Method userSkip</span></span>

<span data-ttu-id="2e774-1134">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1134">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="2e774-1135">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="2e774-1135">Parameters - userSkip</span></span>

<span data-ttu-id="2e774-1136">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1136">value</span></span>  
<span data-ttu-id="2e774-1137">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1137">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="2e774-1138">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="2e774-1138">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="2e774-1139">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="2e774-1139">Return Value - userSkip</span></span>

<span data-ttu-id="2e774-1140">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="2e774-1140">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="2e774-1141">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="2e774-1141">Method userWidth</span></span>

<span data-ttu-id="2e774-1142">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1142">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="2e774-1143">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="2e774-1143">Parameters - userWidth</span></span>

<span data-ttu-id="2e774-1144">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1144">value</span></span>  
<span data-ttu-id="2e774-1145">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1145">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="2e774-1146">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="2e774-1146">Return Value - userWidth</span></span>

<span data-ttu-id="2e774-1147">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1147">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="2e774-1148">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="2e774-1148">Remarks - userWidth</span></span>

<span data-ttu-id="2e774-1149">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1149">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="2e774-1150">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="2e774-1150">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="2e774-1151">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1151">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-value"></a><span data-ttu-id="2e774-1152">メソッド value</span><span class="sxs-lookup"><span data-stu-id="2e774-1152">Method value</span></span>

```xpp
public boolean value([boolean value])
```

### <a name="parameters---value"></a><span data-ttu-id="2e774-1153">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="2e774-1153">Parameters - value</span></span>

<span data-ttu-id="2e774-1154">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1154">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="2e774-1155">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="2e774-1155">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="2e774-1156">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2e774-1156">Method verticalSpacing</span></span>

<span data-ttu-id="2e774-1157">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1157">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="2e774-1158">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2e774-1158">Parameters - verticalSpacing</span></span>

<span data-ttu-id="2e774-1159">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1159">value</span></span>  
<span data-ttu-id="2e774-1160">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1160">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2e774-1161">モード</span><span class="sxs-lookup"><span data-stu-id="2e774-1161">mode</span></span>  
<span data-ttu-id="2e774-1162">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1162">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="2e774-1163">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2e774-1163">Return Value - verticalSpacing</span></span>

<span data-ttu-id="2e774-1164">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="2e774-1164">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="2e774-1165">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1165">Method verticalSpacingMode</span></span>

<span data-ttu-id="2e774-1166">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1166">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="2e774-1167">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1167">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="2e774-1168">モード</span><span class="sxs-lookup"><span data-stu-id="2e774-1168">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="2e774-1169">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1169">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="2e774-1170">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-1170">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="2e774-1171">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1171">Method verticalSpacingValue</span></span>

<span data-ttu-id="2e774-1172">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1172">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="2e774-1173">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1173">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="2e774-1174">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1174">value</span></span>  
<span data-ttu-id="2e774-1175">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2e774-1175">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="2e774-1176">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1176">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="2e774-1177">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="2e774-1177">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="2e774-1178">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="2e774-1178">Method visible</span></span>

<span data-ttu-id="2e774-1179">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1179">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="2e774-1180">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="2e774-1180">Parameters - visible</span></span>

<span data-ttu-id="2e774-1181">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1181">value</span></span>  
<span data-ttu-id="2e774-1182">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1182">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="2e774-1183">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="2e774-1183">Return Value - visible</span></span>

<span data-ttu-id="2e774-1184">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2e774-1184">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="2e774-1185">メソッド width</span><span class="sxs-lookup"><span data-stu-id="2e774-1185">Method width</span></span>

<span data-ttu-id="2e774-1186">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1186">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="2e774-1187">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="2e774-1187">Parameters - width</span></span>

<span data-ttu-id="2e774-1188">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1188">value</span></span>  

<!-- -->

<span data-ttu-id="2e774-1189">モード</span><span class="sxs-lookup"><span data-stu-id="2e774-1189">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="2e774-1190">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="2e774-1190">Return Value - width</span></span>

<span data-ttu-id="2e774-1191">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2e774-1191">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="2e774-1192">備考 - width</span><span class="sxs-lookup"><span data-stu-id="2e774-1192">Remarks - width</span></span>

<span data-ttu-id="2e774-1193">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1193">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2e774-1194">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="2e774-1194">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="2e774-1195">モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-1195">Mode.</span></span>           | <span data-ttu-id="2e774-1196">幅計算。</span><span class="sxs-lookup"><span data-stu-id="2e774-1196">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e774-1197">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="2e774-1197">-1 Exact.</span></span>       | <span data-ttu-id="2e774-1198">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1198">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2e774-1199">0 自動。</span><span class="sxs-lookup"><span data-stu-id="2e774-1199">0 Auto.</span></span>         | <span data-ttu-id="2e774-1200">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1200">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2e774-1201">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="2e774-1201">1 Column width.</span></span> | <span data-ttu-id="2e774-1202">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2e774-1202">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2e774-1203">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1203">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="2e774-1204">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1204">Method widthMode</span></span>

<span data-ttu-id="2e774-1205">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1205">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="2e774-1206">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1206">Parameters - widthMode</span></span>

<span data-ttu-id="2e774-1207">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1207">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="2e774-1208">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1208">Return Value - widthMode</span></span>

<span data-ttu-id="2e774-1209">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1209">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="2e774-1210">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1210">Remarks - widthMode</span></span>

<span data-ttu-id="2e774-1211">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="2e774-1211">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="2e774-1212">モード。</span><span class="sxs-lookup"><span data-stu-id="2e774-1212">Mode.</span></span>         | <span data-ttu-id="2e774-1213">幅計算。</span><span class="sxs-lookup"><span data-stu-id="2e774-1213">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e774-1214">正確。</span><span class="sxs-lookup"><span data-stu-id="2e774-1214">Exact.</span></span>        | <span data-ttu-id="2e774-1215">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1215">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2e774-1216">自動。</span><span class="sxs-lookup"><span data-stu-id="2e774-1216">Auto.</span></span>         | <span data-ttu-id="2e774-1217">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1217">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2e774-1218">列の幅。</span><span class="sxs-lookup"><span data-stu-id="2e774-1218">Column width.</span></span> | <span data-ttu-id="2e774-1219">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2e774-1219">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2e774-1220">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2e774-1220">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="2e774-1221">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1221">Method widthValue</span></span>

<span data-ttu-id="2e774-1222">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1222">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="2e774-1223">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1223">Parameters - widthValue</span></span>

<span data-ttu-id="2e774-1224">値</span><span class="sxs-lookup"><span data-stu-id="2e774-1224">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="2e774-1225">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1225">Return Value - widthValue</span></span>

<span data-ttu-id="2e774-1226">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2e774-1226">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="2e774-1227">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2e774-1227">Remarks - widthValue</span></span>

<span data-ttu-id="2e774-1228">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1228">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="2e774-1229">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="2e774-1229">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="2e774-1230">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="2e774-1230">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="2e774-1231">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="2e774-1231">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="2e774-1232">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="2e774-1232">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="2e774-1233">overrideObject</span><span class="sxs-lookup"><span data-stu-id="2e774-1233">overrideObject</span></span>  

## <a name="method-copy"></a><span data-ttu-id="2e774-1234">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="2e774-1234">Method copy</span></span>

<span data-ttu-id="2e774-1235">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="2e774-1235">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="2e774-1236">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-1236">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="2e774-1237">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-1237">Parameters - OnLostFocus</span></span>

<span data-ttu-id="2e774-1238">sender</span><span class="sxs-lookup"><span data-stu-id="2e774-1238">sender</span></span>  

<!-- -->

<span data-ttu-id="2e774-1239">e</span><span class="sxs-lookup"><span data-stu-id="2e774-1239">e</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="2e774-1240">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-1240">Method gotFocus</span></span>

<span data-ttu-id="2e774-1241">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1241">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-mouseleave"></a><span data-ttu-id="2e774-1242">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="2e774-1242">Method mouseLeave</span></span>

<span data-ttu-id="2e774-1243">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1243">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="2e774-1244">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="2e774-1244">Method prefColumnSize</span></span>

<span data-ttu-id="2e774-1245">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1245">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="2e774-1246">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="2e774-1246">Parameters - prefColumnSize</span></span>

<span data-ttu-id="2e774-1247">width</span><span class="sxs-lookup"><span data-stu-id="2e774-1247">width</span></span>  
<span data-ttu-id="2e774-1248">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="2e774-1248">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="2e774-1249">height</span><span class="sxs-lookup"><span data-stu-id="2e774-1249">height</span></span>  
<span data-ttu-id="2e774-1250">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="2e774-1250">The preferred height of the control.</span></span>

## <a name="method-drop"></a><span data-ttu-id="2e774-1251">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="2e774-1251">Method drop</span></span>

<span data-ttu-id="2e774-1252">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1252">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="2e774-1253">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="2e774-1253">Parameters - drop</span></span>

<span data-ttu-id="2e774-1254">dragSource</span><span class="sxs-lookup"><span data-stu-id="2e774-1254">dragSource</span></span>  
<span data-ttu-id="2e774-1255">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1255">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-1256">dragMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1256">dragMode</span></span>  
<span data-ttu-id="2e774-1257">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1257">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-1258">x</span><span class="sxs-lookup"><span data-stu-id="2e774-1258">x</span></span>  
<span data-ttu-id="2e774-1259">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1259">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-1260">y</span><span class="sxs-lookup"><span data-stu-id="2e774-1260">y</span></span>  
<span data-ttu-id="2e774-1261">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1261">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="2e774-1262">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="2e774-1262">Method endDrag</span></span>

<span data-ttu-id="2e774-1263">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1263">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="2e774-1264">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="2e774-1264">Remarks - endDrag</span></span>

<span data-ttu-id="2e774-1265">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="2e774-1265">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="2e774-1266">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1266">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-clicked"></a><span data-ttu-id="2e774-1267">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="2e774-1267">Method clicked</span></span>

```xpp
public void clicked()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="2e774-1268">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-1268">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="2e774-1269">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-1269">Parameters - OnGotFocus</span></span>

<span data-ttu-id="2e774-1270">sender</span><span class="sxs-lookup"><span data-stu-id="2e774-1270">sender</span></span>  

<!-- -->

<span data-ttu-id="2e774-1271">e</span><span class="sxs-lookup"><span data-stu-id="2e774-1271">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="2e774-1272">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-1272">Method lostFocus</span></span>

<span data-ttu-id="2e774-1273">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1273">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-setfocus"></a><span data-ttu-id="2e774-1274">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="2e774-1274">Method setFocus</span></span>

<span data-ttu-id="2e774-1275">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1275">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="2e774-1276">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="2e774-1276">Method resetUserSetting</span></span>

<span data-ttu-id="2e774-1277">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="2e774-1277">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-dropex"></a><span data-ttu-id="2e774-1278">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="2e774-1278">Method dropEx</span></span>

<span data-ttu-id="2e774-1279">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1279">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="2e774-1280">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="2e774-1280">Parameters - dropEx</span></span>

<span data-ttu-id="2e774-1281">dragSource</span><span class="sxs-lookup"><span data-stu-id="2e774-1281">dragSource</span></span>  
<span data-ttu-id="2e774-1282">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1282">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-1283">dragMode</span><span class="sxs-lookup"><span data-stu-id="2e774-1283">dragMode</span></span>  
<span data-ttu-id="2e774-1284">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1284">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-1285">x</span><span class="sxs-lookup"><span data-stu-id="2e774-1285">x</span></span>  
<span data-ttu-id="2e774-1286">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1286">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2e774-1287">y</span><span class="sxs-lookup"><span data-stu-id="2e774-1287">y</span></span>  
<span data-ttu-id="2e774-1288">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1288">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onclicked"></a><span data-ttu-id="2e774-1289">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="2e774-1289">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="2e774-1290">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="2e774-1290">Parameters - OnClicked</span></span>

<span data-ttu-id="2e774-1291">sender</span><span class="sxs-lookup"><span data-stu-id="2e774-1291">sender</span></span>  

<!-- -->

<span data-ttu-id="2e774-1292">e</span><span class="sxs-lookup"><span data-stu-id="2e774-1292">e</span></span>  

## <a name="method-cut"></a><span data-ttu-id="2e774-1293">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="2e774-1293">Method cut</span></span>

<span data-ttu-id="2e774-1294">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="2e774-1294">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-context"></a><span data-ttu-id="2e774-1295">メソッド context</span><span class="sxs-lookup"><span data-stu-id="2e774-1295">Method context</span></span>

<span data-ttu-id="2e774-1296">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1296">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-dragleave"></a><span data-ttu-id="2e774-1297">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="2e774-1297">Method dragLeave</span></span>

<span data-ttu-id="2e774-1298">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1298">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-mouseenter"></a><span data-ttu-id="2e774-1299">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="2e774-1299">Method mouseEnter</span></span>

<span data-ttu-id="2e774-1300">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1300">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="2e774-1301">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="2e774-1301">Parameters - mouseEnter</span></span>

<span data-ttu-id="2e774-1302">x</span><span class="sxs-lookup"><span data-stu-id="2e774-1302">x</span></span>  
<span data-ttu-id="2e774-1303">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1303">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-1304">y</span><span class="sxs-lookup"><span data-stu-id="2e774-1304">y</span></span>  
<span data-ttu-id="2e774-1305">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1305">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-1306">ボタン</span><span class="sxs-lookup"><span data-stu-id="2e774-1306">button</span></span>  
<span data-ttu-id="2e774-1307">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1307">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-1308">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2e774-1308">Ctrl</span></span>  
<span data-ttu-id="2e774-1309">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1309">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2e774-1310">シフト</span><span class="sxs-lookup"><span data-stu-id="2e774-1310">Shift</span></span>  
<span data-ttu-id="2e774-1311">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2e774-1311">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="2e774-1312">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="2e774-1312">Method displayControl</span></span>

<span data-ttu-id="2e774-1313">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1313">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-paste"></a><span data-ttu-id="2e774-1314">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="2e774-1314">Method paste</span></span>

<span data-ttu-id="2e774-1315">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2e774-1315">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-inputsearch"></a><span data-ttu-id="2e774-1316">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="2e774-1316">Method inputSearch</span></span>

<span data-ttu-id="2e774-1317">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="2e774-1317">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="2e774-1318">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="2e774-1318">Parameters - inputSearch</span></span>

<span data-ttu-id="2e774-1319">searchStr</span><span class="sxs-lookup"><span data-stu-id="2e774-1319">searchStr</span></span>  
<span data-ttu-id="2e774-1320">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2e774-1320">The string value to use to filter data; optional.</span></span>

