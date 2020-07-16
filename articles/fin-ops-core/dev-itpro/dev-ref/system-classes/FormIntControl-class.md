---
title: FormIntControl クラス
description: このトピックでは、FormIntControl クラスについて説明します。
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
ms.openlocfilehash: bd9b4099034701d5aa8f7b892da58de2136c04f9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502934"
---
# <a name="class-formintcontrol"></a><span data-ttu-id="ec64d-103">クラス FormIntControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-103">Class FormIntControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormIntControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="ec64d-104">備考</span><span class="sxs-lookup"><span data-stu-id="ec64d-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="ec64d-105">例</span><span class="sxs-lookup"><span data-stu-id="ec64d-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ec64d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="ec64d-106">Methods</span></span>

| <span data-ttu-id="ec64d-107">方法</span><span class="sxs-lookup"><span data-stu-id="ec64d-107">Method</span></span>                                                                                                      | <span data-ttu-id="ec64d-108">説明</span><span class="sxs-lookup"><span data-stu-id="ec64d-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec64d-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="ec64d-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ec64d-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="ec64d-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="ec64d-114">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-114">public int allowNegative(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-115">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="ec64d-115">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="ec64d-116">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-116">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="ec64d-117">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-117">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="ec64d-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="ec64d-120">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-120">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="ec64d-121">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-121">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="ec64d-122">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-122">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="ec64d-123">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-123">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="ec64d-124">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ec64d-124">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="ec64d-125">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-125">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="ec64d-126">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-126">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="ec64d-127">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-127">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="ec64d-128">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-128">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="ec64d-129">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-129">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="ec64d-130">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-130">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-131">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="ec64d-131">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="ec64d-132">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-132">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="ec64d-133">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-133">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="ec64d-134">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-134">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="ec64d-135">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ec64d-135">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-136">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-136">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="ec64d-137">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-137">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ec64d-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="ec64d-139">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-139">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="ec64d-140">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="ec64d-140">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="ec64d-141">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-141">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="ec64d-142">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-142">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="ec64d-143">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-143">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="ec64d-144">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-144">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-145">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-145">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-146">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="ec64d-146">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-147">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="ec64d-147">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-148">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-148">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-149">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-149">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="ec64d-150">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-150">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="ec64d-151">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-151">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="ec64d-152">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-152">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="ec64d-153">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-153">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-154">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-154">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>                                               |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-155">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-155">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-156">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-156">public int displaceNegativeValue(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-157">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-157">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-158">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-158">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-159">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-159">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-160">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-160">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-161">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-161">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-162">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-162">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-163">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-163">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="ec64d-164">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-164">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="ec64d-165">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-165">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="ec64d-166">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-166">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="ec64d-167">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ec64d-167">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="ec64d-168">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-168">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="ec64d-169">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ec64d-169">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="ec64d-170">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-170">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="ec64d-171">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="ec64d-171">public str dragText()</span></span>                                                                                       | <span data-ttu-id="ec64d-172">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-172">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="ec64d-173">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-173">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="ec64d-174">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-174">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="ec64d-175">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-175">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-176">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-176">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-177">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-177">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="ec64d-178">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-178">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="ec64d-179">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-179">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="ec64d-180">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-180">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="ec64d-181">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-181">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="ec64d-182">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-182">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="ec64d-183">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="ec64d-183">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-184">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="ec64d-184">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-185">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="ec64d-185">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-186">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="ec64d-186">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-187">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="ec64d-187">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-188">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-188">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="ec64d-189">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-189">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="ec64d-190">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="ec64d-190">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="ec64d-191">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-191">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="ec64d-192">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-192">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="ec64d-193">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-193">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="ec64d-194">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-194">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="ec64d-195">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-195">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="ec64d-196">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-196">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="ec64d-197">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-197">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="ec64d-198">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="ec64d-198">public str helpField()</span></span>                                                                                      | <span data-ttu-id="ec64d-199">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-199">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ec64d-200">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-200">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="ec64d-201">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-201">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="ec64d-202">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-202">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="ec64d-203">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-203">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="ec64d-204">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="ec64d-204">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="ec64d-205">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-205">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ec64d-206">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-206">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-207">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="ec64d-207">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-208">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="ec64d-208">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="ec64d-209">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-209">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="ec64d-210">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="ec64d-210">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="ec64d-211">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-211">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="ec64d-212">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="ec64d-212">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="ec64d-213">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-213">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="ec64d-214">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="ec64d-214">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-215">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-215">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-216">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-216">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="ec64d-217">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-217">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="ec64d-218">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-218">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-219">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-219">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-220">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-220">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-221">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-221">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-222">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-222">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-223">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-223">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-224">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-224">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-225">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-225">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-226">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-226">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-227">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-227">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-228">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-228">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-229">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-229">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-230">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-230">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-231">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-231">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-232">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-232">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-233">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-233">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-234">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-234">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-235">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-235">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-236">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-236">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-237">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="ec64d-237">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-238">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-238">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="ec64d-239">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-239">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="ec64d-240">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-240">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="ec64d-241">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-241">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ec64d-242">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-242">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="ec64d-243">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-243">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="ec64d-244">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-244">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-245">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-245">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-246">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-246">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-247">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="ec64d-247">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-248">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="ec64d-248">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-249">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="ec64d-249">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-250">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-250">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-251">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-251">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-252">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-252">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="ec64d-253">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-253">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="ec64d-254">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="ec64d-254">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-255">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-255">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="ec64d-256">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-256">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="ec64d-257">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-257">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="ec64d-258">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-258">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="ec64d-259">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-259">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="ec64d-260">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-260">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="ec64d-261">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-261">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="ec64d-262">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-262">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="ec64d-263">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-263">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="ec64d-264">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-264">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="ec64d-265">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-265">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-266">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="ec64d-266">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-267">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="ec64d-267">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="ec64d-268">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-268">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ec64d-269">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="ec64d-269">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-270">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-270">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-271">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-271">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-272">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-272">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-273">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-273">public int rotateSign(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-274">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-274">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-275">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-275">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-276">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-276">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="ec64d-277">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-277">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="ec64d-278">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="ec64d-278">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="ec64d-279">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-279">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ec64d-280">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-280">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-281">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-281">public int showZero(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-282">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-282">public int signDisplay(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-283">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-283">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="ec64d-284">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-284">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="ec64d-285">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-285">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-286">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-286">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-287">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="ec64d-287">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="ec64d-288">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-288">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="ec64d-289">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-289">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="ec64d-290">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-290">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="ec64d-291">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-291">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="ec64d-292">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-292">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="ec64d-293">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-293">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="ec64d-294">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-294">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="ec64d-295">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-295">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-296">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-296">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="ec64d-297">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-297">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="ec64d-298">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="ec64d-298">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-299">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-299">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="ec64d-300">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-300">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="ec64d-301">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-301">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="ec64d-302">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-302">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="ec64d-303">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-303">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="ec64d-304">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-304">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="ec64d-305">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-305">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="ec64d-306">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-306">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="ec64d-307">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-307">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-308">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-308">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="ec64d-309">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-309">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="ec64d-310">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-310">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="ec64d-311">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-311">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="ec64d-312">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-312">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="ec64d-313">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-313">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="ec64d-314">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-314">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="ec64d-315">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-315">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ec64d-316">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-316">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="ec64d-317">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-317">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="ec64d-318">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-318">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="ec64d-319">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-319">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="ec64d-320">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-320">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="ec64d-321">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-321">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="ec64d-322">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-322">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="ec64d-323">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-323">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="ec64d-324">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="ec64d-324">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-325">public int value(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-325">public int value(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-326">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-326">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="ec64d-327">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-327">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ec64d-328">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-328">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="ec64d-329">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-329">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="ec64d-330">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-330">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="ec64d-331">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-331">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ec64d-332">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-332">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-333">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-333">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="ec64d-334">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-334">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="ec64d-335">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-335">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="ec64d-336">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-336">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="ec64d-337">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-337">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="ec64d-338">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-338">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="ec64d-339">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-339">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="ec64d-340">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-340">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="ec64d-341">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="ec64d-341">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="ec64d-342">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-342">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="ec64d-343">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ec64d-343">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="ec64d-344">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-344">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="ec64d-345">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-345">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-346">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="ec64d-346">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-347">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-347">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-348">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-348">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-349">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ec64d-349">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="ec64d-350">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-350">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="ec64d-351">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="ec64d-351">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="ec64d-352">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-352">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="ec64d-353">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="ec64d-353">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-354">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-354">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-355">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="ec64d-355">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-356">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="ec64d-356">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="ec64d-357">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-357">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ec64d-358">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="ec64d-358">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-359">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-359">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-360">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-360">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-361">public void context()</span><span class="sxs-lookup"><span data-stu-id="ec64d-361">public void context()</span></span>                                                                                       | <span data-ttu-id="ec64d-362">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-362">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ec64d-363">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="ec64d-363">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-364">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="ec64d-364">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="ec64d-365">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-365">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="ec64d-366">public void enter()</span><span class="sxs-lookup"><span data-stu-id="ec64d-366">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-367">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-367">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-368">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-368">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-369">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="ec64d-369">public void displayControl()</span></span>                                                                                | <span data-ttu-id="ec64d-370">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-370">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="ec64d-371">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-371">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-372">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ec64d-372">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="ec64d-373">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-373">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="ec64d-374">public void copy()</span><span class="sxs-lookup"><span data-stu-id="ec64d-374">public void copy()</span></span>                                                                                          | <span data-ttu-id="ec64d-375">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-375">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="ec64d-376">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="ec64d-376">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="ec64d-377">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-377">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="ec64d-378">public void undo()</span><span class="sxs-lookup"><span data-stu-id="ec64d-378">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-379">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="ec64d-379">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="ec64d-380">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-380">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="ec64d-381">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ec64d-381">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-382">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="ec64d-382">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-383">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="ec64d-383">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="ec64d-384">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-384">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="ec64d-385">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-385">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-386">public void paste()</span><span class="sxs-lookup"><span data-stu-id="ec64d-386">public void paste()</span></span>                                                                                         | <span data-ttu-id="ec64d-387">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-387">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ec64d-388">public void cut()</span><span class="sxs-lookup"><span data-stu-id="ec64d-388">public void cut()</span></span>                                                                                           | <span data-ttu-id="ec64d-389">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-389">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="ec64d-390">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="ec64d-390">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-391">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-391">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-392">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-392">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="ec64d-393">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="ec64d-393">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="ec64d-394">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-394">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="ec64d-395">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="ec64d-395">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="ec64d-396">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-396">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="ec64d-397">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="ec64d-397">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="ec64d-398">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-398">Method alignControl</span></span>

<span data-ttu-id="ec64d-399">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-399">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="ec64d-400">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-400">Parameters - alignControl</span></span>

<span data-ttu-id="ec64d-401">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-401">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="ec64d-402">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-402">Return Value - alignControl</span></span>

<span data-ttu-id="ec64d-403">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-403">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="ec64d-404">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-404">Remarks - alignControl</span></span>

<span data-ttu-id="ec64d-405">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-405">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="ec64d-406">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="ec64d-406">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="ec64d-407">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="ec64d-407">Parameters - alignment</span></span>

<span data-ttu-id="ec64d-408">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-408">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="ec64d-409">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="ec64d-409">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="ec64d-410">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="ec64d-410">Method allowEdit</span></span>

<span data-ttu-id="ec64d-411">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-411">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="ec64d-412">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ec64d-412">Parameters - allowEdit</span></span>

<span data-ttu-id="ec64d-413">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-413">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="ec64d-414">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ec64d-414">Return Value - allowEdit</span></span>

<span data-ttu-id="ec64d-415">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-415">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="ec64d-416">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ec64d-416">Remarks - allowEdit</span></span>

<span data-ttu-id="ec64d-417">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-417">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allownegative"></a><span data-ttu-id="ec64d-418">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="ec64d-418">Method allowNegative</span></span>

```xpp
public int allowNegative([int value])
```

### <a name="parameters---allownegative"></a><span data-ttu-id="ec64d-419">パラメーター - allowNegative</span><span class="sxs-lookup"><span data-stu-id="ec64d-419">Parameters - allowNegative</span></span>

<span data-ttu-id="ec64d-420">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-420">value</span></span>  

### <a name="return-value---allownegative"></a><span data-ttu-id="ec64d-421">戻り値 - allowNegative</span><span class="sxs-lookup"><span data-stu-id="ec64d-421">Return Value - allowNegative</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="ec64d-422">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="ec64d-422">Method allowSysSetup</span></span>

<span data-ttu-id="ec64d-423">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-423">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="ec64d-424">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="ec64d-424">Return Value - allowSysSetup</span></span>

<span data-ttu-id="ec64d-425">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-425">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="ec64d-426">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-426">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="ec64d-427">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-427">Parameters - arrayIndex</span></span>

<span data-ttu-id="ec64d-428">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-428">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="ec64d-429">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-429">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="ec64d-430">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ec64d-430">Method autoDeclaration</span></span>

<span data-ttu-id="ec64d-431">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-431">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="ec64d-432">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ec64d-432">Parameters - autoDeclaration</span></span>

<span data-ttu-id="ec64d-433">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-433">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="ec64d-434">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ec64d-434">Return Value - autoDeclaration</span></span>

<span data-ttu-id="ec64d-435">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-435">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="ec64d-436">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ec64d-436">Remarks - autoDeclaration</span></span>

<span data-ttu-id="ec64d-437">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-437">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="ec64d-438">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-438">Method backgroundColor</span></span>

<span data-ttu-id="ec64d-439">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-439">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="ec64d-440">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-440">Parameters - backgroundColor</span></span>

<span data-ttu-id="ec64d-441">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-441">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="ec64d-442">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-442">Return Value - backgroundColor</span></span>

<span data-ttu-id="ec64d-443">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="ec64d-443">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="ec64d-444">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-444">Remarks - backgroundColor</span></span>

<span data-ttu-id="ec64d-445">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-445">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="ec64d-446">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-446">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="ec64d-447">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-447">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="ec64d-448">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-448">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="ec64d-449">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-449">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="ec64d-450">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-450">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="ec64d-451">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="ec64d-451">Method backStyle</span></span>

<span data-ttu-id="ec64d-452">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-452">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="ec64d-453">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="ec64d-453">Parameters - backStyle</span></span>

<span data-ttu-id="ec64d-454">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-454">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="ec64d-455">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="ec64d-455">Return Value - backStyle</span></span>

<span data-ttu-id="ec64d-456">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-456">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="ec64d-457">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="ec64d-457">Method beginDrag</span></span>

<span data-ttu-id="ec64d-458">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-458">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="ec64d-459">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ec64d-459">Parameters - beginDrag</span></span>

<span data-ttu-id="ec64d-460">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-460">x</span></span>  
<span data-ttu-id="ec64d-461">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-461">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="ec64d-462">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-462">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="ec64d-463">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-463">y</span></span>  
<span data-ttu-id="ec64d-464">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-464">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="ec64d-465">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-465">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="ec64d-466">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ec64d-466">Return Value - beginDrag</span></span>

<span data-ttu-id="ec64d-467">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-467">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="ec64d-468">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ec64d-468">Remarks - beginDrag</span></span>

<span data-ttu-id="ec64d-469">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-469">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="ec64d-470">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-470">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="ec64d-471">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="ec64d-471">Method bold</span></span>

<span data-ttu-id="ec64d-472">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-472">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="ec64d-473">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="ec64d-473">Parameters - bold</span></span>

<span data-ttu-id="ec64d-474">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-474">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="ec64d-475">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="ec64d-475">Return Value - bold</span></span>

<span data-ttu-id="ec64d-476">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-476">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="ec64d-477">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="ec64d-477">Remarks - bold</span></span>

<span data-ttu-id="ec64d-478">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-478">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="ec64d-479">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-479">0 Use the default font weight.</span></span>
-   <span data-ttu-id="ec64d-480">1 シン。</span><span class="sxs-lookup"><span data-stu-id="ec64d-480">1 Thin.</span></span>
-   <span data-ttu-id="ec64d-481">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="ec64d-481">2 Extra-light.</span></span>
-   <span data-ttu-id="ec64d-482">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="ec64d-482">3 Light.</span></span>
-   <span data-ttu-id="ec64d-483">4 標準。</span><span class="sxs-lookup"><span data-stu-id="ec64d-483">4 Normal.</span></span>
-   <span data-ttu-id="ec64d-484">5 中。</span><span class="sxs-lookup"><span data-stu-id="ec64d-484">5 Medium.</span></span>
-   <span data-ttu-id="ec64d-485">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="ec64d-485">6 Semibold.</span></span>
-   <span data-ttu-id="ec64d-486">7 太字。</span><span class="sxs-lookup"><span data-stu-id="ec64d-486">7 Bold.</span></span>
-   <span data-ttu-id="ec64d-487">8 極太。</span><span class="sxs-lookup"><span data-stu-id="ec64d-487">8 Extra-bold.</span></span>
-   <span data-ttu-id="ec64d-488">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="ec64d-488">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="ec64d-489">メソッド border</span><span class="sxs-lookup"><span data-stu-id="ec64d-489">Method border</span></span>

<span data-ttu-id="ec64d-490">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-490">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="ec64d-491">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="ec64d-491">Parameters - border</span></span>

<span data-ttu-id="ec64d-492">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-492">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="ec64d-493">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="ec64d-493">Return Value - border</span></span>

<span data-ttu-id="ec64d-494">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="ec64d-494">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="ec64d-495">備考 - border</span><span class="sxs-lookup"><span data-stu-id="ec64d-495">Remarks - border</span></span>

<span data-ttu-id="ec64d-496">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-496">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="ec64d-497">値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-497">Value.</span></span> | <span data-ttu-id="ec64d-498">説明。</span><span class="sxs-lookup"><span data-stu-id="ec64d-498">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="ec64d-499">0</span><span class="sxs-lookup"><span data-stu-id="ec64d-499">0</span></span>      | <span data-ttu-id="ec64d-500">自動。</span><span class="sxs-lookup"><span data-stu-id="ec64d-500">Auto.</span></span>        |
| <span data-ttu-id="ec64d-501">1</span><span class="sxs-lookup"><span data-stu-id="ec64d-501">1</span></span>      | <span data-ttu-id="ec64d-502">3D。</span><span class="sxs-lookup"><span data-stu-id="ec64d-502">3D.</span></span>          |
| <span data-ttu-id="ec64d-503">2</span><span class="sxs-lookup"><span data-stu-id="ec64d-503">2</span></span>      | <span data-ttu-id="ec64d-504">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="ec64d-504">Single line.</span></span> |
| <span data-ttu-id="ec64d-505">3</span><span class="sxs-lookup"><span data-stu-id="ec64d-505">3</span></span>      | <span data-ttu-id="ec64d-506">均一。</span><span class="sxs-lookup"><span data-stu-id="ec64d-506">Flat.</span></span>        |
| <span data-ttu-id="ec64d-507">4</span><span class="sxs-lookup"><span data-stu-id="ec64d-507">4</span></span>      | <span data-ttu-id="ec64d-508">なし。</span><span class="sxs-lookup"><span data-stu-id="ec64d-508">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="ec64d-509">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-509">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="ec64d-510">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-510">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="ec64d-511">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-511">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="ec64d-512">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-512">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="ec64d-513">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-513">Method calcControlSize</span></span>

<span data-ttu-id="ec64d-514">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-514">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="ec64d-515">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-515">Parameters - calcControlSize</span></span>

<span data-ttu-id="ec64d-516">chars</span><span class="sxs-lookup"><span data-stu-id="ec64d-516">chars</span></span>  
<span data-ttu-id="ec64d-517">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="ec64d-517">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="ec64d-518">明細行</span><span class="sxs-lookup"><span data-stu-id="ec64d-518">lines</span></span>  
<span data-ttu-id="ec64d-519">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="ec64d-519">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="ec64d-520">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-520">Return Value - calcControlSize</span></span>

<span data-ttu-id="ec64d-521">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="ec64d-521">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="ec64d-522">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="ec64d-522">Method characterSet</span></span>

<span data-ttu-id="ec64d-523">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-523">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="ec64d-524">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="ec64d-524">Parameters - characterSet</span></span>

<span data-ttu-id="ec64d-525">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-525">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="ec64d-526">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="ec64d-526">Return Value - characterSet</span></span>

<span data-ttu-id="ec64d-527">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-527">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="ec64d-528">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="ec64d-528">Remarks - characterSet</span></span>

<span data-ttu-id="ec64d-529">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-529">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="ec64d-530">値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-530">Value.</span></span> | <span data-ttu-id="ec64d-531">説明。</span><span class="sxs-lookup"><span data-stu-id="ec64d-531">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="ec64d-532">0</span><span class="sxs-lookup"><span data-stu-id="ec64d-532">0</span></span>      | <span data-ttu-id="ec64d-533">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-533">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="ec64d-534">1</span><span class="sxs-lookup"><span data-stu-id="ec64d-534">1</span></span>      | <span data-ttu-id="ec64d-535">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-535">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="ec64d-536">2</span><span class="sxs-lookup"><span data-stu-id="ec64d-536">2</span></span>      | <span data-ttu-id="ec64d-537">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-537">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="ec64d-538">77</span><span class="sxs-lookup"><span data-stu-id="ec64d-538">77</span></span>     | <span data-ttu-id="ec64d-539">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-539">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="ec64d-540">128</span><span class="sxs-lookup"><span data-stu-id="ec64d-540">128</span></span>    | <span data-ttu-id="ec64d-541">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-541">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="ec64d-542">129</span><span class="sxs-lookup"><span data-stu-id="ec64d-542">129</span></span>    | <span data-ttu-id="ec64d-543">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-543">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="ec64d-544">134</span><span class="sxs-lookup"><span data-stu-id="ec64d-544">134</span></span>    | <span data-ttu-id="ec64d-545">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-545">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="ec64d-546">136</span><span class="sxs-lookup"><span data-stu-id="ec64d-546">136</span></span>    | <span data-ttu-id="ec64d-547">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-547">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="ec64d-548">161</span><span class="sxs-lookup"><span data-stu-id="ec64d-548">161</span></span>    | <span data-ttu-id="ec64d-549">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-549">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="ec64d-550">162</span><span class="sxs-lookup"><span data-stu-id="ec64d-550">162</span></span>    | <span data-ttu-id="ec64d-551">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-551">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="ec64d-552">163</span><span class="sxs-lookup"><span data-stu-id="ec64d-552">163</span></span>    | <span data-ttu-id="ec64d-553">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-553">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="ec64d-554">186</span><span class="sxs-lookup"><span data-stu-id="ec64d-554">186</span></span>    | <span data-ttu-id="ec64d-555">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-555">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="ec64d-556">204</span><span class="sxs-lookup"><span data-stu-id="ec64d-556">204</span></span>    | <span data-ttu-id="ec64d-557">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-557">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="ec64d-558">238</span><span class="sxs-lookup"><span data-stu-id="ec64d-558">238</span></span>    | <span data-ttu-id="ec64d-559">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-559">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="ec64d-560">255</span><span class="sxs-lookup"><span data-stu-id="ec64d-560">255</span></span>    | <span data-ttu-id="ec64d-561">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-561">OEM\_CHARSET</span></span>         |

<span data-ttu-id="ec64d-562">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-562">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="ec64d-563">値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-563">Value.</span></span> | <span data-ttu-id="ec64d-564">説明。</span><span class="sxs-lookup"><span data-stu-id="ec64d-564">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="ec64d-565">130</span><span class="sxs-lookup"><span data-stu-id="ec64d-565">130</span></span>    | <span data-ttu-id="ec64d-566">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-566">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="ec64d-567">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-567">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="ec64d-568">値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-568">Value.</span></span> | <span data-ttu-id="ec64d-569">説明。</span><span class="sxs-lookup"><span data-stu-id="ec64d-569">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="ec64d-570">177</span><span class="sxs-lookup"><span data-stu-id="ec64d-570">177</span></span>    | <span data-ttu-id="ec64d-571">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-571">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="ec64d-572">178</span><span class="sxs-lookup"><span data-stu-id="ec64d-572">178</span></span>    | <span data-ttu-id="ec64d-573">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-573">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="ec64d-574">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-574">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="ec64d-575">値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-575">Value.</span></span> | <span data-ttu-id="ec64d-576">説明。</span><span class="sxs-lookup"><span data-stu-id="ec64d-576">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="ec64d-577">222</span><span class="sxs-lookup"><span data-stu-id="ec64d-577">222</span></span>    | <span data-ttu-id="ec64d-578">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ec64d-578">THAI\_CHARSET</span></span> |

<span data-ttu-id="ec64d-579">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-579">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="ec64d-580">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-580">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="ec64d-581">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec64d-581">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-charfrompos"></a><span data-ttu-id="ec64d-582">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="ec64d-582">Method charFromPos</span></span>

```xpp
public int charFromPos(int x, int y)
```

### <a name="parameters---charfrompos"></a><span data-ttu-id="ec64d-583">パラメーター - charFromPos</span><span class="sxs-lookup"><span data-stu-id="ec64d-583">Parameters - charFromPos</span></span>

<span data-ttu-id="ec64d-584">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-584">x</span></span>  

<!-- -->

<span data-ttu-id="ec64d-585">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-585">y</span></span>  

### <a name="return-value---charfrompos"></a><span data-ttu-id="ec64d-586">戻り値 - charFromPos</span><span class="sxs-lookup"><span data-stu-id="ec64d-586">Return Value - charFromPos</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="ec64d-587">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="ec64d-587">Method colorScheme</span></span>

<span data-ttu-id="ec64d-588">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-588">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="ec64d-589">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ec64d-589">Parameters - colorScheme</span></span>

<span data-ttu-id="ec64d-590">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-590">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="ec64d-591">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ec64d-591">Return Value - colorScheme</span></span>

<span data-ttu-id="ec64d-592">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="ec64d-592">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="ec64d-593">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ec64d-593">Remarks - colorScheme</span></span>

<span data-ttu-id="ec64d-594">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-594">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="ec64d-595">値です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-595">Value.</span></span> | <span data-ttu-id="ec64d-596">スタイル。</span><span class="sxs-lookup"><span data-stu-id="ec64d-596">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="ec64d-597">0</span><span class="sxs-lookup"><span data-stu-id="ec64d-597">0</span></span>      | <span data-ttu-id="ec64d-598">既定。</span><span class="sxs-lookup"><span data-stu-id="ec64d-598">Default.</span></span>               |
| <span data-ttu-id="ec64d-599">1</span><span class="sxs-lookup"><span data-stu-id="ec64d-599">1</span></span>      | <span data-ttu-id="ec64d-600">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="ec64d-600">The Windows palette.</span></span>   |
| <span data-ttu-id="ec64d-601">2</span><span class="sxs-lookup"><span data-stu-id="ec64d-601">2</span></span>      | <span data-ttu-id="ec64d-602">真の配色。</span><span class="sxs-lookup"><span data-stu-id="ec64d-602">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="ec64d-603">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="ec64d-603">Method configurationKey</span></span>

<span data-ttu-id="ec64d-604">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-604">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="ec64d-605">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ec64d-605">Parameters - configurationKey</span></span>

<span data-ttu-id="ec64d-606">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-606">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="ec64d-607">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ec64d-607">Return Value - configurationKey</span></span>

<span data-ttu-id="ec64d-608">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="ec64d-608">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="ec64d-609">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ec64d-609">Remarks - configurationKey</span></span>

<span data-ttu-id="ec64d-610">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-610">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="ec64d-611">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-611">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="ec64d-612">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-612">Method configurationKeyEx</span></span>

<span data-ttu-id="ec64d-613">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-613">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="ec64d-614">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-614">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="ec64d-615">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="ec64d-615">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="ec64d-616">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-616">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="ec64d-617">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-617">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="ec64d-618">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-618">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="ec64d-619">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-619">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="ec64d-620">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ec64d-620">Method countryRegionCodes</span></span>

<span data-ttu-id="ec64d-621">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-621">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="ec64d-622">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ec64d-622">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="ec64d-623">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-623">value</span></span>  
<span data-ttu-id="ec64d-624">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-624">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="ec64d-625">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ec64d-625">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="ec64d-626">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="ec64d-626">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="ec64d-627">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ec64d-627">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="ec64d-628">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ec64d-628">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="ec64d-629">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-629">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="ec64d-630">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ec64d-630">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="ec64d-631">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="ec64d-631">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="ec64d-632">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="ec64d-632">Parameters - dataField</span></span>

<span data-ttu-id="ec64d-633">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-633">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="ec64d-634">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="ec64d-634">Return Value - dataField</span></span>

## <a name="method-datafieldarrayindex"></a><span data-ttu-id="ec64d-635">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-635">Method dataFieldArrayIndex</span></span>

```xpp
public int dataFieldArrayIndex()
```

### <a name="return-value---datafieldarrayindex"></a><span data-ttu-id="ec64d-636">戻り値 - dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-636">Return Value - dataFieldArrayIndex</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="ec64d-637">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="ec64d-637">Method dataFieldName</span></span>

```xpp
public FieldName dataFieldName()
```

### <a name="return-value---datafieldname"></a><span data-ttu-id="ec64d-638">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="ec64d-638">Return Value - dataFieldName</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="ec64d-639">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-639">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="ec64d-640">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-640">Parameters - dataMethod</span></span>

<span data-ttu-id="ec64d-641">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-641">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="ec64d-642">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-642">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="ec64d-643">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ec64d-643">Method dataRelationPath</span></span>

<span data-ttu-id="ec64d-644">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-644">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="ec64d-645">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ec64d-645">Parameters - dataRelationPath</span></span>

<span data-ttu-id="ec64d-646">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-646">value</span></span>  
<span data-ttu-id="ec64d-647">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-647">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="ec64d-648">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ec64d-648">Return Value - dataRelationPath</span></span>

<span data-ttu-id="ec64d-649">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="ec64d-649">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="ec64d-650">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ec64d-650">Remarks - dataRelationPath</span></span>

<span data-ttu-id="ec64d-651">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-651">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="ec64d-652">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="ec64d-652">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="ec64d-653">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="ec64d-653">Method dataSource</span></span>

<span data-ttu-id="ec64d-654">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-654">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="ec64d-655">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="ec64d-655">Parameters - dataSource</span></span>

<span data-ttu-id="ec64d-656">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-656">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="ec64d-657">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="ec64d-657">Return Value - dataSource</span></span>

<span data-ttu-id="ec64d-658">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="ec64d-658">The identifier of the data source to be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="ec64d-659">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="ec64d-659">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="ec64d-660">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="ec64d-660">Parameters - direction</span></span>

<span data-ttu-id="ec64d-661">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-661">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="ec64d-662">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="ec64d-662">Return Value - direction</span></span>

## <a name="method-displacenegative"></a><span data-ttu-id="ec64d-663">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="ec64d-663">Method displaceNegative</span></span>

```xpp
public int displaceNegative([int value], [AutoMode mode])
```

### <a name="parameters---displacenegative"></a><span data-ttu-id="ec64d-664">パラメーター - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="ec64d-664">Parameters - displaceNegative</span></span>

<span data-ttu-id="ec64d-665">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-665">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-666">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-666">mode</span></span>  

### <a name="return-value---displacenegative"></a><span data-ttu-id="ec64d-667">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="ec64d-667">Return Value - displaceNegative</span></span>

## <a name="method-displacenegativemode"></a><span data-ttu-id="ec64d-668">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-668">Method displaceNegativeMode</span></span>

```xpp
public AutoMode displaceNegativeMode([AutoMode mode])
```

### <a name="parameters---displacenegativemode"></a><span data-ttu-id="ec64d-669">パラメーター - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-669">Parameters - displaceNegativeMode</span></span>

<span data-ttu-id="ec64d-670">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-670">mode</span></span>  

### <a name="return-value---displacenegativemode"></a><span data-ttu-id="ec64d-671">戻り値 - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-671">Return Value - displaceNegativeMode</span></span>

## <a name="method-displacenegativevalue"></a><span data-ttu-id="ec64d-672">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-672">Method displaceNegativeValue</span></span>

```xpp
public int displaceNegativeValue([int value])
```

### <a name="parameters---displacenegativevalue"></a><span data-ttu-id="ec64d-673">パラメーター - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-673">Parameters - displaceNegativeValue</span></span>

<span data-ttu-id="ec64d-674">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-674">value</span></span>  

### <a name="return-value---displacenegativevalue"></a><span data-ttu-id="ec64d-675">戻り値 - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-675">Return Value - displaceNegativeValue</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="ec64d-676">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-676">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="ec64d-677">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-677">Parameters - displayHeight</span></span>

<span data-ttu-id="ec64d-678">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-678">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-679">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-679">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="ec64d-680">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-680">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="ec64d-681">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-681">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="ec64d-682">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-682">Parameters - displayHeightMode</span></span>

<span data-ttu-id="ec64d-683">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-683">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="ec64d-684">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-684">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="ec64d-685">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-685">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="ec64d-686">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-686">Parameters - displayHeightValue</span></span>

<span data-ttu-id="ec64d-687">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-687">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="ec64d-688">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-688">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="ec64d-689">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="ec64d-689">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="ec64d-690">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="ec64d-690">Parameters - displayLength</span></span>

<span data-ttu-id="ec64d-691">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-691">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-692">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-692">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="ec64d-693">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="ec64d-693">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="ec64d-694">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-694">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="ec64d-695">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-695">Parameters - displayLengthMode</span></span>

<span data-ttu-id="ec64d-696">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-696">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="ec64d-697">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-697">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="ec64d-698">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-698">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="ec64d-699">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-699">Parameters - displayLengthValue</span></span>

<span data-ttu-id="ec64d-700">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-700">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="ec64d-701">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-701">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="ec64d-702">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="ec64d-702">Method displayTarget</span></span>

<span data-ttu-id="ec64d-703">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-703">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="ec64d-704">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ec64d-704">Parameters - displayTarget</span></span>

<span data-ttu-id="ec64d-705">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-705">value</span></span>  
<span data-ttu-id="ec64d-706">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-706">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="ec64d-707">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ec64d-707">Return Value - displayTarget</span></span>

<span data-ttu-id="ec64d-708">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-708">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="ec64d-709">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="ec64d-709">Method dragDrop</span></span>

<span data-ttu-id="ec64d-710">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-710">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="ec64d-711">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ec64d-711">Parameters - dragDrop</span></span>

<span data-ttu-id="ec64d-712">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-712">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="ec64d-713">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ec64d-713">Return Value - dragDrop</span></span>

<span data-ttu-id="ec64d-714">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-714">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="ec64d-715">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="ec64d-715">Method dragOver</span></span>

<span data-ttu-id="ec64d-716">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-716">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="ec64d-717">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="ec64d-717">Parameters - dragOver</span></span>

<span data-ttu-id="ec64d-718">dragSource</span><span class="sxs-lookup"><span data-stu-id="ec64d-718">dragSource</span></span>  
<span data-ttu-id="ec64d-719">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-719">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-720">dragMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-720">dragMode</span></span>  
<span data-ttu-id="ec64d-721">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-721">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-722">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-722">x</span></span>  
<span data-ttu-id="ec64d-723">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-723">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-724">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-724">y</span></span>  
<span data-ttu-id="ec64d-725">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-725">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="ec64d-726">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="ec64d-726">Return Value - dragOver</span></span>

<span data-ttu-id="ec64d-727">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-727">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="ec64d-728">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-728">Method dragOverEx</span></span>

<span data-ttu-id="ec64d-729">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-729">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="ec64d-730">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-730">Parameters - dragOverEx</span></span>

<span data-ttu-id="ec64d-731">dragSource</span><span class="sxs-lookup"><span data-stu-id="ec64d-731">dragSource</span></span>  
<span data-ttu-id="ec64d-732">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-732">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-733">dragMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-733">dragMode</span></span>  
<span data-ttu-id="ec64d-734">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-734">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-735">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-735">x</span></span>  
<span data-ttu-id="ec64d-736">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-736">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-737">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-737">y</span></span>  
<span data-ttu-id="ec64d-738">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-738">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="ec64d-739">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-739">Return Value - dragOverEx</span></span>

<span data-ttu-id="ec64d-740">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-740">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="ec64d-741">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="ec64d-741">Method dragText</span></span>

<span data-ttu-id="ec64d-742">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-742">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="ec64d-743">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="ec64d-743">Return Value - dragText</span></span>

<span data-ttu-id="ec64d-744">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ec64d-744">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="ec64d-745">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-745">Method enabled</span></span>

<span data-ttu-id="ec64d-746">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-746">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="ec64d-747">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-747">Parameters - enabled</span></span>

<span data-ttu-id="ec64d-748">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-748">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="ec64d-749">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-749">Return Value - enabled</span></span>

<span data-ttu-id="ec64d-750">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-750">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="ec64d-751">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-751">Remarks - enabled</span></span>

<span data-ttu-id="ec64d-752">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-752">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="ec64d-753">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-753">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="ec64d-754">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-754">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="ec64d-755">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="ec64d-755">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="ec64d-756">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="ec64d-756">Parameters - extendedDataType</span></span>

<span data-ttu-id="ec64d-757">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-757">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="ec64d-758">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="ec64d-758">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="ec64d-759">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ec64d-759">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="ec64d-760">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ec64d-760">Parameters - fastTabSummary</span></span>

<span data-ttu-id="ec64d-761">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-761">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="ec64d-762">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ec64d-762">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="ec64d-763">メソッド font</span><span class="sxs-lookup"><span data-stu-id="ec64d-763">Method font</span></span>

<span data-ttu-id="ec64d-764">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-764">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="ec64d-765">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="ec64d-765">Parameters - font</span></span>

<span data-ttu-id="ec64d-766">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-766">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="ec64d-767">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="ec64d-767">Return Value - font</span></span>

<span data-ttu-id="ec64d-768">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="ec64d-768">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="ec64d-769">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-769">Method fontSize</span></span>

<span data-ttu-id="ec64d-770">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-770">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="ec64d-771">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-771">Parameters - fontSize</span></span>

<span data-ttu-id="ec64d-772">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-772">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="ec64d-773">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-773">Return Value - fontSize</span></span>

<span data-ttu-id="ec64d-774">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="ec64d-774">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="ec64d-775">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-775">Method foregroundColor</span></span>

<span data-ttu-id="ec64d-776">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-776">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="ec64d-777">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-777">Parameters - foregroundColor</span></span>

<span data-ttu-id="ec64d-778">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-778">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="ec64d-779">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-779">Return Value - foregroundColor</span></span>

<span data-ttu-id="ec64d-780">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="ec64d-780">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="ec64d-781">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-781">Remarks - foregroundColor</span></span>

<span data-ttu-id="ec64d-782">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-782">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="ec64d-783">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-783">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="ec64d-784">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-784">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="ec64d-785">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ec64d-785">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="ec64d-786">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-786">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="ec64d-787">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-787">The maximum value for a single byte is 255.</span></span>

## <a name="method-getcursorpos"></a><span data-ttu-id="ec64d-788">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="ec64d-788">Method getCursorPos</span></span>

```xpp
public container getCursorPos()
```

### <a name="return-value---getcursorpos"></a><span data-ttu-id="ec64d-789">戻り値 - getCursorPos</span><span class="sxs-lookup"><span data-stu-id="ec64d-789">Return Value - getCursorPos</span></span>

## <a name="method-getfirstvisibleline"></a><span data-ttu-id="ec64d-790">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="ec64d-790">Method getFirstVisibleLine</span></span>

```xpp
public int getFirstVisibleLine()
```

### <a name="return-value---getfirstvisibleline"></a><span data-ttu-id="ec64d-791">戻り値 - getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="ec64d-791">Return Value - getFirstVisibleLine</span></span>

## <a name="method-getline"></a><span data-ttu-id="ec64d-792">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="ec64d-792">Method getLine</span></span>

```xpp
public str getLine(int lineNo)
```

### <a name="parameters---getline"></a><span data-ttu-id="ec64d-793">パラメーター - getLine</span><span class="sxs-lookup"><span data-stu-id="ec64d-793">Parameters - getLine</span></span>

<span data-ttu-id="ec64d-794">lineNo</span><span class="sxs-lookup"><span data-stu-id="ec64d-794">lineNo</span></span>  

### <a name="return-value---getline"></a><span data-ttu-id="ec64d-795">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="ec64d-795">Return Value - getLine</span></span>

## <a name="method-getlinecount"></a><span data-ttu-id="ec64d-796">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="ec64d-796">Method getLineCount</span></span>

```xpp
public int getLineCount()
```

### <a name="return-value---getlinecount"></a><span data-ttu-id="ec64d-797">戻り値 - getLineCount</span><span class="sxs-lookup"><span data-stu-id="ec64d-797">Return Value - getLineCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="ec64d-798">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="ec64d-798">Method getSelection</span></span>

```xpp
public container getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="ec64d-799">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="ec64d-799">Return Value - getSelection</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="ec64d-800">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="ec64d-800">Method hasChanged</span></span>

<span data-ttu-id="ec64d-801">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-801">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="ec64d-802">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="ec64d-802">Parameters - hasChanged</span></span>

<span data-ttu-id="ec64d-803">val</span><span class="sxs-lookup"><span data-stu-id="ec64d-803">val</span></span>  
<span data-ttu-id="ec64d-804">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-804">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="ec64d-805">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="ec64d-805">Return Value - hasChanged</span></span>

<span data-ttu-id="ec64d-806">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-806">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="ec64d-807">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="ec64d-807">Method hasUserSetting</span></span>

<span data-ttu-id="ec64d-808">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-808">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="ec64d-809">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="ec64d-809">Return Value - hasUserSetting</span></span>

<span data-ttu-id="ec64d-810">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-810">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="ec64d-811">メソッド height</span><span class="sxs-lookup"><span data-stu-id="ec64d-811">Method height</span></span>

<span data-ttu-id="ec64d-812">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-812">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="ec64d-813">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="ec64d-813">Parameters - height</span></span>

<span data-ttu-id="ec64d-814">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-814">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-815">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-815">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="ec64d-816">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="ec64d-816">Return Value - height</span></span>

<span data-ttu-id="ec64d-817">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="ec64d-817">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="ec64d-818">備考 - height</span><span class="sxs-lookup"><span data-stu-id="ec64d-818">Remarks - height</span></span>

<span data-ttu-id="ec64d-819">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-819">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ec64d-820">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ec64d-820">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ec64d-821">モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-821">Mode.</span></span>            | <span data-ttu-id="ec64d-822">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ec64d-822">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec64d-823">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ec64d-823">-1 Exact.</span></span>        | <span data-ttu-id="ec64d-824">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-824">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ec64d-825">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ec64d-825">0 Auto.</span></span>          | <span data-ttu-id="ec64d-826">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-826">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ec64d-827">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="ec64d-827">1 Column height.</span></span> | <span data-ttu-id="ec64d-828">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-828">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ec64d-829">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-829">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="ec64d-830">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-830">Method heightMode</span></span>

<span data-ttu-id="ec64d-831">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-831">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="ec64d-832">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-832">Parameters - heightMode</span></span>

<span data-ttu-id="ec64d-833">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-833">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="ec64d-834">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-834">Return Value - heightMode</span></span>

<span data-ttu-id="ec64d-835">計算モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-835">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="ec64d-836">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-836">Remarks - heightMode</span></span>

<span data-ttu-id="ec64d-837">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ec64d-837">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ec64d-838">モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-838">Mode.</span></span>          | <span data-ttu-id="ec64d-839">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ec64d-839">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec64d-840">正確。</span><span class="sxs-lookup"><span data-stu-id="ec64d-840">Exact.</span></span>         | <span data-ttu-id="ec64d-841">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-841">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ec64d-842">自動。</span><span class="sxs-lookup"><span data-stu-id="ec64d-842">Auto.</span></span>          | <span data-ttu-id="ec64d-843">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-843">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ec64d-844">列の高さ</span><span class="sxs-lookup"><span data-stu-id="ec64d-844">Column height.</span></span> | <span data-ttu-id="ec64d-845">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-845">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ec64d-846">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-846">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="ec64d-847">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-847">Method heightValue</span></span>

<span data-ttu-id="ec64d-848">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-848">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="ec64d-849">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-849">Parameters - heightValue</span></span>

<span data-ttu-id="ec64d-850">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-850">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="ec64d-851">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-851">Return Value - heightValue</span></span>

<span data-ttu-id="ec64d-852">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="ec64d-852">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="ec64d-853">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-853">Remarks - heightValue</span></span>

<span data-ttu-id="ec64d-854">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-854">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="ec64d-855">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="ec64d-855">Method helpField</span></span>

<span data-ttu-id="ec64d-856">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-856">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="ec64d-857">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="ec64d-857">Return Value - helpField</span></span>

<span data-ttu-id="ec64d-858">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ec64d-858">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="ec64d-859">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="ec64d-859">Remarks - helpField</span></span>

<span data-ttu-id="ec64d-860">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-860">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="ec64d-861">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-861">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="ec64d-862">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="ec64d-862">Method helpText</span></span>

<span data-ttu-id="ec64d-863">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-863">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="ec64d-864">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="ec64d-864">Parameters - helpText</span></span>

<span data-ttu-id="ec64d-865">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-865">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="ec64d-866">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="ec64d-866">Return Value - helpText</span></span>

<span data-ttu-id="ec64d-867">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="ec64d-867">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="ec64d-868">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="ec64d-868">Remarks - helpText</span></span>

<span data-ttu-id="ec64d-869">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-869">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="ec64d-870">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-870">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="ec64d-871">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ec64d-871">Method hierarchyParent</span></span>

<span data-ttu-id="ec64d-872">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-872">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="ec64d-873">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ec64d-873">Parameters - hierarchyParent</span></span>

<span data-ttu-id="ec64d-874">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-874">value</span></span>  
<span data-ttu-id="ec64d-875">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-875">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="ec64d-876">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ec64d-876">Return Value - hierarchyParent</span></span>

<span data-ttu-id="ec64d-877">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-877">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="ec64d-878">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="ec64d-878">Method hWnd</span></span>

<span data-ttu-id="ec64d-879">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-879">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="ec64d-880">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="ec64d-880">Return Value - hWnd</span></span>

<span data-ttu-id="ec64d-881">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="ec64d-881">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="ec64d-882">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="ec64d-882">Remarks - hWnd</span></span>

<span data-ttu-id="ec64d-883">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-883">The handle can be used with the Windows API.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="ec64d-884">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-884">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="ec64d-885">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-885">Parameters - iMEMode</span></span>

<span data-ttu-id="ec64d-886">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-886">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="ec64d-887">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-887">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="ec64d-888">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="ec64d-888">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="ec64d-889">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="ec64d-889">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="ec64d-890">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ec64d-890">Method isDisplayed</span></span>

<span data-ttu-id="ec64d-891">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-891">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="ec64d-892">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ec64d-892">Return Value - isDisplayed</span></span>

<span data-ttu-id="ec64d-893">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-893">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="ec64d-894">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ec64d-894">Remarks - isDisplayed</span></span>

<span data-ttu-id="ec64d-895">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-895">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="ec64d-896">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="ec64d-896">Method isRestricted</span></span>

<span data-ttu-id="ec64d-897">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-897">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="ec64d-898">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="ec64d-898">Return Value - isRestricted</span></span>

<span data-ttu-id="ec64d-899">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-899">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="ec64d-900">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-900">Method isUserSetupEnabled</span></span>

<span data-ttu-id="ec64d-901">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-901">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="ec64d-902">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-902">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="ec64d-903">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="ec64d-903">neededSetupRights</span></span>  
<span data-ttu-id="ec64d-904">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-904">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="ec64d-905">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-905">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="ec64d-906">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-906">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="ec64d-907">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ec64d-907">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="ec64d-908">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-908">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span> <span data-ttu-id="ec64d-909">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-909">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec64d-910">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="ec64d-910">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="ec64d-911">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-911">No changes can be made to the control.</span></span> <span data-ttu-id="ec64d-912">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-912">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="ec64d-913">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="ec64d-913">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="ec64d-914">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-914">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="ec64d-915">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-915">The user cannot move the control.</span></span>   |
| <span data-ttu-id="ec64d-916">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="ec64d-916">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="ec64d-917">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-917">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="ec64d-918">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-918">The user can also move the control.</span></span> |

## <a name="method-isvalid"></a><span data-ttu-id="ec64d-919">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="ec64d-919">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="ec64d-920">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="ec64d-920">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="ec64d-921">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="ec64d-921">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="ec64d-922">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="ec64d-922">Parameters - italic</span></span>

<span data-ttu-id="ec64d-923">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-923">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="ec64d-924">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="ec64d-924">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="ec64d-925">メソッド label</span><span class="sxs-lookup"><span data-stu-id="ec64d-925">Method label</span></span>

<span data-ttu-id="ec64d-926">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-926">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="ec64d-927">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="ec64d-927">Parameters - label</span></span>

<span data-ttu-id="ec64d-928">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-928">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="ec64d-929">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="ec64d-929">Return Value - label</span></span>

<span data-ttu-id="ec64d-930">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-930">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="ec64d-931">備考 - label</span><span class="sxs-lookup"><span data-stu-id="ec64d-931">Remarks - label</span></span>

<span data-ttu-id="ec64d-932">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-932">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="ec64d-933">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-933">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="ec64d-934">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="ec64d-934">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="ec64d-935">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="ec64d-935">Parameters - labelAlignment</span></span>

<span data-ttu-id="ec64d-936">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-936">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="ec64d-937">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="ec64d-937">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="ec64d-938">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="ec64d-938">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="ec64d-939">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="ec64d-939">Parameters - labelBold</span></span>

<span data-ttu-id="ec64d-940">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-940">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="ec64d-941">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="ec64d-941">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="ec64d-942">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="ec64d-942">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="ec64d-943">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="ec64d-943">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="ec64d-944">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-944">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="ec64d-945">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="ec64d-945">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="ec64d-946">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="ec64d-946">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="ec64d-947">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="ec64d-947">Parameters - labelFont</span></span>

<span data-ttu-id="ec64d-948">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-948">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="ec64d-949">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="ec64d-949">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="ec64d-950">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-950">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="ec64d-951">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-951">Parameters - labelFontSize</span></span>

<span data-ttu-id="ec64d-952">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-952">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="ec64d-953">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-953">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="ec64d-954">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-954">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="ec64d-955">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-955">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="ec64d-956">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-956">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="ec64d-957">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="ec64d-957">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="ec64d-958">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="ec64d-958">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="ec64d-959">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="ec64d-959">Parameters - labelGuide</span></span>

<span data-ttu-id="ec64d-960">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-960">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="ec64d-961">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="ec64d-961">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="ec64d-962">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-962">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="ec64d-963">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-963">Parameters - labelHeight</span></span>

<span data-ttu-id="ec64d-964">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-964">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-965">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-965">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="ec64d-966">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-966">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="ec64d-967">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-967">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="ec64d-968">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-968">Parameters - labelHeightMode</span></span>

<span data-ttu-id="ec64d-969">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-969">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="ec64d-970">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-970">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="ec64d-971">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-971">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="ec64d-972">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-972">Parameters - labelHeightValue</span></span>

<span data-ttu-id="ec64d-973">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-973">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="ec64d-974">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-974">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="ec64d-975">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="ec64d-975">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="ec64d-976">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="ec64d-976">Parameters - labelItalic</span></span>

<span data-ttu-id="ec64d-977">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-977">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="ec64d-978">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="ec64d-978">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="ec64d-979">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ec64d-979">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="ec64d-980">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ec64d-980">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="ec64d-981">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-981">x</span></span>  

<!-- -->

<span data-ttu-id="ec64d-982">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-982">y</span></span>  

<!-- -->

<span data-ttu-id="ec64d-983">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-983">button</span></span>  

<!-- -->

<span data-ttu-id="ec64d-984">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-984">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="ec64d-985">Shift</span><span class="sxs-lookup"><span data-stu-id="ec64d-985">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="ec64d-986">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ec64d-986">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="ec64d-987">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="ec64d-987">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="ec64d-988">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="ec64d-988">Parameters - labelMouseDown</span></span>

<span data-ttu-id="ec64d-989">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-989">x</span></span>  

<!-- -->

<span data-ttu-id="ec64d-990">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-990">y</span></span>  

<!-- -->

<span data-ttu-id="ec64d-991">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-991">button</span></span>  

<!-- -->

<span data-ttu-id="ec64d-992">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-992">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="ec64d-993">Shift</span><span class="sxs-lookup"><span data-stu-id="ec64d-993">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="ec64d-994">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="ec64d-994">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="ec64d-995">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="ec64d-995">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="ec64d-996">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="ec64d-996">Parameters - labelMouseUp</span></span>

<span data-ttu-id="ec64d-997">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-997">x</span></span>  

<!-- -->

<span data-ttu-id="ec64d-998">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-998">y</span></span>  

<!-- -->

<span data-ttu-id="ec64d-999">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-999">button</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1000">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1000">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1001">Shift</span><span class="sxs-lookup"><span data-stu-id="ec64d-1001">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="ec64d-1002">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="ec64d-1002">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="ec64d-1003">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="ec64d-1003">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="ec64d-1004">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="ec64d-1004">Parameters - labelPosition</span></span>

<span data-ttu-id="ec64d-1005">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1005">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="ec64d-1006">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="ec64d-1006">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="ec64d-1007">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="ec64d-1007">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="ec64d-1008">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="ec64d-1008">Parameters - labelUnderline</span></span>

<span data-ttu-id="ec64d-1009">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1009">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="ec64d-1010">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="ec64d-1010">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="ec64d-1011">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="ec64d-1011">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="ec64d-1012">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="ec64d-1012">Parameters - labelWidth</span></span>

<span data-ttu-id="ec64d-1013">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1013">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1014">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1014">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="ec64d-1015">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="ec64d-1015">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="ec64d-1016">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1016">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="ec64d-1017">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1017">Parameters - labelWidthMode</span></span>

<span data-ttu-id="ec64d-1018">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1018">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="ec64d-1019">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1019">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="ec64d-1020">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1020">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="ec64d-1021">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1021">Parameters - labelWidthValue</span></span>

<span data-ttu-id="ec64d-1022">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1022">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="ec64d-1023">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1023">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="ec64d-1024">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="ec64d-1024">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="ec64d-1025">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="ec64d-1025">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="ec64d-1026">メソッド left</span><span class="sxs-lookup"><span data-stu-id="ec64d-1026">Method left</span></span>

<span data-ttu-id="ec64d-1027">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1027">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="ec64d-1028">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="ec64d-1028">Parameters - left</span></span>

<span data-ttu-id="ec64d-1029">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1029">value</span></span>  
<span data-ttu-id="ec64d-1030">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1030">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1031">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1031">mode</span></span>  
<span data-ttu-id="ec64d-1032">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1032">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="ec64d-1033">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="ec64d-1033">Return Value - left</span></span>

<span data-ttu-id="ec64d-1034">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1034">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="ec64d-1035">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1035">Method leftMode</span></span>

<span data-ttu-id="ec64d-1036">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1036">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="ec64d-1037">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1037">Parameters - leftMode</span></span>

<span data-ttu-id="ec64d-1038">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1038">value</span></span>  
<span data-ttu-id="ec64d-1039">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1039">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="ec64d-1040">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1040">Return Value - leftMode</span></span>

<span data-ttu-id="ec64d-1041">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1041">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="ec64d-1042">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1042">Method leftValue</span></span>

<span data-ttu-id="ec64d-1043">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1043">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="ec64d-1044">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1044">Parameters - leftValue</span></span>

<span data-ttu-id="ec64d-1045">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1045">value</span></span>  
<span data-ttu-id="ec64d-1046">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1046">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="ec64d-1047">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1047">Return Value - leftValue</span></span>

<span data-ttu-id="ec64d-1048">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1048">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="ec64d-1049">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1049">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="ec64d-1050">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1050">Parameters - limitText</span></span>

<span data-ttu-id="ec64d-1051">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1051">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1052">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1052">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="ec64d-1053">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1053">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="ec64d-1054">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1054">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="ec64d-1055">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1055">Parameters - limitTextMode</span></span>

<span data-ttu-id="ec64d-1056">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1056">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="ec64d-1057">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1057">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="ec64d-1058">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1058">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="ec64d-1059">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1059">Parameters - limitTextValue</span></span>

<span data-ttu-id="ec64d-1060">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1060">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="ec64d-1061">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1061">Return Value - limitTextValue</span></span>

## <a name="method-linefromchar"></a><span data-ttu-id="ec64d-1062">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="ec64d-1062">Method lineFromChar</span></span>

```xpp
public int lineFromChar(int charIndex)
```

### <a name="parameters---linefromchar"></a><span data-ttu-id="ec64d-1063">パラメーター - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="ec64d-1063">Parameters - lineFromChar</span></span>

<span data-ttu-id="ec64d-1064">charIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-1064">charIndex</span></span>  

### <a name="return-value---linefromchar"></a><span data-ttu-id="ec64d-1065">戻り値 - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="ec64d-1065">Return Value - lineFromChar</span></span>

## <a name="method-lineindex"></a><span data-ttu-id="ec64d-1066">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-1066">Method lineIndex</span></span>

```xpp
public int lineIndex(int lineNo)
```

### <a name="parameters---lineindex"></a><span data-ttu-id="ec64d-1067">パラメーター - lineIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-1067">Parameters - lineIndex</span></span>

<span data-ttu-id="ec64d-1068">lineNo</span><span class="sxs-lookup"><span data-stu-id="ec64d-1068">lineNo</span></span>  

### <a name="return-value---lineindex"></a><span data-ttu-id="ec64d-1069">戻り値 - lineIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-1069">Return Value - lineIndex</span></span>

## <a name="method-linelength"></a><span data-ttu-id="ec64d-1070">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="ec64d-1070">Method lineLength</span></span>

```xpp
public int lineLength(int lineNo)
```

### <a name="parameters---linelength"></a><span data-ttu-id="ec64d-1071">パラメーター - lineLength</span><span class="sxs-lookup"><span data-stu-id="ec64d-1071">Parameters - lineLength</span></span>

<span data-ttu-id="ec64d-1072">lineNo</span><span class="sxs-lookup"><span data-stu-id="ec64d-1072">lineNo</span></span>  

### <a name="return-value---linelength"></a><span data-ttu-id="ec64d-1073">戻り値 - lineLength</span><span class="sxs-lookup"><span data-stu-id="ec64d-1073">Return Value - lineLength</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="ec64d-1074">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="ec64d-1074">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="ec64d-1075">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="ec64d-1075">Parameters - lookupButton</span></span>

<span data-ttu-id="ec64d-1076">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1076">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="ec64d-1077">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="ec64d-1077">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="ec64d-1078">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="ec64d-1078">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="ec64d-1079">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="ec64d-1079">Parameters - mandatory</span></span>

<span data-ttu-id="ec64d-1080">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1080">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="ec64d-1081">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="ec64d-1081">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="ec64d-1082">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ec64d-1082">Method markAsUserAdd</span></span>

<span data-ttu-id="ec64d-1083">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1083">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="ec64d-1084">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ec64d-1084">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="ec64d-1085">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1085">value</span></span>  
<span data-ttu-id="ec64d-1086">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1086">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="ec64d-1087">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ec64d-1087">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="ec64d-1088">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1088">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="ec64d-1089">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="ec64d-1089">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="ec64d-1090">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="ec64d-1090">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="ec64d-1091">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ec64d-1091">Method mouseDblClick</span></span>

<span data-ttu-id="ec64d-1092">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1092">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="ec64d-1093">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ec64d-1093">Parameters - mouseDblClick</span></span>

<span data-ttu-id="ec64d-1094">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1094">x</span></span>  
<span data-ttu-id="ec64d-1095">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1095">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1096">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1096">y</span></span>  
<span data-ttu-id="ec64d-1097">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1097">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1098">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-1098">button</span></span>  
<span data-ttu-id="ec64d-1099">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1099">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1100">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1100">Ctrl</span></span>  
<span data-ttu-id="ec64d-1101">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1101">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1102">シフト</span><span class="sxs-lookup"><span data-stu-id="ec64d-1102">Shift</span></span>  
<span data-ttu-id="ec64d-1103">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1103">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="ec64d-1104">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ec64d-1104">Return Value - mouseDblClick</span></span>

<span data-ttu-id="ec64d-1105">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1105">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="ec64d-1106">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ec64d-1106">Remarks - mouseDblClick</span></span>

<span data-ttu-id="ec64d-1107">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1107">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="ec64d-1108">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="ec64d-1108">Method mouseDown</span></span>

<span data-ttu-id="ec64d-1109">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1109">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="ec64d-1110">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ec64d-1110">Parameters - mouseDown</span></span>

<span data-ttu-id="ec64d-1111">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1111">x</span></span>  
<span data-ttu-id="ec64d-1112">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1112">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1113">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1113">y</span></span>  
<span data-ttu-id="ec64d-1114">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1114">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1115">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-1115">button</span></span>  
<span data-ttu-id="ec64d-1116">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1116">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1117">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1117">Ctrl</span></span>  
<span data-ttu-id="ec64d-1118">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1118">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1119">シフト</span><span class="sxs-lookup"><span data-stu-id="ec64d-1119">Shift</span></span>  
<span data-ttu-id="ec64d-1120">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1120">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="ec64d-1121">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ec64d-1121">Return Value - mouseDown</span></span>

<span data-ttu-id="ec64d-1122">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1122">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="ec64d-1123">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ec64d-1123">Remarks - mouseDown</span></span>

<span data-ttu-id="ec64d-1124">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1124">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="ec64d-1125">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1125">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="ec64d-1126">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="ec64d-1126">Method mouseMove</span></span>

<span data-ttu-id="ec64d-1127">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1127">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="ec64d-1128">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ec64d-1128">Parameters - mouseMove</span></span>

<span data-ttu-id="ec64d-1129">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1129">x</span></span>  
<span data-ttu-id="ec64d-1130">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1130">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1131">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1131">y</span></span>  
<span data-ttu-id="ec64d-1132">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1132">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1133">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-1133">button</span></span>  
<span data-ttu-id="ec64d-1134">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1134">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1135">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1135">Ctrl</span></span>  
<span data-ttu-id="ec64d-1136">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1136">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1137">シフト</span><span class="sxs-lookup"><span data-stu-id="ec64d-1137">Shift</span></span>  
<span data-ttu-id="ec64d-1138">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1138">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="ec64d-1139">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ec64d-1139">Return Value - mouseMove</span></span>

<span data-ttu-id="ec64d-1140">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1140">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="ec64d-1141">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ec64d-1141">Remarks - mouseMove</span></span>

<span data-ttu-id="ec64d-1142">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1142">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="ec64d-1143">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="ec64d-1143">Method mouseUp</span></span>

<span data-ttu-id="ec64d-1144">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1144">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="ec64d-1145">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ec64d-1145">Parameters - mouseUp</span></span>

<span data-ttu-id="ec64d-1146">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1146">x</span></span>  
<span data-ttu-id="ec64d-1147">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1147">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1148">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1148">y</span></span>  
<span data-ttu-id="ec64d-1149">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1149">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1150">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-1150">button</span></span>  
<span data-ttu-id="ec64d-1151">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1151">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1152">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1152">Ctrl</span></span>  
<span data-ttu-id="ec64d-1153">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1153">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1154">シフト</span><span class="sxs-lookup"><span data-stu-id="ec64d-1154">Shift</span></span>  
<span data-ttu-id="ec64d-1155">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1155">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="ec64d-1156">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ec64d-1156">Return Value - mouseUp</span></span>

<span data-ttu-id="ec64d-1157">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1157">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="ec64d-1158">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ec64d-1158">Remarks - mouseUp</span></span>

<span data-ttu-id="ec64d-1159">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1159">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="ec64d-1160">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1160">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="ec64d-1161">メソッド名</span><span class="sxs-lookup"><span data-stu-id="ec64d-1161">Method name</span></span>

<span data-ttu-id="ec64d-1162">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1162">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="ec64d-1163">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="ec64d-1163">Parameters - name</span></span>

<span data-ttu-id="ec64d-1164">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1164">value</span></span>  
<span data-ttu-id="ec64d-1165">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1165">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="ec64d-1166">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="ec64d-1166">Return Value - name</span></span>

<span data-ttu-id="ec64d-1167">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1167">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="ec64d-1168">備考 - name</span><span class="sxs-lookup"><span data-stu-id="ec64d-1168">Remarks - name</span></span>

<span data-ttu-id="ec64d-1169">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1169">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="ec64d-1170">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1170">It must start with a letter.</span></span>
-   <span data-ttu-id="ec64d-1171">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1171">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="ec64d-1172">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1172">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="ec64d-1173">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1173">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="ec64d-1174">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1174">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="ec64d-1175">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="ec64d-1175">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="ec64d-1176">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ec64d-1176">Parameters - neededPermission</span></span>

<span data-ttu-id="ec64d-1177">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1177">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="ec64d-1178">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ec64d-1178">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="ec64d-1179">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ec64d-1179">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="ec64d-1180">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ec64d-1180">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="ec64d-1181">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1181">Method parentControl</span></span>

<span data-ttu-id="ec64d-1182">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1182">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="ec64d-1183">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1183">Return Value - parentControl</span></span>

<span data-ttu-id="ec64d-1184">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1184">The parent control for the control.</span></span>

## <a name="method-posfromchar"></a><span data-ttu-id="ec64d-1185">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="ec64d-1185">Method posFromChar</span></span>

```xpp
public container posFromChar(int charIndex)
```

### <a name="parameters---posfromchar"></a><span data-ttu-id="ec64d-1186">パラメーター - posFromChar</span><span class="sxs-lookup"><span data-stu-id="ec64d-1186">Parameters - posFromChar</span></span>

<span data-ttu-id="ec64d-1187">charIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-1187">charIndex</span></span>  

### <a name="return-value---posfromchar"></a><span data-ttu-id="ec64d-1188">戻り値 - posFromChar</span><span class="sxs-lookup"><span data-stu-id="ec64d-1188">Return Value - posFromChar</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="ec64d-1189">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="ec64d-1189">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="ec64d-1190">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="ec64d-1190">Parameters - previewPartRef</span></span>

<span data-ttu-id="ec64d-1191">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1191">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="ec64d-1192">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="ec64d-1192">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="ec64d-1193">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="ec64d-1193">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="ec64d-1194">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="ec64d-1194">Parameters - promptrect</span></span>

<span data-ttu-id="ec64d-1195">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1195">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="ec64d-1196">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="ec64d-1196">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="ec64d-1197">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1197">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="ec64d-1198">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1198">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="ec64d-1199">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1199">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="ec64d-1200">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1200">Return Value - replaceOnLookup</span></span>

## <a name="method-rotatesign"></a><span data-ttu-id="ec64d-1201">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="ec64d-1201">Method rotateSign</span></span>

```xpp
public int rotateSign([int value])
```

### <a name="parameters---rotatesign"></a><span data-ttu-id="ec64d-1202">パラメーター - rotateSign</span><span class="sxs-lookup"><span data-stu-id="ec64d-1202">Parameters - rotateSign</span></span>

<span data-ttu-id="ec64d-1203">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1203">value</span></span>  

### <a name="return-value---rotatesign"></a><span data-ttu-id="ec64d-1204">戻り値 - rotateSign</span><span class="sxs-lookup"><span data-stu-id="ec64d-1204">Return Value - rotateSign</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="ec64d-1205">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="ec64d-1205">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="ec64d-1206">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="ec64d-1206">Parameters - searchAfterInput</span></span>

<span data-ttu-id="ec64d-1207">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1207">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="ec64d-1208">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="ec64d-1208">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="ec64d-1209">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1209">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="ec64d-1210">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1210">Parameters - searchMode</span></span>

<span data-ttu-id="ec64d-1211">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1211">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="ec64d-1212">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1212">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="ec64d-1213">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="ec64d-1213">Method securityKey</span></span>

<span data-ttu-id="ec64d-1214">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1214">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="ec64d-1215">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="ec64d-1215">Parameters - securityKey</span></span>

<span data-ttu-id="ec64d-1216">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1216">value</span></span>  
<span data-ttu-id="ec64d-1217">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1217">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="ec64d-1218">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="ec64d-1218">Return Value - securityKey</span></span>

<span data-ttu-id="ec64d-1219">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1219">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="ec64d-1220">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ec64d-1220">Method showContextMenu</span></span>

<span data-ttu-id="ec64d-1221">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1221">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="ec64d-1222">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ec64d-1222">Parameters - showContextMenu</span></span>

<span data-ttu-id="ec64d-1223">menuHandle</span><span class="sxs-lookup"><span data-stu-id="ec64d-1223">menuHandle</span></span>  
<span data-ttu-id="ec64d-1224">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1224">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="ec64d-1225">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ec64d-1225">Return Value - showContextMenu</span></span>

<span data-ttu-id="ec64d-1226">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1226">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="ec64d-1227">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="ec64d-1227">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="ec64d-1228">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="ec64d-1228">Parameters - showLabel</span></span>

<span data-ttu-id="ec64d-1229">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1229">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="ec64d-1230">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="ec64d-1230">Return Value - showLabel</span></span>

## <a name="method-showzero"></a><span data-ttu-id="ec64d-1231">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="ec64d-1231">Method showZero</span></span>

```xpp
public int showZero([int value])
```

### <a name="parameters---showzero"></a><span data-ttu-id="ec64d-1232">パラメーター - showZero</span><span class="sxs-lookup"><span data-stu-id="ec64d-1232">Parameters - showZero</span></span>

<span data-ttu-id="ec64d-1233">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1233">value</span></span>  

### <a name="return-value---showzero"></a><span data-ttu-id="ec64d-1234">戻り値 - showZero</span><span class="sxs-lookup"><span data-stu-id="ec64d-1234">Return Value - showZero</span></span>

## <a name="method-signdisplay"></a><span data-ttu-id="ec64d-1235">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="ec64d-1235">Method signDisplay</span></span>

```xpp
public int signDisplay([int value])
```

### <a name="parameters---signdisplay"></a><span data-ttu-id="ec64d-1236">パラメーター - signDisplay</span><span class="sxs-lookup"><span data-stu-id="ec64d-1236">Parameters - signDisplay</span></span>

<span data-ttu-id="ec64d-1237">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1237">value</span></span>  

### <a name="return-value---signdisplay"></a><span data-ttu-id="ec64d-1238">戻り値 - signDisplay</span><span class="sxs-lookup"><span data-stu-id="ec64d-1238">Return Value - signDisplay</span></span>

## <a name="method-skip"></a><span data-ttu-id="ec64d-1239">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1239">Method skip</span></span>

<span data-ttu-id="ec64d-1240">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1240">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="ec64d-1241">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1241">Parameters - skip</span></span>

<span data-ttu-id="ec64d-1242">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1242">value</span></span>  
<span data-ttu-id="ec64d-1243">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1243">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="ec64d-1244">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1244">Return Value - skip</span></span>

<span data-ttu-id="ec64d-1245">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1245">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="ec64d-1246">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="ec64d-1246">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="ec64d-1247">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="ec64d-1247">Parameters - sort</span></span>

<span data-ttu-id="ec64d-1248">sortDirection</span><span class="sxs-lookup"><span data-stu-id="ec64d-1248">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="ec64d-1249">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="ec64d-1249">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="ec64d-1250">メソッド style</span><span class="sxs-lookup"><span data-stu-id="ec64d-1250">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="ec64d-1251">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="ec64d-1251">Parameters - style</span></span>

<span data-ttu-id="ec64d-1252">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1252">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="ec64d-1253">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="ec64d-1253">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="ec64d-1254">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1254">Method toolTip</span></span>

<span data-ttu-id="ec64d-1255">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1255">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="ec64d-1256">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1256">Return Value - toolTip</span></span>

<span data-ttu-id="ec64d-1257">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1257">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="ec64d-1258">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1258">Remarks - toolTip</span></span>

<span data-ttu-id="ec64d-1259">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1259">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="ec64d-1260">メソッド top</span><span class="sxs-lookup"><span data-stu-id="ec64d-1260">Method top</span></span>

<span data-ttu-id="ec64d-1261">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1261">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="ec64d-1262">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="ec64d-1262">Parameters - top</span></span>

<span data-ttu-id="ec64d-1263">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1263">value</span></span>  
<span data-ttu-id="ec64d-1264">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1264">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1265">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1265">mode</span></span>  
<span data-ttu-id="ec64d-1266">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1266">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="ec64d-1267">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="ec64d-1267">Return Value - top</span></span>

<span data-ttu-id="ec64d-1268">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1268">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="ec64d-1269">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1269">Method topMode</span></span>

<span data-ttu-id="ec64d-1270">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1270">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="ec64d-1271">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1271">Parameters - topMode</span></span>

<span data-ttu-id="ec64d-1272">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1272">value</span></span>  
<span data-ttu-id="ec64d-1273">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1273">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="ec64d-1274">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1274">Return Value - topMode</span></span>

<span data-ttu-id="ec64d-1275">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1275">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="ec64d-1276">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1276">Method topValue</span></span>

<span data-ttu-id="ec64d-1277">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1277">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="ec64d-1278">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1278">Parameters - topValue</span></span>

<span data-ttu-id="ec64d-1279">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1279">value</span></span>  
<span data-ttu-id="ec64d-1280">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1280">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="ec64d-1281">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1281">Return Value - topValue</span></span>

<span data-ttu-id="ec64d-1282">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1282">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="ec64d-1283">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="ec64d-1283">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="ec64d-1284">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="ec64d-1284">Parameters - type</span></span>

<span data-ttu-id="ec64d-1285">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1285">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="ec64d-1286">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="ec64d-1286">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="ec64d-1287">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="ec64d-1287">Method underline</span></span>

<span data-ttu-id="ec64d-1288">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1288">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="ec64d-1289">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="ec64d-1289">Parameters - underline</span></span>

<span data-ttu-id="ec64d-1290">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1290">value</span></span>  
<span data-ttu-id="ec64d-1291">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1291">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="ec64d-1292">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="ec64d-1292">Return Value - underline</span></span>

<span data-ttu-id="ec64d-1293">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1293">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="ec64d-1294">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ec64d-1294">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="ec64d-1295">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ec64d-1295">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="ec64d-1296">データ</span><span class="sxs-lookup"><span data-stu-id="ec64d-1296">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="ec64d-1297">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ec64d-1297">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="ec64d-1298">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="ec64d-1298">Method userData</span></span>

<span data-ttu-id="ec64d-1299">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1299">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="ec64d-1300">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="ec64d-1300">Parameters - userData</span></span>

<span data-ttu-id="ec64d-1301">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1301">value</span></span>  
<span data-ttu-id="ec64d-1302">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1302">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="ec64d-1303">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="ec64d-1303">Return Value - userData</span></span>

<span data-ttu-id="ec64d-1304">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1304">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="ec64d-1305">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="ec64d-1305">Method userDataItem</span></span>

<span data-ttu-id="ec64d-1306">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1306">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="ec64d-1307">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ec64d-1307">Parameters - userDataItem</span></span>

<span data-ttu-id="ec64d-1308">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1308">value</span></span>  
<span data-ttu-id="ec64d-1309">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1309">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="ec64d-1310">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ec64d-1310">Return Value - userDataItem</span></span>

<span data-ttu-id="ec64d-1311">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1311">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="ec64d-1312">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="ec64d-1312">Method userDataItems</span></span>

<span data-ttu-id="ec64d-1313">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1313">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="ec64d-1314">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ec64d-1314">Parameters - userDataItems</span></span>

<span data-ttu-id="ec64d-1315">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1315">value</span></span>  
<span data-ttu-id="ec64d-1316">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1316">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="ec64d-1317">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ec64d-1317">Return Value - userDataItems</span></span>

<span data-ttu-id="ec64d-1318">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1318">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="ec64d-1319">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="ec64d-1319">Method userDisable</span></span>

<span data-ttu-id="ec64d-1320">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1320">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="ec64d-1321">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="ec64d-1321">Parameters - userDisable</span></span>

<span data-ttu-id="ec64d-1322">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1322">value</span></span>  
<span data-ttu-id="ec64d-1323">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1323">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="ec64d-1324">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="ec64d-1324">Return Value - userDisable</span></span>

<span data-ttu-id="ec64d-1325">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1325">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="ec64d-1326">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ec64d-1326">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="ec64d-1327">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ec64d-1327">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="ec64d-1328">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1328">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="ec64d-1329">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ec64d-1329">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="ec64d-1330">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-1330">Method userHeight</span></span>

<span data-ttu-id="ec64d-1331">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1331">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="ec64d-1332">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-1332">Parameters - userHeight</span></span>

<span data-ttu-id="ec64d-1333">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1333">value</span></span>  
<span data-ttu-id="ec64d-1334">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1334">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="ec64d-1335">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="ec64d-1335">Return Value - userHeight</span></span>

<span data-ttu-id="ec64d-1336">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1336">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="ec64d-1337">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="ec64d-1337">Method userHide</span></span>

<span data-ttu-id="ec64d-1338">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1338">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="ec64d-1339">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="ec64d-1339">Parameters - userHide</span></span>

<span data-ttu-id="ec64d-1340">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1340">value</span></span>  
<span data-ttu-id="ec64d-1341">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1341">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="ec64d-1342">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="ec64d-1342">Return Value - userHide</span></span>

<span data-ttu-id="ec64d-1343">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1343">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="ec64d-1344">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="ec64d-1344">Remarks - userHide</span></span>

<span data-ttu-id="ec64d-1345">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1345">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="ec64d-1346">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1346">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="ec64d-1347">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1347">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="ec64d-1348">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ec64d-1348">Method userOrgContainer</span></span>

<span data-ttu-id="ec64d-1349">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1349">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="ec64d-1350">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ec64d-1350">Parameters - userOrgContainer</span></span>

<span data-ttu-id="ec64d-1351">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1351">value</span></span>  
<span data-ttu-id="ec64d-1352">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1352">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="ec64d-1353">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ec64d-1353">Return Value - userOrgContainer</span></span>

<span data-ttu-id="ec64d-1354">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1354">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="ec64d-1355">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ec64d-1355">Method userOrgSibling</span></span>

<span data-ttu-id="ec64d-1356">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1356">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="ec64d-1357">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ec64d-1357">Parameters - userOrgSibling</span></span>

<span data-ttu-id="ec64d-1358">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1358">value</span></span>  
<span data-ttu-id="ec64d-1359">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1359">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="ec64d-1360">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ec64d-1360">Return Value - userOrgSibling</span></span>

<span data-ttu-id="ec64d-1361">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1361">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="ec64d-1362">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1362">Method userPromptText</span></span>

<span data-ttu-id="ec64d-1363">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1363">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="ec64d-1364">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1364">Parameters - userPromptText</span></span>

<span data-ttu-id="ec64d-1365">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1365">value</span></span>  
<span data-ttu-id="ec64d-1366">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1366">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="ec64d-1367">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1367">Return Value - userPromptText</span></span>

<span data-ttu-id="ec64d-1368">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1368">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="ec64d-1369">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ec64d-1369">Method userSecurityLevel</span></span>

<span data-ttu-id="ec64d-1370">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1370">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="ec64d-1371">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ec64d-1371">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="ec64d-1372">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1372">value</span></span>  
<span data-ttu-id="ec64d-1373">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1373">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="ec64d-1374">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ec64d-1374">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="ec64d-1375">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1375">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="ec64d-1376">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1376">Method userSkip</span></span>

<span data-ttu-id="ec64d-1377">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1377">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="ec64d-1378">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1378">Parameters - userSkip</span></span>

<span data-ttu-id="ec64d-1379">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1379">value</span></span>  
<span data-ttu-id="ec64d-1380">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1380">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="ec64d-1381">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1381">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="ec64d-1382">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="ec64d-1382">Return Value - userSkip</span></span>

<span data-ttu-id="ec64d-1383">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1383">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="ec64d-1384">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="ec64d-1384">Method userWidth</span></span>

<span data-ttu-id="ec64d-1385">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1385">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="ec64d-1386">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="ec64d-1386">Parameters - userWidth</span></span>

<span data-ttu-id="ec64d-1387">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1387">value</span></span>  
<span data-ttu-id="ec64d-1388">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1388">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="ec64d-1389">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="ec64d-1389">Return Value - userWidth</span></span>

<span data-ttu-id="ec64d-1390">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1390">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="ec64d-1391">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="ec64d-1391">Remarks - userWidth</span></span>

<span data-ttu-id="ec64d-1392">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1392">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="ec64d-1393">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1393">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="ec64d-1394">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1394">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="ec64d-1395">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="ec64d-1395">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="ec64d-1396">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="ec64d-1396">Return Value - validate</span></span>

## <a name="method-value"></a><span data-ttu-id="ec64d-1397">メソッド value</span><span class="sxs-lookup"><span data-stu-id="ec64d-1397">Method value</span></span>

```xpp
public int value([int value])
```

### <a name="parameters---value"></a><span data-ttu-id="ec64d-1398">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="ec64d-1398">Parameters - value</span></span>

<span data-ttu-id="ec64d-1399">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1399">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="ec64d-1400">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="ec64d-1400">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="ec64d-1401">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ec64d-1401">Method verticalSpacing</span></span>

<span data-ttu-id="ec64d-1402">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1402">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="ec64d-1403">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ec64d-1403">Parameters - verticalSpacing</span></span>

<span data-ttu-id="ec64d-1404">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1404">value</span></span>  
<span data-ttu-id="ec64d-1405">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1405">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1406">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1406">mode</span></span>  
<span data-ttu-id="ec64d-1407">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1407">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="ec64d-1408">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ec64d-1408">Return Value - verticalSpacing</span></span>

<span data-ttu-id="ec64d-1409">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1409">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="ec64d-1410">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1410">Method verticalSpacingMode</span></span>

<span data-ttu-id="ec64d-1411">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1411">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="ec64d-1412">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1412">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="ec64d-1413">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1413">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="ec64d-1414">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1414">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="ec64d-1415">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1415">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="ec64d-1416">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1416">Method verticalSpacingValue</span></span>

<span data-ttu-id="ec64d-1417">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1417">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="ec64d-1418">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1418">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="ec64d-1419">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1419">value</span></span>  
<span data-ttu-id="ec64d-1420">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1420">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="ec64d-1421">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1421">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="ec64d-1422">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1422">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="ec64d-1423">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1423">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="ec64d-1424">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1424">Parameters - viewEditMode</span></span>

<span data-ttu-id="ec64d-1425">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1425">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="ec64d-1426">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1426">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="ec64d-1427">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="ec64d-1427">Method visible</span></span>

<span data-ttu-id="ec64d-1428">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1428">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="ec64d-1429">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="ec64d-1429">Parameters - visible</span></span>

<span data-ttu-id="ec64d-1430">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1430">value</span></span>  
<span data-ttu-id="ec64d-1431">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1431">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="ec64d-1432">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="ec64d-1432">Return Value - visible</span></span>

<span data-ttu-id="ec64d-1433">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1433">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="ec64d-1434">メソッド width</span><span class="sxs-lookup"><span data-stu-id="ec64d-1434">Method width</span></span>

<span data-ttu-id="ec64d-1435">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1435">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="ec64d-1436">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="ec64d-1436">Parameters - width</span></span>

<span data-ttu-id="ec64d-1437">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1437">value</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1438">モード</span><span class="sxs-lookup"><span data-stu-id="ec64d-1438">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="ec64d-1439">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="ec64d-1439">Return Value - width</span></span>

<span data-ttu-id="ec64d-1440">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1440">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="ec64d-1441">備考 - width</span><span class="sxs-lookup"><span data-stu-id="ec64d-1441">Remarks - width</span></span>

<span data-ttu-id="ec64d-1442">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1442">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ec64d-1443">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ec64d-1443">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ec64d-1444">モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1444">Mode.</span></span>           | <span data-ttu-id="ec64d-1445">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1445">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec64d-1446">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1446">-1 Exact.</span></span>       | <span data-ttu-id="ec64d-1447">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1447">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ec64d-1448">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1448">0 Auto.</span></span>         | <span data-ttu-id="ec64d-1449">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1449">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ec64d-1450">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1450">1 Column width.</span></span> | <span data-ttu-id="ec64d-1451">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1451">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ec64d-1452">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1452">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="ec64d-1453">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1453">Method widthMode</span></span>

<span data-ttu-id="ec64d-1454">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1454">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="ec64d-1455">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1455">Parameters - widthMode</span></span>

<span data-ttu-id="ec64d-1456">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1456">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="ec64d-1457">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1457">Return Value - widthMode</span></span>

<span data-ttu-id="ec64d-1458">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1458">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="ec64d-1459">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1459">Remarks - widthMode</span></span>

<span data-ttu-id="ec64d-1460">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ec64d-1460">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ec64d-1461">モード。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1461">Mode.</span></span>         | <span data-ttu-id="ec64d-1462">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1462">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec64d-1463">正確。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1463">Exact.</span></span>        | <span data-ttu-id="ec64d-1464">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1464">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ec64d-1465">自動。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1465">Auto.</span></span>         | <span data-ttu-id="ec64d-1466">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1466">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ec64d-1467">列の幅。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1467">Column width.</span></span> | <span data-ttu-id="ec64d-1468">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1468">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ec64d-1469">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1469">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="ec64d-1470">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1470">Method widthValue</span></span>

<span data-ttu-id="ec64d-1471">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1471">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="ec64d-1472">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1472">Parameters - widthValue</span></span>

<span data-ttu-id="ec64d-1473">値</span><span class="sxs-lookup"><span data-stu-id="ec64d-1473">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="ec64d-1474">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1474">Return Value - widthValue</span></span>

<span data-ttu-id="ec64d-1475">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1475">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="ec64d-1476">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ec64d-1476">Remarks - widthValue</span></span>

<span data-ttu-id="ec64d-1477">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1477">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="ec64d-1478">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="ec64d-1478">Method setFocus</span></span>

<span data-ttu-id="ec64d-1479">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1479">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="ec64d-1480">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="ec64d-1480">Method mouseEnter</span></span>

<span data-ttu-id="ec64d-1481">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1481">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="ec64d-1482">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="ec64d-1482">Parameters - mouseEnter</span></span>

<span data-ttu-id="ec64d-1483">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1483">x</span></span>  
<span data-ttu-id="ec64d-1484">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1484">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1485">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1485">y</span></span>  
<span data-ttu-id="ec64d-1486">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1486">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1487">ボタン</span><span class="sxs-lookup"><span data-stu-id="ec64d-1487">button</span></span>  
<span data-ttu-id="ec64d-1488">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1488">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1489">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1489">Ctrl</span></span>  
<span data-ttu-id="ec64d-1490">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1490">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1491">シフト</span><span class="sxs-lookup"><span data-stu-id="ec64d-1491">Shift</span></span>  
<span data-ttu-id="ec64d-1492">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1492">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-onmodified"></a><span data-ttu-id="ec64d-1493">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="ec64d-1493">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="ec64d-1494">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="ec64d-1494">Parameters - OnModified</span></span>

<span data-ttu-id="ec64d-1495">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1495">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1496">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1496">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="ec64d-1497">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="ec64d-1497">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="ec64d-1498">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="ec64d-1498">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="ec64d-1499">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="ec64d-1499">Parameters - OnGotFocus</span></span>

<span data-ttu-id="ec64d-1500">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1500">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1501">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1501">e</span></span>  

## <a name="method-performtypelookup"></a><span data-ttu-id="ec64d-1502">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1502">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="ec64d-1503">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1503">Parameters - performTypeLookup</span></span>

<span data-ttu-id="ec64d-1504">userType</span><span class="sxs-lookup"><span data-stu-id="ec64d-1504">userType</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1505">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ec64d-1505">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1506">会社</span><span class="sxs-lookup"><span data-stu-id="ec64d-1506">company</span></span>  

## <a name="method-drop"></a><span data-ttu-id="ec64d-1507">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="ec64d-1507">Method drop</span></span>

<span data-ttu-id="ec64d-1508">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1508">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="ec64d-1509">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="ec64d-1509">Parameters - drop</span></span>

<span data-ttu-id="ec64d-1510">dragSource</span><span class="sxs-lookup"><span data-stu-id="ec64d-1510">dragSource</span></span>  
<span data-ttu-id="ec64d-1511">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1511">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1512">dragMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1512">dragMode</span></span>  
<span data-ttu-id="ec64d-1513">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1513">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1514">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1514">x</span></span>  
<span data-ttu-id="ec64d-1515">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1515">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1516">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1516">y</span></span>  
<span data-ttu-id="ec64d-1517">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1517">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="ec64d-1518">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="ec64d-1518">Method endDrag</span></span>

<span data-ttu-id="ec64d-1519">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1519">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="ec64d-1520">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="ec64d-1520">Remarks - endDrag</span></span>

<span data-ttu-id="ec64d-1521">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1521">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="ec64d-1522">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1522">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-textchange"></a><span data-ttu-id="ec64d-1523">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="ec64d-1523">Method textChange</span></span>

```xpp
public void textChange()
```

## <a name="method-pastetext"></a><span data-ttu-id="ec64d-1524">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1524">Method pasteText</span></span>

```xpp
public void pasteText(str pasteStr, [boolean InsertSel])
```

### <a name="parameters---pastetext"></a><span data-ttu-id="ec64d-1525">パラメーター - pasteText</span><span class="sxs-lookup"><span data-stu-id="ec64d-1525">Parameters - pasteText</span></span>

<span data-ttu-id="ec64d-1526">pasteStr</span><span class="sxs-lookup"><span data-stu-id="ec64d-1526">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1527">InsertSel</span><span class="sxs-lookup"><span data-stu-id="ec64d-1527">InsertSel</span></span>  

## <a name="method-lookup"></a><span data-ttu-id="ec64d-1528">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1528">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-mouseleave"></a><span data-ttu-id="ec64d-1529">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="ec64d-1529">Method mouseLeave</span></span>

<span data-ttu-id="ec64d-1530">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1530">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-scrollcursor"></a><span data-ttu-id="ec64d-1531">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="ec64d-1531">Method scrollCursor</span></span>

```xpp
public void scrollCursor()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="ec64d-1532">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="ec64d-1532">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="ec64d-1533">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="ec64d-1533">Parameters - OnLostFocus</span></span>

<span data-ttu-id="ec64d-1534">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1534">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1535">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1535">e</span></span>  

## <a name="method-onvalidating"></a><span data-ttu-id="ec64d-1536">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="ec64d-1536">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="ec64d-1537">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="ec64d-1537">Parameters - OnValidating</span></span>

<span data-ttu-id="ec64d-1538">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1538">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1539">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1539">e</span></span>  

## <a name="method-context"></a><span data-ttu-id="ec64d-1540">メソッド context</span><span class="sxs-lookup"><span data-stu-id="ec64d-1540">Method context</span></span>

<span data-ttu-id="ec64d-1541">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1541">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-setselection"></a><span data-ttu-id="ec64d-1542">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="ec64d-1542">Method setSelection</span></span>

```xpp
public void setSelection(int charIndexFrom, int charIndexTo)
```

### <a name="parameters---setselection"></a><span data-ttu-id="ec64d-1543">パラメーター - setSelection</span><span class="sxs-lookup"><span data-stu-id="ec64d-1543">Parameters - setSelection</span></span>

<span data-ttu-id="ec64d-1544">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="ec64d-1544">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1545">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="ec64d-1545">charIndexTo</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="ec64d-1546">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="ec64d-1546">Method inputSearch</span></span>

<span data-ttu-id="ec64d-1547">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1547">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="ec64d-1548">パラメーター - inputSerach</span><span class="sxs-lookup"><span data-stu-id="ec64d-1548">Parameters - inputSearch</span></span>

<span data-ttu-id="ec64d-1549">searchStr</span><span class="sxs-lookup"><span data-stu-id="ec64d-1549">searchStr</span></span>  
<span data-ttu-id="ec64d-1550">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1550">The string value to use to filter data; optional.</span></span>

## <a name="method-enter"></a><span data-ttu-id="ec64d-1551">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="ec64d-1551">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-performdblookup"></a><span data-ttu-id="ec64d-1552">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1552">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="ec64d-1553">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1553">Parameters - performDBLookup</span></span>

<span data-ttu-id="ec64d-1554">fieldId</span><span class="sxs-lookup"><span data-stu-id="ec64d-1554">fieldId</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1555">tableId</span><span class="sxs-lookup"><span data-stu-id="ec64d-1555">tableId</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1556">会社</span><span class="sxs-lookup"><span data-stu-id="ec64d-1556">company</span></span>  

## <a name="method-onenter"></a><span data-ttu-id="ec64d-1557">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="ec64d-1557">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="ec64d-1558">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="ec64d-1558">Parameters - OnEnter</span></span>

<span data-ttu-id="ec64d-1559">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1559">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1560">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1560">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="ec64d-1561">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="ec64d-1561">Method displayControl</span></span>

<span data-ttu-id="ec64d-1562">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1562">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-filter"></a><span data-ttu-id="ec64d-1563">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="ec64d-1563">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="ec64d-1564">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="ec64d-1564">Parameters - filter</span></span>

<span data-ttu-id="ec64d-1565">filterStr</span><span class="sxs-lookup"><span data-stu-id="ec64d-1565">filterStr</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="ec64d-1566">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-1566">Method dropEx</span></span>

<span data-ttu-id="ec64d-1567">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1567">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="ec64d-1568">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="ec64d-1568">Parameters - dropEx</span></span>

<span data-ttu-id="ec64d-1569">dragSource</span><span class="sxs-lookup"><span data-stu-id="ec64d-1569">dragSource</span></span>  
<span data-ttu-id="ec64d-1570">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1570">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1571">dragMode</span><span class="sxs-lookup"><span data-stu-id="ec64d-1571">dragMode</span></span>  
<span data-ttu-id="ec64d-1572">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1572">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1573">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1573">x</span></span>  
<span data-ttu-id="ec64d-1574">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1574">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1575">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1575">y</span></span>  
<span data-ttu-id="ec64d-1576">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1576">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-copy"></a><span data-ttu-id="ec64d-1577">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="ec64d-1577">Method copy</span></span>

<span data-ttu-id="ec64d-1578">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1578">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-gotfocus"></a><span data-ttu-id="ec64d-1579">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="ec64d-1579">Method gotFocus</span></span>

<span data-ttu-id="ec64d-1580">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1580">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-undo"></a><span data-ttu-id="ec64d-1581">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="ec64d-1581">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="ec64d-1582">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="ec64d-1582">Method resetUserSetting</span></span>

<span data-ttu-id="ec64d-1583">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1583">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-setcursorpos"></a><span data-ttu-id="ec64d-1584">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="ec64d-1584">Method setCursorPos</span></span>

```xpp
public void setCursorPos(int x, int y)
```

### <a name="parameters---setcursorpos"></a><span data-ttu-id="ec64d-1585">パラメーター - setCursorPos</span><span class="sxs-lookup"><span data-stu-id="ec64d-1585">Parameters - setCursorPos</span></span>

<span data-ttu-id="ec64d-1586">x</span><span class="sxs-lookup"><span data-stu-id="ec64d-1586">x</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1587">y</span><span class="sxs-lookup"><span data-stu-id="ec64d-1587">y</span></span>  

## <a name="method-linescroll"></a><span data-ttu-id="ec64d-1588">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="ec64d-1588">Method lineScroll</span></span>

```xpp
public void lineScroll(int dx, int dy)
```

### <a name="parameters---linescroll"></a><span data-ttu-id="ec64d-1589">パラメーター - lineScroll</span><span class="sxs-lookup"><span data-stu-id="ec64d-1589">Parameters - lineScroll</span></span>

<span data-ttu-id="ec64d-1590">dx</span><span class="sxs-lookup"><span data-stu-id="ec64d-1590">dx</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1591">dy</span><span class="sxs-lookup"><span data-stu-id="ec64d-1591">dy</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="ec64d-1592">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="ec64d-1592">Method dragLeave</span></span>

<span data-ttu-id="ec64d-1593">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1593">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-onleaving"></a><span data-ttu-id="ec64d-1594">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="ec64d-1594">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="ec64d-1595">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="ec64d-1595">Parameters - OnLeaving</span></span>

<span data-ttu-id="ec64d-1596">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1596">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1597">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1597">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="ec64d-1598">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="ec64d-1598">Method paste</span></span>

<span data-ttu-id="ec64d-1599">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1599">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-cut"></a><span data-ttu-id="ec64d-1600">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="ec64d-1600">Method cut</span></span>

<span data-ttu-id="ec64d-1601">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1601">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-performformlookup"></a><span data-ttu-id="ec64d-1602">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1602">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="ec64d-1603">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1603">Parameters - performFormLookup</span></span>

<span data-ttu-id="ec64d-1604">フォーム</span><span class="sxs-lookup"><span data-stu-id="ec64d-1604">form</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="ec64d-1605">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="ec64d-1605">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="ec64d-1606">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="ec64d-1606">Parameters - OnValidated</span></span>

<span data-ttu-id="ec64d-1607">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1607">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1608">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1608">e</span></span>  

## <a name="method-onlookup"></a><span data-ttu-id="ec64d-1609">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1609">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="ec64d-1610">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="ec64d-1610">Parameters - OnLookup</span></span>

<span data-ttu-id="ec64d-1611">sender</span><span class="sxs-lookup"><span data-stu-id="ec64d-1611">sender</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1612">e</span><span class="sxs-lookup"><span data-stu-id="ec64d-1612">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="ec64d-1613">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-1613">Method prefColumnSize</span></span>

<span data-ttu-id="ec64d-1614">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1614">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="ec64d-1615">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="ec64d-1615">Parameters - prefColumnSize</span></span>

<span data-ttu-id="ec64d-1616">width</span><span class="sxs-lookup"><span data-stu-id="ec64d-1616">width</span></span>  
<span data-ttu-id="ec64d-1617">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1617">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="ec64d-1618">height</span><span class="sxs-lookup"><span data-stu-id="ec64d-1618">height</span></span>  
<span data-ttu-id="ec64d-1619">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1619">The preferred height of the control.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="ec64d-1620">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="ec64d-1620">Method lostFocus</span></span>

<span data-ttu-id="ec64d-1621">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="ec64d-1621">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="ec64d-1622">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-1622">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="ec64d-1623">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ec64d-1623">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="ec64d-1624">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="ec64d-1624">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1625">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="ec64d-1625">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="ec64d-1626">overrideObject</span><span class="sxs-lookup"><span data-stu-id="ec64d-1626">overrideObject</span></span>  



