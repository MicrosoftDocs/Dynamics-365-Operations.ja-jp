---
title: FormWindowControl クラス
description: このトピックでは、FormWindowControl クラスについて説明します。
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
ms.openlocfilehash: d6a5dc8a857d4c44320a5bc4a5172e9c6b5c56d3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502616"
---
# <a name="class-formwindowcontrol"></a><span data-ttu-id="46636-103">クラス FormWindowControl</span><span class="sxs-lookup"><span data-stu-id="46636-103">Class FormWindowControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormWindowControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="46636-104">備考</span><span class="sxs-lookup"><span data-stu-id="46636-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="46636-105">例</span><span class="sxs-lookup"><span data-stu-id="46636-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="46636-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="46636-106">Methods</span></span>

| <span data-ttu-id="46636-107">方法</span><span class="sxs-lookup"><span data-stu-id="46636-107">Method</span></span>                                                                                                                         | <span data-ttu-id="46636-108">説明</span><span class="sxs-lookup"><span data-stu-id="46636-108">Description</span></span>                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46636-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-109">public boolean alignControl(\[boolean value\])</span></span>                                                                                 | <span data-ttu-id="46636-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="46636-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                                    | <span data-ttu-id="46636-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="46636-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="46636-113">public boolean allowSysSetup()</span></span>                                                                                                 | <span data-ttu-id="46636-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="46636-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="46636-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="46636-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-117">public int backgroundColor(\[int value\])</span></span>                                                                                      | <span data-ttu-id="46636-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-118">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="46636-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-119">public int backStyle(\[int value\])</span></span>                                                                                            | <span data-ttu-id="46636-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-120">Determines whether the control background can be transparent.</span></span>                                                                                                           |
| <span data-ttu-id="46636-121">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="46636-121">public int beginDrag(int x, int y)</span></span>                                                                                             | <span data-ttu-id="46636-122">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-122">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="46636-123">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-123">public int cacheDataMethod(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="46636-124">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="46636-124">public container calcControlSize(int chars, int lines)</span></span>                                                                         | <span data-ttu-id="46636-125">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-125">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="46636-126">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-126">public int colorScheme(\[int value\])</span></span>                                                                                          | <span data-ttu-id="46636-127">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-127">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="46636-128">public int command(int wParam, int lParam)</span><span class="sxs-lookup"><span data-stu-id="46636-128">public int command(int wParam, int lParam)</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="46636-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="46636-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                                       | <span data-ttu-id="46636-130">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-130">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="46636-131">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="46636-131">public List configurationKeyEx()</span></span>                                                                                               | <span data-ttu-id="46636-132">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-132">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="46636-133">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-133">public str countryRegionCodes(\[str value\])</span></span>                                                                                   | <span data-ttu-id="46636-134">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-134">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="46636-135">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="46636-135">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-136">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="46636-136">public FieldId dataField(\[FieldId value\])</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-137">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-137">public str dataMethod(\[str value\])</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="46636-138">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-138">public str dataRelationPath(\[str value\])</span></span>                                                                                     | <span data-ttu-id="46636-139">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-139">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="46636-140">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="46636-140">public int dataSource(\[AnyType value\])</span></span>                                                                                       | <span data-ttu-id="46636-141">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-141">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="46636-142">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-142">public int displayTarget(\[int value\])</span></span>                                                                                        | <span data-ttu-id="46636-143">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-143">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="46636-144">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-144">public int dragDrop(\[int value\])</span></span>                                                                                             | <span data-ttu-id="46636-145">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-145">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="46636-146">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="46636-146">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                              | <span data-ttu-id="46636-147">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-147">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="46636-148">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="46636-148">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                                  | <span data-ttu-id="46636-149">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-149">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="46636-150">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="46636-150">public str dragText()</span></span>                                                                                                          | <span data-ttu-id="46636-151">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-151">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="46636-152">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-152">public boolean enabled(\[boolean value\])</span></span>                                                                                      | <span data-ttu-id="46636-153">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-153">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="46636-154">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-154">public int foregroundColor(\[int value\])</span></span>                                                                                      | <span data-ttu-id="46636-155">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-155">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="46636-156">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="46636-156">public boolean hasChanged(\[boolean val\])</span></span>                                                                                     | <span data-ttu-id="46636-157">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-157">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="46636-158">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="46636-158">public boolean hasUserSetting()</span></span>                                                                                                | <span data-ttu-id="46636-159">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-159">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="46636-160">public int hDC()</span><span class="sxs-lookup"><span data-stu-id="46636-160">public int hDC()</span></span>                                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="46636-161">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-161">public int height(int value, \[int mode\])</span></span>                                                                                     | <span data-ttu-id="46636-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-162">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="46636-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-163">public int heightMode(\[int value\])</span></span>                                                                                           | <span data-ttu-id="46636-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="46636-165">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-165">public int heightValue(\[int value\])</span></span>                                                                                          | <span data-ttu-id="46636-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-166">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="46636-167">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="46636-167">public str helpField()</span></span>                                                                                                         | <span data-ttu-id="46636-168">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-168">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="46636-169">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-169">public str helpText(\[str value\])</span></span>                                                                                             | <span data-ttu-id="46636-170">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-170">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="46636-171">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-171">public str hierarchyParent(\[str value\])</span></span>                                                                                      | <span data-ttu-id="46636-172">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-172">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="46636-173">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="46636-173">public int hWnd()</span></span>                                                                                                              | <span data-ttu-id="46636-174">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-174">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="46636-175">public Image image(\[Image value\])</span><span class="sxs-lookup"><span data-stu-id="46636-175">public Image image(\[Image value\])</span></span>                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="46636-176">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-176">public int imageLocation(\[int value\])</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="46636-177">public Imagelist imageList(\[Imagelist value\])</span><span class="sxs-lookup"><span data-stu-id="46636-177">public Imagelist imageList(\[Imagelist value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="46636-178">public int imagemode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-178">public int imagemode(\[int value\])</span></span>                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="46636-179">public str imageName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-179">public str imageName(\[str value\])</span></span>                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="46636-180">public int imageResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-180">public int imageResource(\[int value\])</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="46636-181">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="46636-181">public boolean isContainer()</span></span>                                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="46636-182">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="46636-182">public boolean isDisplayed()</span></span>                                                                                                   | <span data-ttu-id="46636-183">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-183">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="46636-184">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="46636-184">public boolean isRestricted()</span></span>                                                                                                  | <span data-ttu-id="46636-185">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-185">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="46636-186">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="46636-186">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                                       | <span data-ttu-id="46636-187">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-187">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="46636-188">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-188">public str label(\[str value\])</span></span>                                                                                                | <span data-ttu-id="46636-189">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-189">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="46636-190">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-190">public int labelAlignment(\[int value\])</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="46636-191">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-191">public int labelBold(\[int value\])</span></span>                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="46636-192">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-192">public int labelCharacterSet(\[int value\])</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-193">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-193">public str labelFont(\[str value\])</span></span>                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="46636-194">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-194">public int labelFontSize(\[int value\])</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="46636-195">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-195">public int labelForegroundColor(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="46636-196">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-196">public int labelGuide(\[int value\])</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="46636-197">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-197">public int labelHeight(int value, \[int mode\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="46636-198">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-198">public int labelHeightMode(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="46636-199">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-199">public int labelHeightValue(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="46636-200">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-200">public boolean labelItalic(\[boolean value\])</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="46636-201">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-201">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           |                                                                                                                                                                         |
| <span data-ttu-id="46636-202">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-202">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                               |                                                                                                                                                                         |
| <span data-ttu-id="46636-203">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-203">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="46636-204">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-204">public int labelPosition(\[int value\])</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="46636-205">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-205">public boolean labelUnderline(\[boolean value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="46636-206">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-206">public int labelWidth(int value, \[int mode\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="46636-207">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-207">public int labelWidthMode(\[int value\])</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="46636-208">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-208">public int labelWidthValue(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="46636-209">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="46636-209">public boolean leave()</span></span>                                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="46636-210">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-210">public int left(int value, \[int mode\])</span></span>                                                                                       | <span data-ttu-id="46636-211">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-211">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="46636-212">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-212">public int leftMode(\[int value\])</span></span>                                                                                             | <span data-ttu-id="46636-213">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-213">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="46636-214">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-214">public int leftValue(\[int value\])</span></span>                                                                                            | <span data-ttu-id="46636-215">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-215">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="46636-216">public str location(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-216">public str location(\[str value\])</span></span>                                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="46636-217">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-217">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                                | <span data-ttu-id="46636-218">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="46636-218">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="46636-219">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="46636-219">public boolean modified()</span></span>                                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="46636-220">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-220">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                | <span data-ttu-id="46636-221">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-221">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="46636-222">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-222">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                    | <span data-ttu-id="46636-223">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-223">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="46636-224">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-224">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                    | <span data-ttu-id="46636-225">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-225">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="46636-226">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-226">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                      | <span data-ttu-id="46636-227">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-227">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="46636-228">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-228">public str name(\[str value\])</span></span>                                                                                                 | <span data-ttu-id="46636-229">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-229">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                               |
| <span data-ttu-id="46636-230">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-230">public int neededPermission(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="46636-231">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-231">public str normalImage(\[str value\])</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="46636-232">public int onHScroll(int pos)</span><span class="sxs-lookup"><span data-stu-id="46636-232">public int onHScroll(int pos)</span></span>                                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="46636-233">public int onVScroll(int pos)</span><span class="sxs-lookup"><span data-stu-id="46636-233">public int onVScroll(int pos)</span></span>                                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="46636-234">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="46636-234">public container SysObsoleteAttribute()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="46636-235">public int paint()</span><span class="sxs-lookup"><span data-stu-id="46636-235">public int paint()</span></span>                                                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="46636-236">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="46636-236">public FormControl parentControl()</span></span>                                                                                             | <span data-ttu-id="46636-237">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-237">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="46636-238">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-238">public str previewPartRef(\[str value\])</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="46636-239">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-239">public int promptrect(\[int value\])</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="46636-240">public int scrollInfo(int VertScroller, \[int Pos\], \[int PageDelta\], \[int MoveDelta\], \[int MinLimit\], \[int MaxLimit\])</span><span class="sxs-lookup"><span data-stu-id="46636-240">public int scrollInfo(int VertScroller, \[int Pos\], \[int PageDelta\], \[int MoveDelta\], \[int MinLimit\], \[int MaxLimit\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="46636-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="46636-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                                      | <span data-ttu-id="46636-242">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-242">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="46636-243">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="46636-243">public int showContextMenu(int menuHandle)</span></span>                                                                                     | <span data-ttu-id="46636-244">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="46636-244">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="46636-245">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-245">public boolean showLabel(\[boolean value\])</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-246">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-246">public boolean skip(\[boolean value\])</span></span>                                                                                         | <span data-ttu-id="46636-247">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-247">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="46636-248">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="46636-248">public int sort(\[SortOrder sortDirection\])</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="46636-249">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="46636-249">public str toolTip()</span></span>                                                                                                           | <span data-ttu-id="46636-250">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-250">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="46636-251">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-251">public int top(int value, \[int mode\])</span></span>                                                                                        | <span data-ttu-id="46636-252">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-252">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="46636-253">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-253">public int topMode(\[int value\])</span></span>                                                                                              | <span data-ttu-id="46636-254">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-254">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="46636-255">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-255">public int topValue(\[int value\])</span></span>                                                                                             | <span data-ttu-id="46636-256">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-256">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="46636-257">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-257">public int type(\[int value\])</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="46636-258">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="46636-258">public boolean SysObsoleteAttribute(container data)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="46636-259">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-259">public int userData(\[int value\])</span></span>                                                                                             | <span data-ttu-id="46636-260">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-260">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="46636-261">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-261">public int userDataItem(\[int value\])</span></span>                                                                                         | <span data-ttu-id="46636-262">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-262">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="46636-263">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-263">public int userDataItems(\[int value\])</span></span>                                                                                        | <span data-ttu-id="46636-264">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-264">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="46636-265">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-265">public int userDisable(\[int value\])</span></span>                                                                                          | <span data-ttu-id="46636-266">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-266">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="46636-267">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-267">public int userHeight(\[int value\])</span></span>                                                                                           | <span data-ttu-id="46636-268">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-268">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="46636-269">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-269">public int userHide(\[int value\])</span></span>                                                                                             | <span data-ttu-id="46636-270">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-270">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="46636-271">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-271">public int userOrgContainer(\[int value\])</span></span>                                                                                     | <span data-ttu-id="46636-272">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-272">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="46636-273">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-273">public int userOrgSibling(\[int value\])</span></span>                                                                                       | <span data-ttu-id="46636-274">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-274">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="46636-275">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="46636-275">public str userPromptText(\[str value\])</span></span>                                                                                       | <span data-ttu-id="46636-276">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-276">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="46636-277">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-277">public int userSecurityLevel(\[int value\])</span></span>                                                                                    | <span data-ttu-id="46636-278">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-278">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="46636-279">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-279">public int userSkip(\[int value\])</span></span>                                                                                             | <span data-ttu-id="46636-280">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-280">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="46636-281">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-281">public int userWidth(\[int value\])</span></span>                                                                                            | <span data-ttu-id="46636-282">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-282">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="46636-283">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="46636-283">public boolean validate()</span></span>                                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="46636-284">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-284">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                                   | <span data-ttu-id="46636-285">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-285">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="46636-286">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-286">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                                         | <span data-ttu-id="46636-287">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-287">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="46636-288">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-288">public int verticalSpacingValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="46636-289">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-289">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="46636-290">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="46636-290">public boolean visible(\[boolean value\])</span></span>                                                                                      | <span data-ttu-id="46636-291">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-291">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="46636-292">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="46636-292">public int width(int value, \[int mode\])</span></span>                                                                                      | <span data-ttu-id="46636-293">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-293">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="46636-294">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-294">public int widthMode(\[int value\])</span></span>                                                                                            | <span data-ttu-id="46636-295">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-295">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="46636-296">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="46636-296">public int widthValue(\[int value\])</span></span>                                                                                           | <span data-ttu-id="46636-297">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-297">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="46636-298">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="46636-298">public void lostFocus()</span></span>                                                                                                        | <span data-ttu-id="46636-299">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-299">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="46636-300">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="46636-300">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-301">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="46636-301">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                                  | <span data-ttu-id="46636-302">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-302">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="46636-303">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="46636-303">public void dragLeave()</span></span>                                                                                                        | <span data-ttu-id="46636-304">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-304">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="46636-305">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="46636-305">public void gotFocus()</span></span>                                                                                                         | <span data-ttu-id="46636-306">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-306">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="46636-307">public void context()</span><span class="sxs-lookup"><span data-stu-id="46636-307">public void context()</span></span>                                                                                                          | <span data-ttu-id="46636-308">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="46636-308">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="46636-309">public void lockDC()</span><span class="sxs-lookup"><span data-stu-id="46636-309">public void lockDC()</span></span>                                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="46636-310">public void enter()</span><span class="sxs-lookup"><span data-stu-id="46636-310">public void enter()</span></span>                                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="46636-311">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="46636-311">public void endDrag()</span></span>                                                                                                          | <span data-ttu-id="46636-312">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-312">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="46636-313">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-313">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="46636-314">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-314">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                       |                                                                                                                                                                         |
| <span data-ttu-id="46636-315">public void setDirty(\[int x\], \[int y\], \[int width\], \[int height\])</span><span class="sxs-lookup"><span data-stu-id="46636-315">public void setDirty(\[int x\], \[int y\], \[int width\], \[int height\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="46636-316">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="46636-316">public void resetUserSetting()</span></span>                                                                                                 | <span data-ttu-id="46636-317">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="46636-317">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="46636-318">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-318">private void OnClicked(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="46636-319">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-319">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="46636-320">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="46636-320">public void filter(\[str filterStr\])</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="46636-321">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-321">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-322">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-322">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="46636-323">public void size(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="46636-323">public void size(int width, int height)</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="46636-324">public void dropFile(str FileName)</span><span class="sxs-lookup"><span data-stu-id="46636-324">public void dropFile(str FileName)</span></span>                                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="46636-325">public void cut()</span><span class="sxs-lookup"><span data-stu-id="46636-325">public void cut()</span></span>                                                                                                              | <span data-ttu-id="46636-326">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="46636-326">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="46636-327">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="46636-327">public void lookup()</span></span>                                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="46636-328">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="46636-328">public void setFocus()</span></span>                                                                                                         | <span data-ttu-id="46636-329">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-329">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="46636-330">public void undo()</span><span class="sxs-lookup"><span data-stu-id="46636-330">public void undo()</span></span>                                                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="46636-331">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-331">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="46636-332">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="46636-332">public void jumpRef()</span></span>                                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="46636-333">public void setScrollInfo()</span><span class="sxs-lookup"><span data-stu-id="46636-333">public void setScrollInfo()</span></span>                                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-334">public void paste()</span><span class="sxs-lookup"><span data-stu-id="46636-334">public void paste()</span></span>                                                                                                            | <span data-ttu-id="46636-335">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="46636-335">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="46636-336">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-336">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="46636-337">public void clicked()</span><span class="sxs-lookup"><span data-stu-id="46636-337">public void clicked()</span></span>                                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="46636-338">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="46636-338">public void inputSearch(str searchStr)</span></span>                                                                                         | <span data-ttu-id="46636-339">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="46636-339">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="46636-340">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="46636-340">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="46636-341">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="46636-341">public void mouseLeave()</span></span>                                                                                                       | <span data-ttu-id="46636-342">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-342">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="46636-343">public void copy()</span><span class="sxs-lookup"><span data-stu-id="46636-343">public void copy()</span></span>                                                                                                             | <span data-ttu-id="46636-344">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="46636-344">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="46636-345">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="46636-345">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                                      | <span data-ttu-id="46636-346">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-346">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="46636-347">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="46636-347">public void displayControl()</span></span>                                                                                                   | <span data-ttu-id="46636-348">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="46636-348">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="46636-349">public void unlockDC()</span><span class="sxs-lookup"><span data-stu-id="46636-349">public void unlockDC()</span></span>                                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="46636-350">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="46636-350">public void prefColumnSize(int width, int height)</span></span>                                                                              | <span data-ttu-id="46636-351">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="46636-351">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="46636-352">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="46636-352">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                                          | <span data-ttu-id="46636-353">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-353">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |

## <a name="method-aligncontrol"></a><span data-ttu-id="46636-354">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="46636-354">Method alignControl</span></span>

<span data-ttu-id="46636-355">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-355">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="46636-356">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="46636-356">Parameters - alignControl</span></span>

<span data-ttu-id="46636-357">値</span><span class="sxs-lookup"><span data-stu-id="46636-357">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="46636-358">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="46636-358">Return Value - alignControl</span></span>

<span data-ttu-id="46636-359">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="46636-359">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="46636-360">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="46636-360">Remarks - alignControl</span></span>

<span data-ttu-id="46636-361">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="46636-361">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="46636-362">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="46636-362">Method allowEdit</span></span>

<span data-ttu-id="46636-363">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-363">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="46636-364">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="46636-364">Parameters - allowEdit</span></span>

<span data-ttu-id="46636-365">値</span><span class="sxs-lookup"><span data-stu-id="46636-365">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="46636-366">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="46636-366">Return Value - allowEdit</span></span>

<span data-ttu-id="46636-367">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-367">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="46636-368">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="46636-368">Remarks - allowEdit</span></span>

<span data-ttu-id="46636-369">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="46636-369">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="46636-370">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="46636-370">Method allowSysSetup</span></span>

<span data-ttu-id="46636-371">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-371">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="46636-372">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="46636-372">Return Value - allowSysSetup</span></span>

<span data-ttu-id="46636-373">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-373">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="46636-374">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="46636-374">Method autoDeclaration</span></span>

<span data-ttu-id="46636-375">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-375">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="46636-376">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="46636-376">Parameters - autoDeclaration</span></span>

<span data-ttu-id="46636-377">値</span><span class="sxs-lookup"><span data-stu-id="46636-377">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="46636-378">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="46636-378">Return Value - autoDeclaration</span></span>

<span data-ttu-id="46636-379">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-379">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="46636-380">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="46636-380">Remarks - autoDeclaration</span></span>

<span data-ttu-id="46636-381">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="46636-381">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="46636-382">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-382">Method backgroundColor</span></span>

<span data-ttu-id="46636-383">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-383">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="46636-384">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-384">Parameters - backgroundColor</span></span>

<span data-ttu-id="46636-385">値</span><span class="sxs-lookup"><span data-stu-id="46636-385">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="46636-386">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-386">Return Value - backgroundColor</span></span>

<span data-ttu-id="46636-387">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="46636-387">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="46636-388">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-388">Remarks - backgroundColor</span></span>

<span data-ttu-id="46636-389">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="46636-389">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="46636-390">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="46636-390">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="46636-391">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="46636-391">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="46636-392">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="46636-392">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="46636-393">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="46636-393">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="46636-394">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="46636-394">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="46636-395">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="46636-395">Method backStyle</span></span>

<span data-ttu-id="46636-396">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-396">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="46636-397">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="46636-397">Parameters - backStyle</span></span>

<span data-ttu-id="46636-398">値</span><span class="sxs-lookup"><span data-stu-id="46636-398">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="46636-399">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="46636-399">Return Value - backStyle</span></span>

<span data-ttu-id="46636-400">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="46636-400">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="46636-401">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="46636-401">Method beginDrag</span></span>

<span data-ttu-id="46636-402">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-402">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="46636-403">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="46636-403">Parameters - beginDrag</span></span>

<span data-ttu-id="46636-404">x</span><span class="sxs-lookup"><span data-stu-id="46636-404">x</span></span>  
<span data-ttu-id="46636-405">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-405">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="46636-406">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="46636-406">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="46636-407">y</span><span class="sxs-lookup"><span data-stu-id="46636-407">y</span></span>  
<span data-ttu-id="46636-408">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-408">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="46636-409">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="46636-409">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="46636-410">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="46636-410">Return Value - beginDrag</span></span>

<span data-ttu-id="46636-411">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="46636-411">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="46636-412">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="46636-412">Remarks - beginDrag</span></span>

<span data-ttu-id="46636-413">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="46636-413">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="46636-414">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="46636-414">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="46636-415">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="46636-415">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="46636-416">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="46636-416">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="46636-417">値</span><span class="sxs-lookup"><span data-stu-id="46636-417">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="46636-418">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="46636-418">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="46636-419">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="46636-419">Method calcControlSize</span></span>

<span data-ttu-id="46636-420">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-420">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="46636-421">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="46636-421">Parameters - calcControlSize</span></span>

<span data-ttu-id="46636-422">chars</span><span class="sxs-lookup"><span data-stu-id="46636-422">chars</span></span>  
<span data-ttu-id="46636-423">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="46636-423">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="46636-424">明細行</span><span class="sxs-lookup"><span data-stu-id="46636-424">lines</span></span>  
<span data-ttu-id="46636-425">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="46636-425">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="46636-426">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="46636-426">Return Value - calcControlSize</span></span>

<span data-ttu-id="46636-427">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="46636-427">The container that holds the width and height.</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="46636-428">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="46636-428">Method colorScheme</span></span>

<span data-ttu-id="46636-429">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-429">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="46636-430">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="46636-430">Parameters - colorScheme</span></span>

<span data-ttu-id="46636-431">値</span><span class="sxs-lookup"><span data-stu-id="46636-431">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="46636-432">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="46636-432">Return Value - colorScheme</span></span>

<span data-ttu-id="46636-433">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="46636-433">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="46636-434">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="46636-434">Remarks - colorScheme</span></span>

<span data-ttu-id="46636-435">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="46636-435">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="46636-436">金額</span><span class="sxs-lookup"><span data-stu-id="46636-436">Value</span></span> | <span data-ttu-id="46636-437">スタイル</span><span class="sxs-lookup"><span data-stu-id="46636-437">Style</span></span>                        |
|-------|------------------------------|
| <span data-ttu-id="46636-438">0</span><span class="sxs-lookup"><span data-stu-id="46636-438">0</span></span>     | <span data-ttu-id="46636-439">既定</span><span class="sxs-lookup"><span data-stu-id="46636-439">Default</span></span>                      |
| <span data-ttu-id="46636-440">1</span><span class="sxs-lookup"><span data-stu-id="46636-440">1</span></span>     | <span data-ttu-id="46636-441">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="46636-441">The Microsoft Windows palette</span></span> |
| <span data-ttu-id="46636-442">2</span><span class="sxs-lookup"><span data-stu-id="46636-442">2</span></span>     | <span data-ttu-id="46636-443">真の配色</span><span class="sxs-lookup"><span data-stu-id="46636-443">The true-color scheme</span></span>        |

## <a name="method-command"></a><span data-ttu-id="46636-444">メソッド command</span><span class="sxs-lookup"><span data-stu-id="46636-444">Method command</span></span>

```xpp
public int command(int wParam, int lParam)
```

### <a name="parameters---command"></a><span data-ttu-id="46636-445">パラメーター - command</span><span class="sxs-lookup"><span data-stu-id="46636-445">Parameters - command</span></span>

<span data-ttu-id="46636-446">wParam</span><span class="sxs-lookup"><span data-stu-id="46636-446">wParam</span></span>  

<!-- -->

<span data-ttu-id="46636-447">lParam</span><span class="sxs-lookup"><span data-stu-id="46636-447">lParam</span></span>  

### <a name="return-value---command"></a><span data-ttu-id="46636-448">戻り値 - command</span><span class="sxs-lookup"><span data-stu-id="46636-448">Return Value - command</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="46636-449">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="46636-449">Method configurationKey</span></span>

<span data-ttu-id="46636-450">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-450">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="46636-451">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="46636-451">Parameters - configurationKey</span></span>

<span data-ttu-id="46636-452">値</span><span class="sxs-lookup"><span data-stu-id="46636-452">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="46636-453">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="46636-453">Return Value - configurationKey</span></span>

<span data-ttu-id="46636-454">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="46636-454">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="46636-455">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="46636-455">Remarks - configurationKey</span></span>

<span data-ttu-id="46636-456">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="46636-456">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="46636-457">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="46636-457">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="46636-458">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="46636-458">Method configurationKeyEx</span></span>

<span data-ttu-id="46636-459">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-459">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="46636-460">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="46636-460">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="46636-461">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="46636-461">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="46636-462">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="46636-462">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="46636-463">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="46636-463">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="46636-464">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="46636-464">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="46636-465">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="46636-465">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="46636-466">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="46636-466">Method countryRegionCodes</span></span>

<span data-ttu-id="46636-467">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-467">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="46636-468">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="46636-468">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="46636-469">値</span><span class="sxs-lookup"><span data-stu-id="46636-469">value</span></span>  
<span data-ttu-id="46636-470">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-470">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="46636-471">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="46636-471">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="46636-472">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="46636-472">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="46636-473">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="46636-473">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="46636-474">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="46636-474">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="46636-475">値</span><span class="sxs-lookup"><span data-stu-id="46636-475">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="46636-476">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="46636-476">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="46636-477">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="46636-477">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="46636-478">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="46636-478">Parameters - dataField</span></span>

<span data-ttu-id="46636-479">値</span><span class="sxs-lookup"><span data-stu-id="46636-479">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="46636-480">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="46636-480">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="46636-481">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="46636-481">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="46636-482">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="46636-482">Parameters - dataMethod</span></span>

<span data-ttu-id="46636-483">値</span><span class="sxs-lookup"><span data-stu-id="46636-483">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="46636-484">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="46636-484">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="46636-485">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="46636-485">Method dataRelationPath</span></span>

<span data-ttu-id="46636-486">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-486">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="46636-487">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="46636-487">Parameters - dataRelationPath</span></span>

<span data-ttu-id="46636-488">値</span><span class="sxs-lookup"><span data-stu-id="46636-488">value</span></span>  
<span data-ttu-id="46636-489">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-489">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="46636-490">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="46636-490">Return Value - dataRelationPath</span></span>

<span data-ttu-id="46636-491">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="46636-491">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="46636-492">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="46636-492">Remarks - dataRelationPath</span></span>

<span data-ttu-id="46636-493">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="46636-493">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="46636-494">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="46636-494">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="46636-495">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="46636-495">Method dataSource</span></span>

<span data-ttu-id="46636-496">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-496">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="46636-497">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="46636-497">Parameters - dataSource</span></span>

<span data-ttu-id="46636-498">値</span><span class="sxs-lookup"><span data-stu-id="46636-498">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="46636-499">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="46636-499">Return Value - dataSource</span></span>

<span data-ttu-id="46636-500">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="46636-500">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="46636-501">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="46636-501">Method displayTarget</span></span>

<span data-ttu-id="46636-502">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-502">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="46636-503">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="46636-503">Parameters - displayTarget</span></span>

<span data-ttu-id="46636-504">値</span><span class="sxs-lookup"><span data-stu-id="46636-504">value</span></span>  
<span data-ttu-id="46636-505">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-505">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="46636-506">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="46636-506">Return Value - displayTarget</span></span>

<span data-ttu-id="46636-507">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="46636-507">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="46636-508">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="46636-508">Method dragDrop</span></span>

<span data-ttu-id="46636-509">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-509">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="46636-510">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="46636-510">Parameters - dragDrop</span></span>

<span data-ttu-id="46636-511">値</span><span class="sxs-lookup"><span data-stu-id="46636-511">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="46636-512">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="46636-512">Return Value - dragDrop</span></span>

<span data-ttu-id="46636-513">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="46636-513">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="46636-514">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="46636-514">Method dragOver</span></span>

<span data-ttu-id="46636-515">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-515">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="46636-516">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="46636-516">Parameters - dragOver</span></span>

<span data-ttu-id="46636-517">dragSource</span><span class="sxs-lookup"><span data-stu-id="46636-517">dragSource</span></span>  
<span data-ttu-id="46636-518">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-518">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-519">dragMode</span><span class="sxs-lookup"><span data-stu-id="46636-519">dragMode</span></span>  
<span data-ttu-id="46636-520">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-520">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-521">x</span><span class="sxs-lookup"><span data-stu-id="46636-521">x</span></span>  
<span data-ttu-id="46636-522">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-522">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-523">y</span><span class="sxs-lookup"><span data-stu-id="46636-523">y</span></span>  
<span data-ttu-id="46636-524">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-524">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="46636-525">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="46636-525">Return Value - dragOver</span></span>

<span data-ttu-id="46636-526">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="46636-526">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="46636-527">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="46636-527">Method dragOverEx</span></span>

<span data-ttu-id="46636-528">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-528">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="46636-529">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="46636-529">Parameters - dragOverEx</span></span>

<span data-ttu-id="46636-530">dragSource</span><span class="sxs-lookup"><span data-stu-id="46636-530">dragSource</span></span>  
<span data-ttu-id="46636-531">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-531">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-532">dragMode</span><span class="sxs-lookup"><span data-stu-id="46636-532">dragMode</span></span>  
<span data-ttu-id="46636-533">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-533">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-534">x</span><span class="sxs-lookup"><span data-stu-id="46636-534">x</span></span>  
<span data-ttu-id="46636-535">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-535">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-536">y</span><span class="sxs-lookup"><span data-stu-id="46636-536">y</span></span>  
<span data-ttu-id="46636-537">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-537">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="46636-538">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="46636-538">Return Value - dragOverEx</span></span>

<span data-ttu-id="46636-539">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="46636-539">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="46636-540">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="46636-540">Method dragText</span></span>

<span data-ttu-id="46636-541">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-541">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="46636-542">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="46636-542">Return Value - dragText</span></span>

<span data-ttu-id="46636-543">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="46636-543">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="46636-544">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="46636-544">Method enabled</span></span>

<span data-ttu-id="46636-545">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="46636-545">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="46636-546">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="46636-546">Parameters - enabled</span></span>

<span data-ttu-id="46636-547">値</span><span class="sxs-lookup"><span data-stu-id="46636-547">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="46636-548">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="46636-548">Return Value - enabled</span></span>

<span data-ttu-id="46636-549">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-549">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="46636-550">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="46636-550">Remarks - enabled</span></span>

<span data-ttu-id="46636-551">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="46636-551">The enabled property gives for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="46636-552">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="46636-552">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="46636-553">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="46636-553">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="46636-554">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-554">Method foregroundColor</span></span>

<span data-ttu-id="46636-555">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-555">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="46636-556">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-556">Parameters - foregroundColor</span></span>

<span data-ttu-id="46636-557">値</span><span class="sxs-lookup"><span data-stu-id="46636-557">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="46636-558">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-558">Return Value - foregroundColor</span></span>

<span data-ttu-id="46636-559">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="46636-559">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="46636-560">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-560">Remarks - foregroundColor</span></span>

<span data-ttu-id="46636-561">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="46636-561">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="46636-562">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="46636-562">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="46636-563">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="46636-563">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="46636-564">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="46636-564">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="46636-565">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="46636-565">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="46636-566">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="46636-566">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="46636-567">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="46636-567">Method hasChanged</span></span>

<span data-ttu-id="46636-568">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-568">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="46636-569">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="46636-569">Parameters - hasChanged</span></span>

<span data-ttu-id="46636-570">val</span><span class="sxs-lookup"><span data-stu-id="46636-570">val</span></span>  
<span data-ttu-id="46636-571">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-571">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="46636-572">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="46636-572">Return Value - hasChanged</span></span>

<span data-ttu-id="46636-573">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-573">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="46636-574">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="46636-574">Method hasUserSetting</span></span>

<span data-ttu-id="46636-575">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-575">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="46636-576">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="46636-576">Return Value - hasUserSetting</span></span>

<span data-ttu-id="46636-577">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-577">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-hdc"></a><span data-ttu-id="46636-578">メソッド hDC</span><span class="sxs-lookup"><span data-stu-id="46636-578">Method hDC</span></span>

```xpp
public int hDC()
```

### <a name="return-value---hdc"></a><span data-ttu-id="46636-579">戻り値 - hDC</span><span class="sxs-lookup"><span data-stu-id="46636-579">Return Value - hDC</span></span>

## <a name="method-height"></a><span data-ttu-id="46636-580">メソッド height</span><span class="sxs-lookup"><span data-stu-id="46636-580">Method height</span></span>

<span data-ttu-id="46636-581">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-581">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="46636-582">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="46636-582">Parameters - height</span></span>

<span data-ttu-id="46636-583">値</span><span class="sxs-lookup"><span data-stu-id="46636-583">value</span></span>  

<!-- -->

<span data-ttu-id="46636-584">モード</span><span class="sxs-lookup"><span data-stu-id="46636-584">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="46636-585">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="46636-585">Return Value - height</span></span>

<span data-ttu-id="46636-586">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="46636-586">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="46636-587">備考 - height</span><span class="sxs-lookup"><span data-stu-id="46636-587">Remarks - height</span></span>

<span data-ttu-id="46636-588">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="46636-588">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="46636-589">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="46636-589">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="46636-590">モード</span><span class="sxs-lookup"><span data-stu-id="46636-590">Mode</span></span>            | <span data-ttu-id="46636-591">高さの計算</span><span class="sxs-lookup"><span data-stu-id="46636-591">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="46636-592">-1 正確</span><span class="sxs-lookup"><span data-stu-id="46636-592">-1 Exact</span></span>        | <span data-ttu-id="46636-593">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="46636-593">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="46636-594">0 自動</span><span class="sxs-lookup"><span data-stu-id="46636-594">0 Auto</span></span>          | <span data-ttu-id="46636-595">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="46636-595">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="46636-596">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="46636-596">1 Column height</span></span> | <span data-ttu-id="46636-597">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="46636-597">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="46636-598">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="46636-598">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="46636-599">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="46636-599">Method heightMode</span></span>

<span data-ttu-id="46636-600">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-600">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="46636-601">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="46636-601">Parameters - heightMode</span></span>

<span data-ttu-id="46636-602">値</span><span class="sxs-lookup"><span data-stu-id="46636-602">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="46636-603">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="46636-603">Return Value - heightMode</span></span>

<span data-ttu-id="46636-604">計算モード。</span><span class="sxs-lookup"><span data-stu-id="46636-604">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="46636-605">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="46636-605">Remarks - heightMode</span></span>

<span data-ttu-id="46636-606">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="46636-606">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="46636-607">モード</span><span class="sxs-lookup"><span data-stu-id="46636-607">Mode</span></span>          | <span data-ttu-id="46636-608">高さの計算</span><span class="sxs-lookup"><span data-stu-id="46636-608">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="46636-609">正確</span><span class="sxs-lookup"><span data-stu-id="46636-609">Exact</span></span>         | <span data-ttu-id="46636-610">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="46636-610">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="46636-611">自動</span><span class="sxs-lookup"><span data-stu-id="46636-611">Auto</span></span>          | <span data-ttu-id="46636-612">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="46636-612">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="46636-613">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="46636-613">Column height</span></span> | <span data-ttu-id="46636-614">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="46636-614">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="46636-615">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="46636-615">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="46636-616">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="46636-616">Method heightValue</span></span>

<span data-ttu-id="46636-617">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-617">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="46636-618">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="46636-618">Parameters - heightValue</span></span>

<span data-ttu-id="46636-619">値</span><span class="sxs-lookup"><span data-stu-id="46636-619">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="46636-620">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="46636-620">Return Value - heightValue</span></span>

<span data-ttu-id="46636-621">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="46636-621">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="46636-622">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="46636-622">Remarks - heightValue</span></span>

<span data-ttu-id="46636-623">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="46636-623">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="46636-624">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="46636-624">Method helpField</span></span>

<span data-ttu-id="46636-625">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-625">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="46636-626">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="46636-626">Return Value - helpField</span></span>

<span data-ttu-id="46636-627">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="46636-627">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="46636-628">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="46636-628">Remarks - helpField</span></span>

<span data-ttu-id="46636-629">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="46636-629">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="46636-630">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="46636-630">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="46636-631">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="46636-631">Method helpText</span></span>

<span data-ttu-id="46636-632">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-632">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="46636-633">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="46636-633">Parameters - helpText</span></span>

<span data-ttu-id="46636-634">値</span><span class="sxs-lookup"><span data-stu-id="46636-634">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="46636-635">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="46636-635">Return Value - helpText</span></span>

<span data-ttu-id="46636-636">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="46636-636">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="46636-637">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="46636-637">Remarks - helpText</span></span>

<span data-ttu-id="46636-638">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-638">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="46636-639">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="46636-639">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="46636-640">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="46636-640">Method hierarchyParent</span></span>

<span data-ttu-id="46636-641">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-641">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="46636-642">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="46636-642">Parameters - hierarchyParent</span></span>

<span data-ttu-id="46636-643">値</span><span class="sxs-lookup"><span data-stu-id="46636-643">value</span></span>  
<span data-ttu-id="46636-644">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="46636-644">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="46636-645">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="46636-645">Return Value - hierarchyParent</span></span>

<span data-ttu-id="46636-646">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="46636-646">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="46636-647">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="46636-647">Method hWnd</span></span>

<span data-ttu-id="46636-648">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-648">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="46636-649">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="46636-649">Return Value - hWnd</span></span>

<span data-ttu-id="46636-650">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="46636-650">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="46636-651">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="46636-651">Remarks - hWnd</span></span>

<span data-ttu-id="46636-652">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="46636-652">The handle can be used with the Windows API.</span></span>

## <a name="method-image"></a><span data-ttu-id="46636-653">メソッド image</span><span class="sxs-lookup"><span data-stu-id="46636-653">Method image</span></span>

```xpp
public Image image([Image value])
```

### <a name="parameters---image"></a><span data-ttu-id="46636-654">パラメーター - image</span><span class="sxs-lookup"><span data-stu-id="46636-654">Parameters - image</span></span>

<span data-ttu-id="46636-655">値</span><span class="sxs-lookup"><span data-stu-id="46636-655">value</span></span>  

### <a name="return-value---image"></a><span data-ttu-id="46636-656">戻り値 - image</span><span class="sxs-lookup"><span data-stu-id="46636-656">Return Value - image</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="46636-657">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="46636-657">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="46636-658">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="46636-658">Parameters - imageLocation</span></span>

<span data-ttu-id="46636-659">値</span><span class="sxs-lookup"><span data-stu-id="46636-659">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="46636-660">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="46636-660">Return Value - imageLocation</span></span>

## <a name="method-imagelist"></a><span data-ttu-id="46636-661">メソッド imageList</span><span class="sxs-lookup"><span data-stu-id="46636-661">Method imageList</span></span>

```xpp
public Imagelist imageList([Imagelist value])
```

### <a name="parameters---imagelist"></a><span data-ttu-id="46636-662">パラメーター - imageList</span><span class="sxs-lookup"><span data-stu-id="46636-662">Parameters - imageList</span></span>

<span data-ttu-id="46636-663">値</span><span class="sxs-lookup"><span data-stu-id="46636-663">value</span></span>  

### <a name="return-value---imagelist"></a><span data-ttu-id="46636-664">戻り値 - imageList</span><span class="sxs-lookup"><span data-stu-id="46636-664">Return Value - imageList</span></span>

## <a name="method-imagemode"></a><span data-ttu-id="46636-665">メソッド imagemode</span><span class="sxs-lookup"><span data-stu-id="46636-665">Method imagemode</span></span>

```xpp
public int imagemode([int value])
```

### <a name="parameters---imagemode"></a><span data-ttu-id="46636-666">パラメーター - imagemode</span><span class="sxs-lookup"><span data-stu-id="46636-666">Parameters - imagemode</span></span>

<span data-ttu-id="46636-667">値</span><span class="sxs-lookup"><span data-stu-id="46636-667">value</span></span>  

### <a name="return-value---imagemode"></a><span data-ttu-id="46636-668">戻り値 - imagemode</span><span class="sxs-lookup"><span data-stu-id="46636-668">Return Value - imagemode</span></span>

## <a name="method-imagename"></a><span data-ttu-id="46636-669">メソッド imageName</span><span class="sxs-lookup"><span data-stu-id="46636-669">Method imageName</span></span>

```xpp
public str imageName([str value])
```

### <a name="parameters---imagename"></a><span data-ttu-id="46636-670">パラメーター - imageName</span><span class="sxs-lookup"><span data-stu-id="46636-670">Parameters - imageName</span></span>

<span data-ttu-id="46636-671">値</span><span class="sxs-lookup"><span data-stu-id="46636-671">value</span></span>  

### <a name="return-value---imagename"></a><span data-ttu-id="46636-672">戻り値 - imageName</span><span class="sxs-lookup"><span data-stu-id="46636-672">Return Value - imageName</span></span>

## <a name="method-imageresource"></a><span data-ttu-id="46636-673">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="46636-673">Method imageResource</span></span>

```xpp
public int imageResource([int value])
```

### <a name="parameters---imageresource"></a><span data-ttu-id="46636-674">パラメーター - imageResource</span><span class="sxs-lookup"><span data-stu-id="46636-674">Parameters - imageResource</span></span>

<span data-ttu-id="46636-675">値</span><span class="sxs-lookup"><span data-stu-id="46636-675">value</span></span>  

### <a name="return-value---imageresource"></a><span data-ttu-id="46636-676">戻り値 - imageResource</span><span class="sxs-lookup"><span data-stu-id="46636-676">Return Value - imageResource</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="46636-677">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="46636-677">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="46636-678">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="46636-678">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="46636-679">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="46636-679">Method isDisplayed</span></span>

<span data-ttu-id="46636-680">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-680">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="46636-681">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="46636-681">Return Value - isDisplayed</span></span>

<span data-ttu-id="46636-682">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="46636-682">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="46636-683">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="46636-683">Remarks - isDisplayed</span></span>

<span data-ttu-id="46636-684">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="46636-684">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="46636-685">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="46636-685">Method isRestricted</span></span>

<span data-ttu-id="46636-686">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-686">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="46636-687">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="46636-687">Return Value - isRestricted</span></span>

<span data-ttu-id="46636-688">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="46636-688">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="46636-689">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="46636-689">Method isUserSetupEnabled</span></span>

<span data-ttu-id="46636-690">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-690">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="46636-691">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="46636-691">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="46636-692">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="46636-692">neededSetupRights</span></span>  
<span data-ttu-id="46636-693">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="46636-693">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="46636-694">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="46636-694">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="46636-695">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-695">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="46636-696">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="46636-696">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="46636-697">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="46636-697">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46636-698">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="46636-698">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="46636-699">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="46636-699">No changes can be made to the control.</span></span> <span data-ttu-id="46636-700">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="46636-700">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="46636-701">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="46636-701">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="46636-702">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="46636-702">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="46636-703">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="46636-703">The user cannot move the control.</span></span>   |
| <span data-ttu-id="46636-704">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="46636-704">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="46636-705">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="46636-705">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="46636-706">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="46636-706">The user can also move the control.</span></span> |

<span data-ttu-id="46636-707">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="46636-707">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-label"></a><span data-ttu-id="46636-708">メソッド label</span><span class="sxs-lookup"><span data-stu-id="46636-708">Method label</span></span>

<span data-ttu-id="46636-709">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-709">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="46636-710">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="46636-710">Parameters - label</span></span>

<span data-ttu-id="46636-711">値</span><span class="sxs-lookup"><span data-stu-id="46636-711">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="46636-712">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="46636-712">Return Value - label</span></span>

<span data-ttu-id="46636-713">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="46636-713">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="46636-714">備考 - label</span><span class="sxs-lookup"><span data-stu-id="46636-714">Remarks - label</span></span>

<span data-ttu-id="46636-715">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="46636-715">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="46636-716">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="46636-716">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="46636-717">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="46636-717">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="46636-718">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="46636-718">Parameters - labelAlignment</span></span>

<span data-ttu-id="46636-719">値</span><span class="sxs-lookup"><span data-stu-id="46636-719">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="46636-720">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="46636-720">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="46636-721">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="46636-721">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="46636-722">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="46636-722">Parameters - labelBold</span></span>

<span data-ttu-id="46636-723">値</span><span class="sxs-lookup"><span data-stu-id="46636-723">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="46636-724">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="46636-724">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="46636-725">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="46636-725">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="46636-726">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="46636-726">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="46636-727">値</span><span class="sxs-lookup"><span data-stu-id="46636-727">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="46636-728">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="46636-728">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="46636-729">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="46636-729">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="46636-730">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="46636-730">Parameters - labelFont</span></span>

<span data-ttu-id="46636-731">値</span><span class="sxs-lookup"><span data-stu-id="46636-731">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="46636-732">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="46636-732">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="46636-733">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="46636-733">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="46636-734">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="46636-734">Parameters - labelFontSize</span></span>

<span data-ttu-id="46636-735">値</span><span class="sxs-lookup"><span data-stu-id="46636-735">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="46636-736">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="46636-736">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="46636-737">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-737">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="46636-738">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-738">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="46636-739">値</span><span class="sxs-lookup"><span data-stu-id="46636-739">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="46636-740">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="46636-740">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="46636-741">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="46636-741">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="46636-742">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="46636-742">Parameters - labelGuide</span></span>

<span data-ttu-id="46636-743">値</span><span class="sxs-lookup"><span data-stu-id="46636-743">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="46636-744">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="46636-744">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="46636-745">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="46636-745">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="46636-746">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="46636-746">Parameters - labelHeight</span></span>

<span data-ttu-id="46636-747">値</span><span class="sxs-lookup"><span data-stu-id="46636-747">value</span></span>  

<!-- -->

<span data-ttu-id="46636-748">モード</span><span class="sxs-lookup"><span data-stu-id="46636-748">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="46636-749">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="46636-749">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="46636-750">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="46636-750">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="46636-751">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="46636-751">Parameters - labelHeightMode</span></span>

<span data-ttu-id="46636-752">値</span><span class="sxs-lookup"><span data-stu-id="46636-752">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="46636-753">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="46636-753">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="46636-754">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="46636-754">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="46636-755">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="46636-755">Parameters - labelHeightValue</span></span>

<span data-ttu-id="46636-756">値</span><span class="sxs-lookup"><span data-stu-id="46636-756">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="46636-757">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="46636-757">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="46636-758">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="46636-758">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="46636-759">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="46636-759">Parameters - labelItalic</span></span>

<span data-ttu-id="46636-760">値</span><span class="sxs-lookup"><span data-stu-id="46636-760">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="46636-761">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="46636-761">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="46636-762">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="46636-762">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="46636-763">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="46636-763">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="46636-764">x</span><span class="sxs-lookup"><span data-stu-id="46636-764">x</span></span>  

<!-- -->

<span data-ttu-id="46636-765">y</span><span class="sxs-lookup"><span data-stu-id="46636-765">y</span></span>  

<!-- -->

<span data-ttu-id="46636-766">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-766">button</span></span>  

<!-- -->

<span data-ttu-id="46636-767">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-767">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="46636-768">Shift</span><span class="sxs-lookup"><span data-stu-id="46636-768">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="46636-769">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="46636-769">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="46636-770">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="46636-770">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="46636-771">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="46636-771">Parameters - labelMouseDown</span></span>

<span data-ttu-id="46636-772">x</span><span class="sxs-lookup"><span data-stu-id="46636-772">x</span></span>  

<!-- -->

<span data-ttu-id="46636-773">y</span><span class="sxs-lookup"><span data-stu-id="46636-773">y</span></span>  

<!-- -->

<span data-ttu-id="46636-774">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-774">button</span></span>  

<!-- -->

<span data-ttu-id="46636-775">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-775">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="46636-776">Shift</span><span class="sxs-lookup"><span data-stu-id="46636-776">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="46636-777">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="46636-777">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="46636-778">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="46636-778">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="46636-779">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="46636-779">Parameters - labelMouseUp</span></span>

<span data-ttu-id="46636-780">x</span><span class="sxs-lookup"><span data-stu-id="46636-780">x</span></span>  

<!-- -->

<span data-ttu-id="46636-781">y</span><span class="sxs-lookup"><span data-stu-id="46636-781">y</span></span>  

<!-- -->

<span data-ttu-id="46636-782">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-782">button</span></span>  

<!-- -->

<span data-ttu-id="46636-783">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-783">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="46636-784">Shift</span><span class="sxs-lookup"><span data-stu-id="46636-784">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="46636-785">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="46636-785">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="46636-786">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="46636-786">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="46636-787">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="46636-787">Parameters - labelPosition</span></span>

<span data-ttu-id="46636-788">値</span><span class="sxs-lookup"><span data-stu-id="46636-788">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="46636-789">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="46636-789">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="46636-790">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="46636-790">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="46636-791">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="46636-791">Parameters - labelUnderline</span></span>

<span data-ttu-id="46636-792">値</span><span class="sxs-lookup"><span data-stu-id="46636-792">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="46636-793">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="46636-793">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="46636-794">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="46636-794">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="46636-795">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="46636-795">Parameters - labelWidth</span></span>

<span data-ttu-id="46636-796">値</span><span class="sxs-lookup"><span data-stu-id="46636-796">value</span></span>  

<!-- -->

<span data-ttu-id="46636-797">モード</span><span class="sxs-lookup"><span data-stu-id="46636-797">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="46636-798">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="46636-798">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="46636-799">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="46636-799">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="46636-800">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="46636-800">Parameters - labelWidthMode</span></span>

<span data-ttu-id="46636-801">値</span><span class="sxs-lookup"><span data-stu-id="46636-801">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="46636-802">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="46636-802">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="46636-803">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="46636-803">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="46636-804">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="46636-804">Parameters - labelWidthValue</span></span>

<span data-ttu-id="46636-805">値</span><span class="sxs-lookup"><span data-stu-id="46636-805">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="46636-806">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="46636-806">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="46636-807">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="46636-807">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="46636-808">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="46636-808">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="46636-809">メソッド left</span><span class="sxs-lookup"><span data-stu-id="46636-809">Method left</span></span>

<span data-ttu-id="46636-810">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-810">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="46636-811">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="46636-811">Parameters - left</span></span>

<span data-ttu-id="46636-812">値</span><span class="sxs-lookup"><span data-stu-id="46636-812">value</span></span>  
<span data-ttu-id="46636-813">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-813">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="46636-814">モード</span><span class="sxs-lookup"><span data-stu-id="46636-814">mode</span></span>  
<span data-ttu-id="46636-815">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-815">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="46636-816">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="46636-816">Return Value - left</span></span>

<span data-ttu-id="46636-817">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="46636-817">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="46636-818">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="46636-818">Method leftMode</span></span>

<span data-ttu-id="46636-819">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-819">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="46636-820">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="46636-820">Parameters - leftMode</span></span>

<span data-ttu-id="46636-821">値</span><span class="sxs-lookup"><span data-stu-id="46636-821">value</span></span>  
<span data-ttu-id="46636-822">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-822">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="46636-823">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="46636-823">Return Value - leftMode</span></span>

<span data-ttu-id="46636-824">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="46636-824">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="46636-825">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="46636-825">Method leftValue</span></span>

<span data-ttu-id="46636-826">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-826">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="46636-827">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="46636-827">Parameters - leftValue</span></span>

<span data-ttu-id="46636-828">値</span><span class="sxs-lookup"><span data-stu-id="46636-828">value</span></span>  
<span data-ttu-id="46636-829">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-829">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="46636-830">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="46636-830">Return Value - leftValue</span></span>

<span data-ttu-id="46636-831">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="46636-831">The horizontal position of the control in the form.</span></span>

## <a name="method-location"></a><span data-ttu-id="46636-832">メソッド location</span><span class="sxs-lookup"><span data-stu-id="46636-832">Method location</span></span>

```xpp
public str location([str value])
```

### <a name="parameters---location"></a><span data-ttu-id="46636-833">パラメーター - location</span><span class="sxs-lookup"><span data-stu-id="46636-833">Parameters - location</span></span>

<span data-ttu-id="46636-834">値</span><span class="sxs-lookup"><span data-stu-id="46636-834">value</span></span>  

### <a name="return-value---location"></a><span data-ttu-id="46636-835">戻り値 - location</span><span class="sxs-lookup"><span data-stu-id="46636-835">Return Value - location</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="46636-836">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="46636-836">Method markAsUserAdd</span></span>

<span data-ttu-id="46636-837">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="46636-837">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="46636-838">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="46636-838">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="46636-839">値</span><span class="sxs-lookup"><span data-stu-id="46636-839">value</span></span>  
<span data-ttu-id="46636-840">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-840">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="46636-841">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="46636-841">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="46636-842">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-842">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="46636-843">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="46636-843">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="46636-844">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="46636-844">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="46636-845">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="46636-845">Method mouseDblClick</span></span>

<span data-ttu-id="46636-846">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-846">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="46636-847">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="46636-847">Parameters - mouseDblClick</span></span>

<span data-ttu-id="46636-848">x</span><span class="sxs-lookup"><span data-stu-id="46636-848">x</span></span>  
<span data-ttu-id="46636-849">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-849">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-850">y</span><span class="sxs-lookup"><span data-stu-id="46636-850">y</span></span>  
<span data-ttu-id="46636-851">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-851">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-852">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-852">button</span></span>  
<span data-ttu-id="46636-853">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-853">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-854">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-854">Ctrl</span></span>  
<span data-ttu-id="46636-855">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-855">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-856">シフト</span><span class="sxs-lookup"><span data-stu-id="46636-856">Shift</span></span>  
<span data-ttu-id="46636-857">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-857">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="46636-858">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="46636-858">Return Value - mouseDblClick</span></span>

<span data-ttu-id="46636-859">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="46636-859">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="46636-860">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="46636-860">Remarks - mouseDblClick</span></span>

<span data-ttu-id="46636-861">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="46636-861">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="46636-862">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="46636-862">Method mouseDown</span></span>

<span data-ttu-id="46636-863">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-863">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="46636-864">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="46636-864">Parameters - mouseDown</span></span>

<span data-ttu-id="46636-865">x</span><span class="sxs-lookup"><span data-stu-id="46636-865">x</span></span>  
<span data-ttu-id="46636-866">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-866">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-867">y</span><span class="sxs-lookup"><span data-stu-id="46636-867">y</span></span>  
<span data-ttu-id="46636-868">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-868">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-869">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-869">button</span></span>  
<span data-ttu-id="46636-870">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-870">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-871">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-871">Ctrl</span></span>  
<span data-ttu-id="46636-872">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-872">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-873">シフト</span><span class="sxs-lookup"><span data-stu-id="46636-873">Shift</span></span>  
<span data-ttu-id="46636-874">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-874">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="46636-875">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="46636-875">Return Value - mouseDown</span></span>

<span data-ttu-id="46636-876">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="46636-876">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="46636-877">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="46636-877">Remarks - mouseDown</span></span>

<span data-ttu-id="46636-878">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="46636-878">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="46636-879">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-879">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="46636-880">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="46636-880">Method mouseMove</span></span>

<span data-ttu-id="46636-881">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-881">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="46636-882">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="46636-882">Parameters - mouseMove</span></span>

<span data-ttu-id="46636-883">x</span><span class="sxs-lookup"><span data-stu-id="46636-883">x</span></span>  
<span data-ttu-id="46636-884">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-884">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-885">y</span><span class="sxs-lookup"><span data-stu-id="46636-885">y</span></span>  
<span data-ttu-id="46636-886">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-886">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-887">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-887">button</span></span>  
<span data-ttu-id="46636-888">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-888">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-889">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-889">Ctrl</span></span>  
<span data-ttu-id="46636-890">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-890">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-891">シフト</span><span class="sxs-lookup"><span data-stu-id="46636-891">Shift</span></span>  
<span data-ttu-id="46636-892">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-892">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="46636-893">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="46636-893">Return Value - mouseMove</span></span>

<span data-ttu-id="46636-894">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="46636-894">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="46636-895">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="46636-895">Remarks - mouseMove</span></span>

<span data-ttu-id="46636-896">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="46636-896">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="46636-897">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="46636-897">Method mouseUp</span></span>

<span data-ttu-id="46636-898">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-898">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="46636-899">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="46636-899">Parameters - mouseUp</span></span>

<span data-ttu-id="46636-900">x</span><span class="sxs-lookup"><span data-stu-id="46636-900">x</span></span>  
<span data-ttu-id="46636-901">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-901">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-902">y</span><span class="sxs-lookup"><span data-stu-id="46636-902">y</span></span>  
<span data-ttu-id="46636-903">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-903">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-904">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-904">button</span></span>  
<span data-ttu-id="46636-905">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-905">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-906">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-906">Ctrl</span></span>  
<span data-ttu-id="46636-907">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-907">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-908">シフト</span><span class="sxs-lookup"><span data-stu-id="46636-908">Shift</span></span>  
<span data-ttu-id="46636-909">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-909">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="46636-910">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="46636-910">Return Value - mouseUp</span></span>

<span data-ttu-id="46636-911">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="46636-911">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="46636-912">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="46636-912">Remarks - mouseUp</span></span>

<span data-ttu-id="46636-913">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="46636-913">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="46636-914">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-914">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="46636-915">メソッド名</span><span class="sxs-lookup"><span data-stu-id="46636-915">Method name</span></span>

<span data-ttu-id="46636-916">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-916">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="46636-917">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="46636-917">Parameters - name</span></span>

<span data-ttu-id="46636-918">値</span><span class="sxs-lookup"><span data-stu-id="46636-918">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="46636-919">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="46636-919">Return Value - name</span></span>

<span data-ttu-id="46636-920">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="46636-920">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="46636-921">備考 - name</span><span class="sxs-lookup"><span data-stu-id="46636-921">Remarks - name</span></span>

<span data-ttu-id="46636-922">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="46636-922">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="46636-923">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="46636-923">Begins with a letter.</span></span>
-   <span data-ttu-id="46636-924">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="46636-924">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="46636-925">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="46636-925">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="46636-926">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="46636-926">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="46636-927">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="46636-927">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="46636-928">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="46636-928">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="46636-929">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="46636-929">Parameters - neededPermission</span></span>

<span data-ttu-id="46636-930">値</span><span class="sxs-lookup"><span data-stu-id="46636-930">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="46636-931">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="46636-931">Return Value - neededPermission</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="46636-932">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="46636-932">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="46636-933">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="46636-933">Parameters - normalImage</span></span>

<span data-ttu-id="46636-934">値</span><span class="sxs-lookup"><span data-stu-id="46636-934">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="46636-935">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="46636-935">Return Value - normalImage</span></span>

## <a name="method-onhscroll"></a><span data-ttu-id="46636-936">メソッド onHScroll</span><span class="sxs-lookup"><span data-stu-id="46636-936">Method onHScroll</span></span>

```xpp
public int onHScroll(int pos)
```

### <a name="parameters---onhscroll"></a><span data-ttu-id="46636-937">パラメーター - onHScroll</span><span class="sxs-lookup"><span data-stu-id="46636-937">Parameters - onHScroll</span></span>

<span data-ttu-id="46636-938">pos</span><span class="sxs-lookup"><span data-stu-id="46636-938">pos</span></span>  

### <a name="return-value---onhscroll"></a><span data-ttu-id="46636-939">戻り値 - onHScroll</span><span class="sxs-lookup"><span data-stu-id="46636-939">Return Value - onHScroll</span></span>

## <a name="method-onvscroll"></a><span data-ttu-id="46636-940">メソッド onVScroll</span><span class="sxs-lookup"><span data-stu-id="46636-940">Method onVScroll</span></span>

```xpp
public int onVScroll(int pos)
```

### <a name="parameters---onvscroll"></a><span data-ttu-id="46636-941">パラメーター - onVScroll</span><span class="sxs-lookup"><span data-stu-id="46636-941">Parameters - onVScroll</span></span>

<span data-ttu-id="46636-942">pos</span><span class="sxs-lookup"><span data-stu-id="46636-942">pos</span></span>  

### <a name="return-value---onvscroll"></a><span data-ttu-id="46636-943">戻り値 - onVScroll</span><span class="sxs-lookup"><span data-stu-id="46636-943">Return Value - onVScroll</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="46636-944">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="46636-944">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="46636-945">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="46636-945">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-paint"></a><span data-ttu-id="46636-946">メソッド paint</span><span class="sxs-lookup"><span data-stu-id="46636-946">Method paint</span></span>

```xpp
public int paint()
```

### <a name="return-value---paint"></a><span data-ttu-id="46636-947">戻り値 - paint</span><span class="sxs-lookup"><span data-stu-id="46636-947">Return Value - paint</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="46636-948">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="46636-948">Method parentControl</span></span>

<span data-ttu-id="46636-949">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-949">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="46636-950">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="46636-950">Return Value - parentControl</span></span>

<span data-ttu-id="46636-951">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="46636-951">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="46636-952">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="46636-952">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="46636-953">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="46636-953">Parameters - previewPartRef</span></span>

<span data-ttu-id="46636-954">値</span><span class="sxs-lookup"><span data-stu-id="46636-954">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="46636-955">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="46636-955">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="46636-956">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="46636-956">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="46636-957">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="46636-957">Parameters - promptrect</span></span>

<span data-ttu-id="46636-958">値</span><span class="sxs-lookup"><span data-stu-id="46636-958">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="46636-959">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="46636-959">Return Value - promptrect</span></span>

## <a name="method-scrollinfo"></a><span data-ttu-id="46636-960">メソッド scrollInfo</span><span class="sxs-lookup"><span data-stu-id="46636-960">Method scrollInfo</span></span>

```xpp
public int scrollInfo(int VertScroller, [int Pos], [int PageDelta], [int MoveDelta], [int MinLimit], [int MaxLimit])
```

### <a name="parameters---scrollinfo"></a><span data-ttu-id="46636-961">パラメーター - scrollInfo</span><span class="sxs-lookup"><span data-stu-id="46636-961">Parameters - scrollInfo</span></span>

<span data-ttu-id="46636-962">VertScroller</span><span class="sxs-lookup"><span data-stu-id="46636-962">VertScroller</span></span>  

<!-- -->

<span data-ttu-id="46636-963">Pos</span><span class="sxs-lookup"><span data-stu-id="46636-963">Pos</span></span>  

<!-- -->

<span data-ttu-id="46636-964">PageDelta</span><span class="sxs-lookup"><span data-stu-id="46636-964">PageDelta</span></span>  

<!-- -->

<span data-ttu-id="46636-965">MoveDelta</span><span class="sxs-lookup"><span data-stu-id="46636-965">MoveDelta</span></span>  

<!-- -->

<span data-ttu-id="46636-966">MinLimit</span><span class="sxs-lookup"><span data-stu-id="46636-966">MinLimit</span></span>  

<!-- -->

<span data-ttu-id="46636-967">MaxLimit</span><span class="sxs-lookup"><span data-stu-id="46636-967">MaxLimit</span></span>  

### <a name="return-value---scrollinfo"></a><span data-ttu-id="46636-968">戻り値 - scrollInfo</span><span class="sxs-lookup"><span data-stu-id="46636-968">Return Value - scrollInfo</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="46636-969">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="46636-969">Method securityKey</span></span>

<span data-ttu-id="46636-970">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-970">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="46636-971">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="46636-971">Parameters - securityKey</span></span>

<span data-ttu-id="46636-972">値</span><span class="sxs-lookup"><span data-stu-id="46636-972">value</span></span>  
<span data-ttu-id="46636-973">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-973">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="46636-974">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="46636-974">Return Value - securityKey</span></span>

<span data-ttu-id="46636-975">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="46636-975">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="46636-976">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="46636-976">Method showContextMenu</span></span>

<span data-ttu-id="46636-977">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="46636-977">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="46636-978">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="46636-978">Parameters - showContextMenu</span></span>

<span data-ttu-id="46636-979">menuHandle</span><span class="sxs-lookup"><span data-stu-id="46636-979">menuHandle</span></span>  
<span data-ttu-id="46636-980">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="46636-980">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="46636-981">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="46636-981">Return Value - showContextMenu</span></span>

<span data-ttu-id="46636-982">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-982">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="46636-983">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="46636-983">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="46636-984">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="46636-984">Parameters - showLabel</span></span>

<span data-ttu-id="46636-985">値</span><span class="sxs-lookup"><span data-stu-id="46636-985">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="46636-986">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="46636-986">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="46636-987">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="46636-987">Method skip</span></span>

<span data-ttu-id="46636-988">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-988">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="46636-989">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="46636-989">Parameters - skip</span></span>

<span data-ttu-id="46636-990">値</span><span class="sxs-lookup"><span data-stu-id="46636-990">value</span></span>  
<span data-ttu-id="46636-991">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-991">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="46636-992">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="46636-992">Return Value - skip</span></span>

<span data-ttu-id="46636-993">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="46636-993">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="46636-994">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="46636-994">Remarks - skip</span></span>

<span data-ttu-id="46636-995">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="46636-995">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="46636-996">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="46636-996">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="46636-997">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="46636-997">Parameters - sort</span></span>

<span data-ttu-id="46636-998">sortDirection</span><span class="sxs-lookup"><span data-stu-id="46636-998">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="46636-999">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="46636-999">Return Value - sort</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="46636-1000">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="46636-1000">Method toolTip</span></span>

<span data-ttu-id="46636-1001">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="46636-1001">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="46636-1002">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="46636-1002">Return Value - toolTip</span></span>

<span data-ttu-id="46636-1003">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="46636-1003">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="46636-1004">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="46636-1004">Remarks - toolTip</span></span>

<span data-ttu-id="46636-1005">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="46636-1005">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="46636-1006">メソッド top</span><span class="sxs-lookup"><span data-stu-id="46636-1006">Method top</span></span>

<span data-ttu-id="46636-1007">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1007">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="46636-1008">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="46636-1008">Parameters - top</span></span>

<span data-ttu-id="46636-1009">値</span><span class="sxs-lookup"><span data-stu-id="46636-1009">value</span></span>  
<span data-ttu-id="46636-1010">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1010">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="46636-1011">モード</span><span class="sxs-lookup"><span data-stu-id="46636-1011">mode</span></span>  
<span data-ttu-id="46636-1012">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1012">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="46636-1013">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="46636-1013">Return Value - top</span></span>

<span data-ttu-id="46636-1014">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="46636-1014">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="46636-1015">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="46636-1015">Method topMode</span></span>

<span data-ttu-id="46636-1016">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1016">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="46636-1017">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="46636-1017">Parameters - topMode</span></span>

<span data-ttu-id="46636-1018">値</span><span class="sxs-lookup"><span data-stu-id="46636-1018">value</span></span>  
<span data-ttu-id="46636-1019">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1019">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="46636-1020">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="46636-1020">Return Value - topMode</span></span>

<span data-ttu-id="46636-1021">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="46636-1021">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="46636-1022">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="46636-1022">Method topValue</span></span>

<span data-ttu-id="46636-1023">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1023">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="46636-1024">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="46636-1024">Parameters - topValue</span></span>

<span data-ttu-id="46636-1025">値</span><span class="sxs-lookup"><span data-stu-id="46636-1025">value</span></span>  
<span data-ttu-id="46636-1026">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1026">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="46636-1027">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="46636-1027">Return Value - topValue</span></span>

<span data-ttu-id="46636-1028">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="46636-1028">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="46636-1029">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="46636-1029">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="46636-1030">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="46636-1030">Parameters - type</span></span>

<span data-ttu-id="46636-1031">値</span><span class="sxs-lookup"><span data-stu-id="46636-1031">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="46636-1032">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="46636-1032">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="46636-1033">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="46636-1033">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="46636-1034">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="46636-1034">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="46636-1035">データ</span><span class="sxs-lookup"><span data-stu-id="46636-1035">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="46636-1036">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="46636-1036">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="46636-1037">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="46636-1037">Method userData</span></span>

<span data-ttu-id="46636-1038">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1038">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="46636-1039">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="46636-1039">Parameters - userData</span></span>

<span data-ttu-id="46636-1040">値</span><span class="sxs-lookup"><span data-stu-id="46636-1040">value</span></span>  
<span data-ttu-id="46636-1041">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1041">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="46636-1042">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="46636-1042">Return Value - userData</span></span>

<span data-ttu-id="46636-1043">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="46636-1043">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="46636-1044">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="46636-1044">Method userDataItem</span></span>

<span data-ttu-id="46636-1045">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1045">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="46636-1046">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="46636-1046">Parameters - userDataItem</span></span>

<span data-ttu-id="46636-1047">値</span><span class="sxs-lookup"><span data-stu-id="46636-1047">value</span></span>  
<span data-ttu-id="46636-1048">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1048">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="46636-1049">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="46636-1049">Return Value - userDataItem</span></span>

<span data-ttu-id="46636-1050">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="46636-1050">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="46636-1051">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="46636-1051">Method userDataItems</span></span>

<span data-ttu-id="46636-1052">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1052">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="46636-1053">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="46636-1053">Parameters - userDataItems</span></span>

<span data-ttu-id="46636-1054">値</span><span class="sxs-lookup"><span data-stu-id="46636-1054">value</span></span>  
<span data-ttu-id="46636-1055">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1055">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="46636-1056">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="46636-1056">Return Value - userDataItems</span></span>

<span data-ttu-id="46636-1057">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="46636-1057">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="46636-1058">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="46636-1058">Method userDisable</span></span>

<span data-ttu-id="46636-1059">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1059">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="46636-1060">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="46636-1060">Parameters - userDisable</span></span>

<span data-ttu-id="46636-1061">値</span><span class="sxs-lookup"><span data-stu-id="46636-1061">value</span></span>  
<span data-ttu-id="46636-1062">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1062">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="46636-1063">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="46636-1063">Return Value - userDisable</span></span>

<span data-ttu-id="46636-1064">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="46636-1064">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="46636-1065">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="46636-1065">Method userHeight</span></span>

<span data-ttu-id="46636-1066">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1066">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="46636-1067">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="46636-1067">Parameters - userHeight</span></span>

<span data-ttu-id="46636-1068">値</span><span class="sxs-lookup"><span data-stu-id="46636-1068">value</span></span>  
<span data-ttu-id="46636-1069">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1069">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="46636-1070">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="46636-1070">Return Value - userHeight</span></span>

<span data-ttu-id="46636-1071">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="46636-1071">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="46636-1072">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="46636-1072">Method userHide</span></span>

<span data-ttu-id="46636-1073">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1073">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="46636-1074">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="46636-1074">Parameters - userHide</span></span>

<span data-ttu-id="46636-1075">値</span><span class="sxs-lookup"><span data-stu-id="46636-1075">value</span></span>  
<span data-ttu-id="46636-1076">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1076">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="46636-1077">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="46636-1077">Return Value - userHide</span></span>

<span data-ttu-id="46636-1078">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="46636-1078">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="46636-1079">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="46636-1079">Remarks - userHide</span></span>

<span data-ttu-id="46636-1080">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1080">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="46636-1081">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="46636-1081">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="46636-1082">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="46636-1082">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="46636-1083">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="46636-1083">Method userOrgContainer</span></span>

<span data-ttu-id="46636-1084">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1084">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="46636-1085">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="46636-1085">Parameters - userOrgContainer</span></span>

<span data-ttu-id="46636-1086">値</span><span class="sxs-lookup"><span data-stu-id="46636-1086">value</span></span>  
<span data-ttu-id="46636-1087">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1087">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="46636-1088">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="46636-1088">Return Value - userOrgContainer</span></span>

<span data-ttu-id="46636-1089">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="46636-1089">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="46636-1090">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="46636-1090">Method userOrgSibling</span></span>

<span data-ttu-id="46636-1091">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1091">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="46636-1092">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="46636-1092">Parameters - userOrgSibling</span></span>

<span data-ttu-id="46636-1093">値</span><span class="sxs-lookup"><span data-stu-id="46636-1093">value</span></span>  
<span data-ttu-id="46636-1094">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1094">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="46636-1095">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="46636-1095">Return Value - userOrgSibling</span></span>

<span data-ttu-id="46636-1096">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="46636-1096">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="46636-1097">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="46636-1097">Method userPromptText</span></span>

<span data-ttu-id="46636-1098">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1098">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="46636-1099">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="46636-1099">Parameters - userPromptText</span></span>

<span data-ttu-id="46636-1100">値</span><span class="sxs-lookup"><span data-stu-id="46636-1100">value</span></span>  
<span data-ttu-id="46636-1101">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1101">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="46636-1102">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="46636-1102">Return Value - userPromptText</span></span>

<span data-ttu-id="46636-1103">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="46636-1103">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="46636-1104">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="46636-1104">Method userSecurityLevel</span></span>

<span data-ttu-id="46636-1105">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1105">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="46636-1106">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="46636-1106">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="46636-1107">値</span><span class="sxs-lookup"><span data-stu-id="46636-1107">value</span></span>  
<span data-ttu-id="46636-1108">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1108">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="46636-1109">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="46636-1109">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="46636-1110">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="46636-1110">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="46636-1111">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="46636-1111">Method userSkip</span></span>

<span data-ttu-id="46636-1112">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-1112">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="46636-1113">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="46636-1113">Parameters - userSkip</span></span>

<span data-ttu-id="46636-1114">値</span><span class="sxs-lookup"><span data-stu-id="46636-1114">value</span></span>  
<span data-ttu-id="46636-1115">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1115">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="46636-1116">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="46636-1116">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="46636-1117">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="46636-1117">Return Value - userSkip</span></span>

<span data-ttu-id="46636-1118">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="46636-1118">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="46636-1119">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="46636-1119">Method userWidth</span></span>

<span data-ttu-id="46636-1120">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-1120">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="46636-1121">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="46636-1121">Parameters - userWidth</span></span>

<span data-ttu-id="46636-1122">値</span><span class="sxs-lookup"><span data-stu-id="46636-1122">value</span></span>  
<span data-ttu-id="46636-1123">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1123">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="46636-1124">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="46636-1124">Return Value - userWidth</span></span>

<span data-ttu-id="46636-1125">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="46636-1125">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="46636-1126">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="46636-1126">Remarks - userWidth</span></span>

<span data-ttu-id="46636-1127">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="46636-1127">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="46636-1128">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="46636-1128">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="46636-1129">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="46636-1129">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="46636-1130">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="46636-1130">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="46636-1131">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="46636-1131">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="46636-1132">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="46636-1132">Method verticalSpacing</span></span>

<span data-ttu-id="46636-1133">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1133">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="46636-1134">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="46636-1134">Parameters - verticalSpacing</span></span>

<span data-ttu-id="46636-1135">値</span><span class="sxs-lookup"><span data-stu-id="46636-1135">value</span></span>  
<span data-ttu-id="46636-1136">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1136">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="46636-1137">モード</span><span class="sxs-lookup"><span data-stu-id="46636-1137">mode</span></span>  
<span data-ttu-id="46636-1138">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1138">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="46636-1139">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="46636-1139">Return Value - verticalSpacing</span></span>

<span data-ttu-id="46636-1140">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="46636-1140">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="46636-1141">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="46636-1141">Method verticalSpacingMode</span></span>

<span data-ttu-id="46636-1142">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1142">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="46636-1143">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="46636-1143">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="46636-1144">モード</span><span class="sxs-lookup"><span data-stu-id="46636-1144">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="46636-1145">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="46636-1145">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="46636-1146">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="46636-1146">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="46636-1147">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="46636-1147">Method verticalSpacingValue</span></span>

<span data-ttu-id="46636-1148">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1148">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="46636-1149">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="46636-1149">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="46636-1150">値</span><span class="sxs-lookup"><span data-stu-id="46636-1150">value</span></span>  
<span data-ttu-id="46636-1151">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="46636-1151">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="46636-1152">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="46636-1152">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="46636-1153">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="46636-1153">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="46636-1154">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="46636-1154">Method visible</span></span>

<span data-ttu-id="46636-1155">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="46636-1155">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="46636-1156">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="46636-1156">Parameters - visible</span></span>

<span data-ttu-id="46636-1157">値</span><span class="sxs-lookup"><span data-stu-id="46636-1157">value</span></span>  
<span data-ttu-id="46636-1158">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1158">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="46636-1159">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="46636-1159">Return Value - visible</span></span>

<span data-ttu-id="46636-1160">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="46636-1160">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="46636-1161">メソッド width</span><span class="sxs-lookup"><span data-stu-id="46636-1161">Method width</span></span>

<span data-ttu-id="46636-1162">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1162">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="46636-1163">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="46636-1163">Parameters - width</span></span>

<span data-ttu-id="46636-1164">値</span><span class="sxs-lookup"><span data-stu-id="46636-1164">value</span></span>  

<!-- -->

<span data-ttu-id="46636-1165">モード</span><span class="sxs-lookup"><span data-stu-id="46636-1165">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="46636-1166">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="46636-1166">Return Value - width</span></span>

<span data-ttu-id="46636-1167">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="46636-1167">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="46636-1168">備考 - width</span><span class="sxs-lookup"><span data-stu-id="46636-1168">Remarks - width</span></span>

<span data-ttu-id="46636-1169">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="46636-1169">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="46636-1170">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="46636-1170">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="46636-1171">モード</span><span class="sxs-lookup"><span data-stu-id="46636-1171">Mode</span></span>           | <span data-ttu-id="46636-1172">幅計算</span><span class="sxs-lookup"><span data-stu-id="46636-1172">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46636-1173">-1 正確</span><span class="sxs-lookup"><span data-stu-id="46636-1173">-1 Exact</span></span>       | <span data-ttu-id="46636-1174">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="46636-1174">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="46636-1175">0 自動</span><span class="sxs-lookup"><span data-stu-id="46636-1175">0 Auto</span></span>         | <span data-ttu-id="46636-1176">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="46636-1176">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="46636-1177">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="46636-1177">1 Column width</span></span> | <span data-ttu-id="46636-1178">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="46636-1178">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="46636-1179">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="46636-1179">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="46636-1180">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="46636-1180">Method widthMode</span></span>

<span data-ttu-id="46636-1181">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1181">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="46636-1182">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="46636-1182">Parameters - widthMode</span></span>

<span data-ttu-id="46636-1183">値</span><span class="sxs-lookup"><span data-stu-id="46636-1183">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="46636-1184">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="46636-1184">Return Value - widthMode</span></span>

<span data-ttu-id="46636-1185">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1185">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="46636-1186">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="46636-1186">Remarks - widthMode</span></span>

<span data-ttu-id="46636-1187">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="46636-1187">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="46636-1188">モード</span><span class="sxs-lookup"><span data-stu-id="46636-1188">Mode</span></span>         | <span data-ttu-id="46636-1189">幅計算</span><span class="sxs-lookup"><span data-stu-id="46636-1189">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46636-1190">正確</span><span class="sxs-lookup"><span data-stu-id="46636-1190">Exact</span></span>        | <span data-ttu-id="46636-1191">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="46636-1191">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="46636-1192">自動</span><span class="sxs-lookup"><span data-stu-id="46636-1192">Auto</span></span>         | <span data-ttu-id="46636-1193">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="46636-1193">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="46636-1194">列の幅</span><span class="sxs-lookup"><span data-stu-id="46636-1194">Column width</span></span> | <span data-ttu-id="46636-1195">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="46636-1195">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="46636-1196">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="46636-1196">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="46636-1197">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="46636-1197">Method widthValue</span></span>

<span data-ttu-id="46636-1198">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1198">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="46636-1199">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="46636-1199">Parameters - widthValue</span></span>

<span data-ttu-id="46636-1200">値</span><span class="sxs-lookup"><span data-stu-id="46636-1200">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="46636-1201">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="46636-1201">Return Value - widthValue</span></span>

<span data-ttu-id="46636-1202">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="46636-1202">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="46636-1203">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="46636-1203">Remarks - widthValue</span></span>

<span data-ttu-id="46636-1204">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="46636-1204">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="46636-1205">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="46636-1205">Method lostFocus</span></span>

<span data-ttu-id="46636-1206">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-1206">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="46636-1207">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="46636-1207">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="46636-1208">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="46636-1208">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="46636-1209">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="46636-1209">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="46636-1210">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="46636-1210">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="46636-1211">overrideObject</span><span class="sxs-lookup"><span data-stu-id="46636-1211">overrideObject</span></span>  

## <a name="method-mouseenter"></a><span data-ttu-id="46636-1212">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="46636-1212">Method mouseEnter</span></span>

<span data-ttu-id="46636-1213">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-1213">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="46636-1214">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="46636-1214">Parameters - mouseEnter</span></span>

<span data-ttu-id="46636-1215">x</span><span class="sxs-lookup"><span data-stu-id="46636-1215">x</span></span>  
<span data-ttu-id="46636-1216">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-1216">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-1217">y</span><span class="sxs-lookup"><span data-stu-id="46636-1217">y</span></span>  
<span data-ttu-id="46636-1218">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-1218">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-1219">ボタン</span><span class="sxs-lookup"><span data-stu-id="46636-1219">button</span></span>  
<span data-ttu-id="46636-1220">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-1220">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-1221">Ctrl</span><span class="sxs-lookup"><span data-stu-id="46636-1221">Ctrl</span></span>  
<span data-ttu-id="46636-1222">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-1222">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="46636-1223">シフト</span><span class="sxs-lookup"><span data-stu-id="46636-1223">Shift</span></span>  
<span data-ttu-id="46636-1224">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="46636-1224">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="46636-1225">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="46636-1225">Method dragLeave</span></span>

<span data-ttu-id="46636-1226">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-1226">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-gotfocus"></a><span data-ttu-id="46636-1227">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="46636-1227">Method gotFocus</span></span>

<span data-ttu-id="46636-1228">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-1228">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-context"></a><span data-ttu-id="46636-1229">メソッド context</span><span class="sxs-lookup"><span data-stu-id="46636-1229">Method context</span></span>

<span data-ttu-id="46636-1230">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="46636-1230">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-lockdc"></a><span data-ttu-id="46636-1231">メソッド lockDC</span><span class="sxs-lookup"><span data-stu-id="46636-1231">Method lockDC</span></span>

```xpp
public void lockDC()
```

## <a name="method-enter"></a><span data-ttu-id="46636-1232">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="46636-1232">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-enddrag"></a><span data-ttu-id="46636-1233">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="46636-1233">Method endDrag</span></span>

<span data-ttu-id="46636-1234">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46636-1234">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="46636-1235">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="46636-1235">Remarks - endDrag</span></span>

<span data-ttu-id="46636-1236">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="46636-1236">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="46636-1237">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="46636-1237">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-onvalidating"></a><span data-ttu-id="46636-1238">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="46636-1238">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="46636-1239">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="46636-1239">Parameters - OnValidating</span></span>

<span data-ttu-id="46636-1240">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1240">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1241">e</span><span class="sxs-lookup"><span data-stu-id="46636-1241">e</span></span>  

## <a name="method-onenter"></a><span data-ttu-id="46636-1242">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="46636-1242">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="46636-1243">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="46636-1243">Parameters - OnEnter</span></span>

<span data-ttu-id="46636-1244">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1244">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1245">e</span><span class="sxs-lookup"><span data-stu-id="46636-1245">e</span></span>  

## <a name="method-setdirty"></a><span data-ttu-id="46636-1246">メソッド setDirty</span><span class="sxs-lookup"><span data-stu-id="46636-1246">Method setDirty</span></span>

```xpp
public void setDirty([int x], [int y], [int width], [int height])
```

### <a name="parameters---setdirty"></a><span data-ttu-id="46636-1247">パラメーター - setDirty</span><span class="sxs-lookup"><span data-stu-id="46636-1247">Parameters - setDirty</span></span>

<span data-ttu-id="46636-1248">x</span><span class="sxs-lookup"><span data-stu-id="46636-1248">x</span></span>  

<!-- -->

<span data-ttu-id="46636-1249">y</span><span class="sxs-lookup"><span data-stu-id="46636-1249">y</span></span>  

<!-- -->

<span data-ttu-id="46636-1250">width</span><span class="sxs-lookup"><span data-stu-id="46636-1250">width</span></span>  

<!-- -->

<span data-ttu-id="46636-1251">height</span><span class="sxs-lookup"><span data-stu-id="46636-1251">height</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="46636-1252">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="46636-1252">Method resetUserSetting</span></span>

<span data-ttu-id="46636-1253">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="46636-1253">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-onclicked"></a><span data-ttu-id="46636-1254">メソッド OnClicked</span><span class="sxs-lookup"><span data-stu-id="46636-1254">Method OnClicked</span></span>

```xpp
private void OnClicked([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onclicked"></a><span data-ttu-id="46636-1255">パラメーター - OnClicked</span><span class="sxs-lookup"><span data-stu-id="46636-1255">Parameters - OnClicked</span></span>

<span data-ttu-id="46636-1256">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1256">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1257">e</span><span class="sxs-lookup"><span data-stu-id="46636-1257">e</span></span>  

## <a name="method-onlookup"></a><span data-ttu-id="46636-1258">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="46636-1258">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="46636-1259">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="46636-1259">Parameters - OnLookup</span></span>

<span data-ttu-id="46636-1260">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1260">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1261">e</span><span class="sxs-lookup"><span data-stu-id="46636-1261">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="46636-1262">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="46636-1262">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="46636-1263">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="46636-1263">Parameters - filter</span></span>

<span data-ttu-id="46636-1264">filterStr</span><span class="sxs-lookup"><span data-stu-id="46636-1264">filterStr</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="46636-1265">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="46636-1265">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="46636-1266">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="46636-1266">Parameters - OnModified</span></span>

<span data-ttu-id="46636-1267">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1267">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1268">e</span><span class="sxs-lookup"><span data-stu-id="46636-1268">e</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="46636-1269">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="46636-1269">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="46636-1270">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="46636-1270">Parameters - OnValidated</span></span>

<span data-ttu-id="46636-1271">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1271">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1272">e</span><span class="sxs-lookup"><span data-stu-id="46636-1272">e</span></span>  

## <a name="method-size"></a><span data-ttu-id="46636-1273">メソッド size</span><span class="sxs-lookup"><span data-stu-id="46636-1273">Method size</span></span>

```xpp
public void size(int width, int height)
```

### <a name="parameters---size"></a><span data-ttu-id="46636-1274">パラメーター - size</span><span class="sxs-lookup"><span data-stu-id="46636-1274">Parameters - size</span></span>

<span data-ttu-id="46636-1275">width</span><span class="sxs-lookup"><span data-stu-id="46636-1275">width</span></span>  

<!-- -->

<span data-ttu-id="46636-1276">height</span><span class="sxs-lookup"><span data-stu-id="46636-1276">height</span></span>  

## <a name="method-dropfile"></a><span data-ttu-id="46636-1277">メソッド dropFile</span><span class="sxs-lookup"><span data-stu-id="46636-1277">Method dropFile</span></span>

```xpp
public void dropFile(str FileName)
```

### <a name="parameters---dropfile"></a><span data-ttu-id="46636-1278">パラメーター - dropFile</span><span class="sxs-lookup"><span data-stu-id="46636-1278">Parameters - dropFile</span></span>

<span data-ttu-id="46636-1279">FileName</span><span class="sxs-lookup"><span data-stu-id="46636-1279">FileName</span></span>  

## <a name="method-cut"></a><span data-ttu-id="46636-1280">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="46636-1280">Method cut</span></span>

<span data-ttu-id="46636-1281">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="46636-1281">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-lookup"></a><span data-ttu-id="46636-1282">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="46636-1282">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-setfocus"></a><span data-ttu-id="46636-1283">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="46636-1283">Method setFocus</span></span>

<span data-ttu-id="46636-1284">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1284">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-undo"></a><span data-ttu-id="46636-1285">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="46636-1285">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-onleaving"></a><span data-ttu-id="46636-1286">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="46636-1286">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="46636-1287">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="46636-1287">Parameters - OnLeaving</span></span>

<span data-ttu-id="46636-1288">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1288">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1289">e</span><span class="sxs-lookup"><span data-stu-id="46636-1289">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="46636-1290">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="46636-1290">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-setscrollinfo"></a><span data-ttu-id="46636-1291">メソッド setScrollInfo</span><span class="sxs-lookup"><span data-stu-id="46636-1291">Method setScrollInfo</span></span>

```xpp
public void setScrollInfo()
```

## <a name="method-paste"></a><span data-ttu-id="46636-1292">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="46636-1292">Method paste</span></span>

<span data-ttu-id="46636-1293">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="46636-1293">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="46636-1294">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="46636-1294">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="46636-1295">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="46636-1295">Parameters - OnGotFocus</span></span>

<span data-ttu-id="46636-1296">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1296">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1297">e</span><span class="sxs-lookup"><span data-stu-id="46636-1297">e</span></span>  

## <a name="method-clicked"></a><span data-ttu-id="46636-1298">メソッド clicked</span><span class="sxs-lookup"><span data-stu-id="46636-1298">Method clicked</span></span>

```xpp
public void clicked()
```

## <a name="method-inputsearch"></a><span data-ttu-id="46636-1299">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="46636-1299">Method inputSearch</span></span>

<span data-ttu-id="46636-1300">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="46636-1300">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="46636-1301">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="46636-1301">Parameters - inputSearch</span></span>

<span data-ttu-id="46636-1302">searchStr</span><span class="sxs-lookup"><span data-stu-id="46636-1302">searchStr</span></span>  
<span data-ttu-id="46636-1303">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="46636-1303">The string value to use to filter data; optional.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="46636-1304">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="46636-1304">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="46636-1305">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="46636-1305">Parameters - OnLostFocus</span></span>

<span data-ttu-id="46636-1306">sender</span><span class="sxs-lookup"><span data-stu-id="46636-1306">sender</span></span>  

<!-- -->

<span data-ttu-id="46636-1307">e</span><span class="sxs-lookup"><span data-stu-id="46636-1307">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="46636-1308">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="46636-1308">Method mouseLeave</span></span>

<span data-ttu-id="46636-1309">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="46636-1309">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-copy"></a><span data-ttu-id="46636-1310">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="46636-1310">Method copy</span></span>

<span data-ttu-id="46636-1311">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="46636-1311">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-drop"></a><span data-ttu-id="46636-1312">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="46636-1312">Method drop</span></span>

<span data-ttu-id="46636-1313">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-1313">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="46636-1314">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="46636-1314">Parameters - drop</span></span>

<span data-ttu-id="46636-1315">dragSource</span><span class="sxs-lookup"><span data-stu-id="46636-1315">dragSource</span></span>  
<span data-ttu-id="46636-1316">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1316">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-1317">dragMode</span><span class="sxs-lookup"><span data-stu-id="46636-1317">dragMode</span></span>  
<span data-ttu-id="46636-1318">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1318">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-1319">x</span><span class="sxs-lookup"><span data-stu-id="46636-1319">x</span></span>  
<span data-ttu-id="46636-1320">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1320">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-1321">y</span><span class="sxs-lookup"><span data-stu-id="46636-1321">y</span></span>  
<span data-ttu-id="46636-1322">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1322">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="46636-1323">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="46636-1323">Method displayControl</span></span>

<span data-ttu-id="46636-1324">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="46636-1324">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-unlockdc"></a><span data-ttu-id="46636-1325">メソッド unlockDC</span><span class="sxs-lookup"><span data-stu-id="46636-1325">Method unlockDC</span></span>

```xpp
public void unlockDC()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="46636-1326">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="46636-1326">Method prefColumnSize</span></span>

<span data-ttu-id="46636-1327">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="46636-1327">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="46636-1328">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="46636-1328">Parameters - prefColumnSize</span></span>

<span data-ttu-id="46636-1329">width</span><span class="sxs-lookup"><span data-stu-id="46636-1329">width</span></span>  
<span data-ttu-id="46636-1330">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="46636-1330">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="46636-1331">height</span><span class="sxs-lookup"><span data-stu-id="46636-1331">height</span></span>  
<span data-ttu-id="46636-1332">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="46636-1332">The preferred height of the control.</span></span>

## <a name="method-dropex"></a><span data-ttu-id="46636-1333">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="46636-1333">Method dropEx</span></span>

<span data-ttu-id="46636-1334">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="46636-1334">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="46636-1335">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="46636-1335">Parameters - dropEx</span></span>

<span data-ttu-id="46636-1336">dragSource</span><span class="sxs-lookup"><span data-stu-id="46636-1336">dragSource</span></span>  
<span data-ttu-id="46636-1337">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1337">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-1338">dragMode</span><span class="sxs-lookup"><span data-stu-id="46636-1338">dragMode</span></span>  
<span data-ttu-id="46636-1339">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1339">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-1340">x</span><span class="sxs-lookup"><span data-stu-id="46636-1340">x</span></span>  
<span data-ttu-id="46636-1341">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1341">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="46636-1342">y</span><span class="sxs-lookup"><span data-stu-id="46636-1342">y</span></span>  
<span data-ttu-id="46636-1343">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="46636-1343">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>



