---
title: FormTimeControl クラス
description: このトピックでは、FormTimeControl クラスについて説明します。
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
ms.openlocfilehash: 445951456e8f7e4a202e76472f1b555a0ff79b49
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502912"
---
# <a name="class-formtimecontrol"></a><span data-ttu-id="20f86-103">クラス FormTimeControl</span><span class="sxs-lookup"><span data-stu-id="20f86-103">Class FormTimeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormTimeControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="20f86-104">備考</span><span class="sxs-lookup"><span data-stu-id="20f86-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="20f86-105">例</span><span class="sxs-lookup"><span data-stu-id="20f86-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="20f86-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="20f86-106">Methods</span></span>

| <span data-ttu-id="20f86-107">方法</span><span class="sxs-lookup"><span data-stu-id="20f86-107">Method</span></span>                                                                                                      | <span data-ttu-id="20f86-108">説明</span><span class="sxs-lookup"><span data-stu-id="20f86-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f86-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="20f86-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="20f86-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="20f86-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="20f86-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="20f86-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="20f86-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="20f86-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="20f86-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="20f86-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="20f86-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="20f86-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="20f86-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="20f86-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="20f86-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="20f86-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-124">Is called when the user begins dragging a form control.</span></span>                                                                                                                 |
| <span data-ttu-id="20f86-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="20f86-126">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-126">Gets or sets the weight of font that was used to output text in the control.</span></span>                                                                                            |
| <span data-ttu-id="20f86-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="20f86-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="20f86-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="20f86-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="20f86-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="20f86-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="20f86-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="20f86-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-133">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="20f86-134">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="20f86-134">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-135">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-135">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="20f86-136">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-136">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="20f86-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="20f86-138">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-138">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="20f86-139">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="20f86-139">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="20f86-140">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-140">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="20f86-141">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-141">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="20f86-142">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-142">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="20f86-143">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-143">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-144">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-144">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-145">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="20f86-145">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-146">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="20f86-146">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-147">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-147">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-148">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-148">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="20f86-149">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-149">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="20f86-150">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-150">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="20f86-151">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-151">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="20f86-152">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-152">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-153">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-153">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-154">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-154">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-155">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-155">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-156">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-156">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-157">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-157">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-158">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-158">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-159">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-159">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="20f86-160">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-160">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="20f86-161">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-161">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="20f86-162">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-162">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                        |
| <span data-ttu-id="20f86-163">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="20f86-163">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="20f86-164">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-164">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="20f86-165">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="20f86-165">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="20f86-166">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-166">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="20f86-167">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="20f86-167">public str dragText()</span></span>                                                                                       | <span data-ttu-id="20f86-168">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-168">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="20f86-169">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-169">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="20f86-170">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-170">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="20f86-171">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-171">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-172">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-172">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-173">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-173">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="20f86-174">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-174">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="20f86-175">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-175">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="20f86-176">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-176">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="20f86-177">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-177">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="20f86-178">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-178">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="20f86-179">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="20f86-179">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="20f86-180">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="20f86-180">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-181">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="20f86-181">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="20f86-182">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="20f86-182">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="20f86-183">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="20f86-183">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="20f86-184">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="20f86-184">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="20f86-185">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-185">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="20f86-186">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="20f86-186">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="20f86-187">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-187">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="20f86-188">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-188">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="20f86-189">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-189">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="20f86-190">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-190">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="20f86-191">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-191">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="20f86-192">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-192">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="20f86-193">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-193">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="20f86-194">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="20f86-194">public str helpField()</span></span>                                                                                      | <span data-ttu-id="20f86-195">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-195">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="20f86-196">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-196">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="20f86-197">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-197">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="20f86-198">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-198">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="20f86-199">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-199">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="20f86-200">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="20f86-200">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="20f86-201">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-201">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="20f86-202">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-202">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="20f86-203">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="20f86-203">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-204">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="20f86-204">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="20f86-205">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-205">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="20f86-206">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="20f86-206">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="20f86-207">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-207">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="20f86-208">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="20f86-208">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="20f86-209">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-209">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="20f86-210">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="20f86-210">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-211">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-211">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-212">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-212">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="20f86-213">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-213">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="20f86-214">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-214">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-215">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-215">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-216">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-216">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-217">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-217">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-218">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-218">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="20f86-219">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-219">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="20f86-220">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-220">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-221">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-221">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="20f86-222">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-222">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="20f86-223">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-223">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-224">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-224">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="20f86-225">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-225">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-226">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-226">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-227">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-227">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="20f86-228">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-228">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="20f86-229">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-229">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-230">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-230">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="20f86-231">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-231">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-232">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-232">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="20f86-233">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="20f86-233">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="20f86-234">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-234">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="20f86-235">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-235">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="20f86-236">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-236">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="20f86-237">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-237">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="20f86-238">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-238">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="20f86-239">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-239">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="20f86-240">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-240">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="20f86-241">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-241">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-242">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-242">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-243">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="20f86-243">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="20f86-244">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="20f86-244">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="20f86-245">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="20f86-245">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="20f86-246">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-246">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="20f86-247">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-247">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-248">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-248">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="20f86-249">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="20f86-249">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="20f86-250">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="20f86-250">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="20f86-251">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-251">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="20f86-252">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-252">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="20f86-253">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-253">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="20f86-254">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-254">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="20f86-255">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-255">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="20f86-256">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-256">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="20f86-257">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-257">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="20f86-258">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-258">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="20f86-259">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-259">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="20f86-260">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-260">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                               |
| <span data-ttu-id="20f86-261">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-261">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-262">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="20f86-262">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="20f86-263">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="20f86-263">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="20f86-264">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-264">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="20f86-265">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="20f86-265">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-266">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-266">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-267">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-267">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-268">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-268">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="20f86-269">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-269">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-270">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-270">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="20f86-272">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-272">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="20f86-273">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="20f86-273">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="20f86-274">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-274">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="20f86-275">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-275">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-276">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-276">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="20f86-277">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-277">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="20f86-278">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="20f86-278">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-279">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-279">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="20f86-280">public int timeFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-280">public int timeFormat(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-281">public int timeHours(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-281">public int timeHours(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-282">public int timeMinute(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-282">public int timeMinute(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-283">public int timeSeconds(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-283">public int timeSeconds(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="20f86-284">public int timeSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-284">public int timeSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="20f86-285">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="20f86-285">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="20f86-286">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-286">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="20f86-287">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-287">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="20f86-288">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-288">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="20f86-289">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-289">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="20f86-290">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-290">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="20f86-291">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-291">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="20f86-292">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-292">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="20f86-293">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-293">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="20f86-294">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-294">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-295">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="20f86-295">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-296">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-296">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="20f86-297">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-297">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="20f86-298">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-298">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="20f86-299">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-299">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="20f86-300">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-300">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="20f86-301">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-301">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="20f86-302">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-302">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="20f86-303">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-303">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="20f86-304">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-304">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-305">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-305">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="20f86-306">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-306">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="20f86-307">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-307">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="20f86-308">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-308">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="20f86-309">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-309">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="20f86-310">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-310">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="20f86-311">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-311">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="20f86-312">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-312">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="20f86-313">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-313">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="20f86-314">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-314">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="20f86-315">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-315">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="20f86-316">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-316">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="20f86-317">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-317">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="20f86-318">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-318">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="20f86-319">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-319">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="20f86-320">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-320">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="20f86-321">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="20f86-321">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="20f86-322">public int value(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-322">public int value(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="20f86-323">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-323">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="20f86-324">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-324">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="20f86-325">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-325">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="20f86-326">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-326">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="20f86-327">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-327">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="20f86-328">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-328">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="20f86-329">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-329">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="20f86-330">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-330">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="20f86-331">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-331">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="20f86-332">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="20f86-332">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="20f86-333">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-333">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="20f86-334">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-334">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="20f86-335">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-335">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="20f86-336">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="20f86-336">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="20f86-337">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-337">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="20f86-338">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="20f86-338">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-339">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-339">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-340">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="20f86-340">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="20f86-341">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-341">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="20f86-342">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="20f86-342">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-343">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="20f86-343">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="20f86-344">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-344">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="20f86-345">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="20f86-345">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="20f86-346">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-346">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="20f86-347">public void undo()</span><span class="sxs-lookup"><span data-stu-id="20f86-347">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="20f86-348">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="20f86-348">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="20f86-349">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="20f86-349">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="20f86-350">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-350">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-351">public void context()</span><span class="sxs-lookup"><span data-stu-id="20f86-351">public void context()</span></span>                                                                                       | <span data-ttu-id="20f86-352">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-352">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="20f86-353">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="20f86-353">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="20f86-354">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-354">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="20f86-355">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-355">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-356">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="20f86-356">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="20f86-357">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-357">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="20f86-358">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="20f86-358">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="20f86-359">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="20f86-359">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="20f86-360">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="20f86-360">public void displayControl()</span></span>                                                                                | <span data-ttu-id="20f86-361">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-361">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="20f86-362">public void enter()</span><span class="sxs-lookup"><span data-stu-id="20f86-362">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="20f86-363">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="20f86-363">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="20f86-364">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="20f86-364">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="20f86-365">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="20f86-365">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="20f86-366">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-366">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="20f86-367">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="20f86-367">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="20f86-368">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-368">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="20f86-369">public void copy()</span><span class="sxs-lookup"><span data-stu-id="20f86-369">public void copy()</span></span>                                                                                          | <span data-ttu-id="20f86-370">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="20f86-370">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="20f86-371">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="20f86-371">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="20f86-372">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-372">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="20f86-373">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="20f86-373">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="20f86-374">public void cut()</span><span class="sxs-lookup"><span data-stu-id="20f86-374">public void cut()</span></span>                                                                                           | <span data-ttu-id="20f86-375">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="20f86-375">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="20f86-376">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-376">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-377">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="20f86-377">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="20f86-378">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-378">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="20f86-379">public void paste()</span><span class="sxs-lookup"><span data-stu-id="20f86-379">public void paste()</span></span>                                                                                         | <span data-ttu-id="20f86-380">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="20f86-380">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="20f86-381">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="20f86-381">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="20f86-382">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-382">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="20f86-383">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="20f86-383">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="20f86-384">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="20f86-384">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="20f86-385">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="20f86-385">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="20f86-386">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-386">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="20f86-387">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="20f86-387">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="20f86-388">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-388">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="20f86-389">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="20f86-389">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-390">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="20f86-390">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="20f86-391">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="20f86-391">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="20f86-392">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="20f86-392">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="20f86-393">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-393">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="20f86-394">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="20f86-394">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="20f86-395">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="20f86-395">Method alignControl</span></span>

<span data-ttu-id="20f86-396">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-396">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="20f86-397">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="20f86-397">Parameters - alignControl</span></span>

<span data-ttu-id="20f86-398">値</span><span class="sxs-lookup"><span data-stu-id="20f86-398">value</span></span>  
<span data-ttu-id="20f86-399">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-399">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="20f86-400">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="20f86-400">Return Value - alignControl</span></span>

<span data-ttu-id="20f86-401">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="20f86-401">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="20f86-402">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="20f86-402">Remarks - alignControl</span></span>

<span data-ttu-id="20f86-403">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-403">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="20f86-404">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="20f86-404">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="20f86-405">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="20f86-405">Parameters - alignment</span></span>

<span data-ttu-id="20f86-406">値</span><span class="sxs-lookup"><span data-stu-id="20f86-406">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="20f86-407">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="20f86-407">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="20f86-408">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="20f86-408">Method allowEdit</span></span>

<span data-ttu-id="20f86-409">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-409">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="20f86-410">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="20f86-410">Parameters - allowEdit</span></span>

<span data-ttu-id="20f86-411">値</span><span class="sxs-lookup"><span data-stu-id="20f86-411">value</span></span>  
<span data-ttu-id="20f86-412">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="20f86-412">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="20f86-413">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="20f86-413">Return Value - allowEdit</span></span>

<span data-ttu-id="20f86-414">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-414">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="20f86-415">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="20f86-415">Remarks - allowEdit</span></span>

<span data-ttu-id="20f86-416">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="20f86-416">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="20f86-417">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="20f86-417">Method allowSysSetup</span></span>

<span data-ttu-id="20f86-418">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-418">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="20f86-419">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="20f86-419">Return Value - allowSysSetup</span></span>

<span data-ttu-id="20f86-420">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-420">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="20f86-421">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-421">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="20f86-422">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-422">Parameters - arrayIndex</span></span>

<span data-ttu-id="20f86-423">値</span><span class="sxs-lookup"><span data-stu-id="20f86-423">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="20f86-424">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-424">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="20f86-425">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="20f86-425">Method autoDeclaration</span></span>

<span data-ttu-id="20f86-426">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-426">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="20f86-427">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="20f86-427">Parameters - autoDeclaration</span></span>

<span data-ttu-id="20f86-428">値</span><span class="sxs-lookup"><span data-stu-id="20f86-428">value</span></span>  
<span data-ttu-id="20f86-429">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-429">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="20f86-430">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="20f86-430">Return Value - autoDeclaration</span></span>

<span data-ttu-id="20f86-431">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-431">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="20f86-432">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="20f86-432">Remarks - autoDeclaration</span></span>

<span data-ttu-id="20f86-433">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="20f86-433">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="20f86-434">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-434">Method backgroundColor</span></span>

<span data-ttu-id="20f86-435">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-435">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="20f86-436">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-436">Parameters - backgroundColor</span></span>

<span data-ttu-id="20f86-437">値</span><span class="sxs-lookup"><span data-stu-id="20f86-437">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="20f86-438">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-438">Return Value - backgroundColor</span></span>

<span data-ttu-id="20f86-439">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="20f86-439">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="20f86-440">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-440">Remarks - backgroundColor</span></span>

<span data-ttu-id="20f86-441">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="20f86-441">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="20f86-442">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="20f86-442">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="20f86-443">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="20f86-443">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="20f86-444">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="20f86-444">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="20f86-445">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="20f86-445">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="20f86-446">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-446">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="20f86-447">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="20f86-447">Method backStyle</span></span>

<span data-ttu-id="20f86-448">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-448">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="20f86-449">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="20f86-449">Parameters - backStyle</span></span>

<span data-ttu-id="20f86-450">値</span><span class="sxs-lookup"><span data-stu-id="20f86-450">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="20f86-451">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="20f86-451">Return Value - backStyle</span></span>

<span data-ttu-id="20f86-452">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-452">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="20f86-453">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="20f86-453">Method beginDrag</span></span>

<span data-ttu-id="20f86-454">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-454">Is called when the user begins dragging a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="20f86-455">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="20f86-455">Parameters - beginDrag</span></span>

<span data-ttu-id="20f86-456">x</span><span class="sxs-lookup"><span data-stu-id="20f86-456">x</span></span>  
<span data-ttu-id="20f86-457">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-457">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="20f86-458">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="20f86-458">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="20f86-459">y</span><span class="sxs-lookup"><span data-stu-id="20f86-459">y</span></span>  
<span data-ttu-id="20f86-460">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-460">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="20f86-461">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="20f86-461">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="20f86-462">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="20f86-462">Return Value - beginDrag</span></span>

<span data-ttu-id="20f86-463">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="20f86-463">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="20f86-464">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="20f86-464">Remarks - beginDrag</span></span>

<span data-ttu-id="20f86-465">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="20f86-465">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="20f86-466">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="20f86-466">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="20f86-467">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="20f86-467">Method bold</span></span>

<span data-ttu-id="20f86-468">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-468">Gets or sets the weight of font that was used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="20f86-469">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="20f86-469">Parameters - bold</span></span>

<span data-ttu-id="20f86-470">値</span><span class="sxs-lookup"><span data-stu-id="20f86-470">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="20f86-471">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="20f86-471">Return Value - bold</span></span>

<span data-ttu-id="20f86-472">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-472">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="20f86-473">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="20f86-473">Remarks - bold</span></span>

<span data-ttu-id="20f86-474">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20f86-474">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="20f86-475">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="20f86-475">0 Use the default font weight.</span></span>
-   <span data-ttu-id="20f86-476">1 シン。</span><span class="sxs-lookup"><span data-stu-id="20f86-476">1 Thin.</span></span>
-   <span data-ttu-id="20f86-477">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="20f86-477">2 Extra-light.</span></span>
-   <span data-ttu-id="20f86-478">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="20f86-478">3 Light.</span></span>
-   <span data-ttu-id="20f86-479">4 標準。</span><span class="sxs-lookup"><span data-stu-id="20f86-479">4 Normal.</span></span>
-   <span data-ttu-id="20f86-480">5 中。</span><span class="sxs-lookup"><span data-stu-id="20f86-480">5 Medium.</span></span>
-   <span data-ttu-id="20f86-481">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="20f86-481">6 Semibold.</span></span>
-   <span data-ttu-id="20f86-482">7 太字。</span><span class="sxs-lookup"><span data-stu-id="20f86-482">7 Bold.</span></span>
-   <span data-ttu-id="20f86-483">8 極太。</span><span class="sxs-lookup"><span data-stu-id="20f86-483">8 Extra-bold.</span></span>
-   <span data-ttu-id="20f86-484">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="20f86-484">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="20f86-485">メソッド border</span><span class="sxs-lookup"><span data-stu-id="20f86-485">Method border</span></span>

<span data-ttu-id="20f86-486">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-486">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="20f86-487">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="20f86-487">Parameters - border</span></span>

<span data-ttu-id="20f86-488">値</span><span class="sxs-lookup"><span data-stu-id="20f86-488">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="20f86-489">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="20f86-489">Return Value - border</span></span>

<span data-ttu-id="20f86-490">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="20f86-490">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="20f86-491">備考 - border</span><span class="sxs-lookup"><span data-stu-id="20f86-491">Remarks - border</span></span>

<span data-ttu-id="20f86-492">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="20f86-492">The integer that is returned contains the style of the borderline of the control as follows.</span></span>

| <span data-ttu-id="20f86-493">先頭値</span><span class="sxs-lookup"><span data-stu-id="20f86-493">Value</span></span> | <span data-ttu-id="20f86-494">説明</span><span class="sxs-lookup"><span data-stu-id="20f86-494">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="20f86-495">0</span><span class="sxs-lookup"><span data-stu-id="20f86-495">0</span></span>     | <span data-ttu-id="20f86-496">自動</span><span class="sxs-lookup"><span data-stu-id="20f86-496">Auto</span></span>        |
| <span data-ttu-id="20f86-497">1</span><span class="sxs-lookup"><span data-stu-id="20f86-497">1</span></span>     | <span data-ttu-id="20f86-498">3D</span><span class="sxs-lookup"><span data-stu-id="20f86-498">3D</span></span>          |
| <span data-ttu-id="20f86-499">2</span><span class="sxs-lookup"><span data-stu-id="20f86-499">2</span></span>     | <span data-ttu-id="20f86-500">1 行</span><span class="sxs-lookup"><span data-stu-id="20f86-500">Single line</span></span> |
| <span data-ttu-id="20f86-501">3</span><span class="sxs-lookup"><span data-stu-id="20f86-501">3</span></span>     | <span data-ttu-id="20f86-502">集合住宅</span><span class="sxs-lookup"><span data-stu-id="20f86-502">Flat</span></span>        |
| <span data-ttu-id="20f86-503">4</span><span class="sxs-lookup"><span data-stu-id="20f86-503">4</span></span>     | <span data-ttu-id="20f86-504">None</span><span class="sxs-lookup"><span data-stu-id="20f86-504">None</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="20f86-505">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-505">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="20f86-506">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-506">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="20f86-507">値</span><span class="sxs-lookup"><span data-stu-id="20f86-507">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="20f86-508">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-508">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="20f86-509">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="20f86-509">Method calcControlSize</span></span>

<span data-ttu-id="20f86-510">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-510">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="20f86-511">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="20f86-511">Parameters - calcControlSize</span></span>

<span data-ttu-id="20f86-512">chars</span><span class="sxs-lookup"><span data-stu-id="20f86-512">chars</span></span>  
<span data-ttu-id="20f86-513">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="20f86-513">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="20f86-514">明細行</span><span class="sxs-lookup"><span data-stu-id="20f86-514">lines</span></span>  
<span data-ttu-id="20f86-515">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="20f86-515">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="20f86-516">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="20f86-516">Return Value - calcControlSize</span></span>

<span data-ttu-id="20f86-517">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="20f86-517">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="20f86-518">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="20f86-518">Method characterSet</span></span>

<span data-ttu-id="20f86-519">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-519">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="20f86-520">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="20f86-520">Parameters - characterSet</span></span>

<span data-ttu-id="20f86-521">値</span><span class="sxs-lookup"><span data-stu-id="20f86-521">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="20f86-522">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="20f86-522">Return Value - characterSet</span></span>

<span data-ttu-id="20f86-523">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-523">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="20f86-524">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="20f86-524">Remarks - characterSet</span></span>

<span data-ttu-id="20f86-525">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-525">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="20f86-526">先頭値</span><span class="sxs-lookup"><span data-stu-id="20f86-526">Value</span></span> | <span data-ttu-id="20f86-527">説明</span><span class="sxs-lookup"><span data-stu-id="20f86-527">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="20f86-528">0</span><span class="sxs-lookup"><span data-stu-id="20f86-528">0</span></span>     | <span data-ttu-id="20f86-529">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-529">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="20f86-530">1</span><span class="sxs-lookup"><span data-stu-id="20f86-530">1</span></span>     | <span data-ttu-id="20f86-531">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-531">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="20f86-532">2</span><span class="sxs-lookup"><span data-stu-id="20f86-532">2</span></span>     | <span data-ttu-id="20f86-533">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-533">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="20f86-534">77</span><span class="sxs-lookup"><span data-stu-id="20f86-534">77</span></span>    | <span data-ttu-id="20f86-535">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-535">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="20f86-536">128</span><span class="sxs-lookup"><span data-stu-id="20f86-536">128</span></span>   | <span data-ttu-id="20f86-537">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-537">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="20f86-538">129</span><span class="sxs-lookup"><span data-stu-id="20f86-538">129</span></span>   | <span data-ttu-id="20f86-539">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-539">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="20f86-540">134</span><span class="sxs-lookup"><span data-stu-id="20f86-540">134</span></span>   | <span data-ttu-id="20f86-541">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-541">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="20f86-542">136</span><span class="sxs-lookup"><span data-stu-id="20f86-542">136</span></span>   | <span data-ttu-id="20f86-543">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-543">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="20f86-544">161</span><span class="sxs-lookup"><span data-stu-id="20f86-544">161</span></span>   | <span data-ttu-id="20f86-545">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-545">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="20f86-546">162</span><span class="sxs-lookup"><span data-stu-id="20f86-546">162</span></span>   | <span data-ttu-id="20f86-547">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-547">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="20f86-548">163</span><span class="sxs-lookup"><span data-stu-id="20f86-548">163</span></span>   | <span data-ttu-id="20f86-549">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-549">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="20f86-550">186</span><span class="sxs-lookup"><span data-stu-id="20f86-550">186</span></span>   | <span data-ttu-id="20f86-551">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-551">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="20f86-552">204</span><span class="sxs-lookup"><span data-stu-id="20f86-552">204</span></span>   | <span data-ttu-id="20f86-553">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-553">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="20f86-554">238</span><span class="sxs-lookup"><span data-stu-id="20f86-554">238</span></span>   | <span data-ttu-id="20f86-555">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-555">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="20f86-556">255</span><span class="sxs-lookup"><span data-stu-id="20f86-556">255</span></span>   | <span data-ttu-id="20f86-557">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-557">OEM\_CHARSET</span></span>         |

<span data-ttu-id="20f86-558">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="20f86-558">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="20f86-559">金額</span><span class="sxs-lookup"><span data-stu-id="20f86-559">Value</span></span> | <span data-ttu-id="20f86-560">説明</span><span class="sxs-lookup"><span data-stu-id="20f86-560">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="20f86-561">130</span><span class="sxs-lookup"><span data-stu-id="20f86-561">130</span></span>   | <span data-ttu-id="20f86-562">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-562">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="20f86-563">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="20f86-563">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="20f86-564">先頭値</span><span class="sxs-lookup"><span data-stu-id="20f86-564">Value</span></span> | <span data-ttu-id="20f86-565">説明</span><span class="sxs-lookup"><span data-stu-id="20f86-565">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="20f86-566">177</span><span class="sxs-lookup"><span data-stu-id="20f86-566">177</span></span>   | <span data-ttu-id="20f86-567">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-567">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="20f86-568">178</span><span class="sxs-lookup"><span data-stu-id="20f86-568">178</span></span>   | <span data-ttu-id="20f86-569">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-569">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="20f86-570">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="20f86-570">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="20f86-571">先頭値</span><span class="sxs-lookup"><span data-stu-id="20f86-571">Value</span></span> | <span data-ttu-id="20f86-572">説明</span><span class="sxs-lookup"><span data-stu-id="20f86-572">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="20f86-573">222</span><span class="sxs-lookup"><span data-stu-id="20f86-573">222</span></span>   | <span data-ttu-id="20f86-574">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="20f86-574">THAI\_CHARSET</span></span> |

<span data-ttu-id="20f86-575">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-575">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="20f86-576">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-576">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="20f86-577">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20f86-577">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-charfrompos"></a><span data-ttu-id="20f86-578">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="20f86-578">Method charFromPos</span></span>

```xpp
public int charFromPos(int x, int y)
```

### <a name="parameters---charfrompos"></a><span data-ttu-id="20f86-579">パラメーター - charFromPos</span><span class="sxs-lookup"><span data-stu-id="20f86-579">Parameters - charFromPos</span></span>

<span data-ttu-id="20f86-580">x</span><span class="sxs-lookup"><span data-stu-id="20f86-580">x</span></span>  

<!-- -->

<span data-ttu-id="20f86-581">y</span><span class="sxs-lookup"><span data-stu-id="20f86-581">y</span></span>  

### <a name="return-value---charfrompos"></a><span data-ttu-id="20f86-582">戻り値 - charFromPos</span><span class="sxs-lookup"><span data-stu-id="20f86-582">Return Value - charFromPos</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="20f86-583">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="20f86-583">Method colorScheme</span></span>

<span data-ttu-id="20f86-584">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-584">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="20f86-585">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="20f86-585">Parameters - colorScheme</span></span>

<span data-ttu-id="20f86-586">値</span><span class="sxs-lookup"><span data-stu-id="20f86-586">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="20f86-587">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="20f86-587">Return Value - colorScheme</span></span>

<span data-ttu-id="20f86-588">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="20f86-588">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="20f86-589">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="20f86-589">Remarks - colorScheme</span></span>

<span data-ttu-id="20f86-590">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-590">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="20f86-591">先頭値</span><span class="sxs-lookup"><span data-stu-id="20f86-591">Value</span></span> | <span data-ttu-id="20f86-592">スタイル</span><span class="sxs-lookup"><span data-stu-id="20f86-592">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="20f86-593">0</span><span class="sxs-lookup"><span data-stu-id="20f86-593">0</span></span>     | <span data-ttu-id="20f86-594">既定</span><span class="sxs-lookup"><span data-stu-id="20f86-594">Default</span></span>               |
| <span data-ttu-id="20f86-595">1</span><span class="sxs-lookup"><span data-stu-id="20f86-595">1</span></span>     | <span data-ttu-id="20f86-596">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="20f86-596">The Windows palette</span></span>   |
| <span data-ttu-id="20f86-597">2</span><span class="sxs-lookup"><span data-stu-id="20f86-597">2</span></span>     | <span data-ttu-id="20f86-598">真の配色</span><span class="sxs-lookup"><span data-stu-id="20f86-598">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="20f86-599">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="20f86-599">Method configurationKey</span></span>

<span data-ttu-id="20f86-600">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-600">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="20f86-601">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="20f86-601">Parameters - configurationKey</span></span>

<span data-ttu-id="20f86-602">値</span><span class="sxs-lookup"><span data-stu-id="20f86-602">value</span></span>  
<span data-ttu-id="20f86-603">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-603">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="20f86-604">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="20f86-604">Return Value - configurationKey</span></span>

<span data-ttu-id="20f86-605">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="20f86-605">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="20f86-606">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="20f86-606">Remarks - configurationKey</span></span>

<span data-ttu-id="20f86-607">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-607">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="20f86-608">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="20f86-608">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="20f86-609">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="20f86-609">Method configurationKeyEx</span></span>

<span data-ttu-id="20f86-610">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-610">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="20f86-611">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="20f86-611">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="20f86-612">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="20f86-612">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="20f86-613">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="20f86-613">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="20f86-614">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="20f86-614">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="20f86-615">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="20f86-615">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="20f86-616">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20f86-616">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="20f86-617">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="20f86-617">Method countryRegionCodes</span></span>

<span data-ttu-id="20f86-618">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-618">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="20f86-619">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="20f86-619">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="20f86-620">値</span><span class="sxs-lookup"><span data-stu-id="20f86-620">value</span></span>  
<span data-ttu-id="20f86-621">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-621">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="20f86-622">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="20f86-622">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="20f86-623">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="20f86-623">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="20f86-624">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="20f86-624">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="20f86-625">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="20f86-625">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="20f86-626">値</span><span class="sxs-lookup"><span data-stu-id="20f86-626">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="20f86-627">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="20f86-627">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="20f86-628">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="20f86-628">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="20f86-629">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="20f86-629">Parameters - dataField</span></span>

<span data-ttu-id="20f86-630">値</span><span class="sxs-lookup"><span data-stu-id="20f86-630">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="20f86-631">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="20f86-631">Return Value - dataField</span></span>

## <a name="method-datafieldarrayindex"></a><span data-ttu-id="20f86-632">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-632">Method dataFieldArrayIndex</span></span>

```xpp
public int dataFieldArrayIndex()
```

### <a name="return-value---datafieldarrayindex"></a><span data-ttu-id="20f86-633">戻り値 - dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-633">Return Value - dataFieldArrayIndex</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="20f86-634">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="20f86-634">Method dataFieldName</span></span>

```xpp
public FieldName dataFieldName()
```

### <a name="return-value---datafieldname"></a><span data-ttu-id="20f86-635">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="20f86-635">Return Value - dataFieldName</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="20f86-636">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-636">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="20f86-637">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-637">Parameters - dataMethod</span></span>

<span data-ttu-id="20f86-638">値</span><span class="sxs-lookup"><span data-stu-id="20f86-638">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="20f86-639">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-639">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="20f86-640">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="20f86-640">Method dataRelationPath</span></span>

<span data-ttu-id="20f86-641">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-641">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="20f86-642">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="20f86-642">Parameters - dataRelationPath</span></span>

<span data-ttu-id="20f86-643">値</span><span class="sxs-lookup"><span data-stu-id="20f86-643">value</span></span>  
<span data-ttu-id="20f86-644">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-644">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="20f86-645">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="20f86-645">Return Value - dataRelationPath</span></span>

<span data-ttu-id="20f86-646">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="20f86-646">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="20f86-647">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="20f86-647">Remarks - dataRelationPath</span></span>

<span data-ttu-id="20f86-648">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="20f86-648">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="20f86-649">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="20f86-649">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="20f86-650">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="20f86-650">Method dataSource</span></span>

<span data-ttu-id="20f86-651">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-651">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="20f86-652">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="20f86-652">Parameters - dataSource</span></span>

<span data-ttu-id="20f86-653">値</span><span class="sxs-lookup"><span data-stu-id="20f86-653">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="20f86-654">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="20f86-654">Return Value - dataSource</span></span>

<span data-ttu-id="20f86-655">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="20f86-655">The identifier of the data source that will be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="20f86-656">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="20f86-656">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="20f86-657">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="20f86-657">Parameters - direction</span></span>

<span data-ttu-id="20f86-658">値</span><span class="sxs-lookup"><span data-stu-id="20f86-658">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="20f86-659">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="20f86-659">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="20f86-660">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-660">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="20f86-661">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-661">Parameters - displayHeight</span></span>

<span data-ttu-id="20f86-662">値</span><span class="sxs-lookup"><span data-stu-id="20f86-662">value</span></span>  

<!-- -->

<span data-ttu-id="20f86-663">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-663">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="20f86-664">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-664">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="20f86-665">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-665">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="20f86-666">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-666">Parameters - displayHeightMode</span></span>

<span data-ttu-id="20f86-667">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-667">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="20f86-668">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-668">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="20f86-669">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-669">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="20f86-670">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-670">Parameters - displayHeightValue</span></span>

<span data-ttu-id="20f86-671">値</span><span class="sxs-lookup"><span data-stu-id="20f86-671">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="20f86-672">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-672">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="20f86-673">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="20f86-673">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="20f86-674">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="20f86-674">Parameters - displayLength</span></span>

<span data-ttu-id="20f86-675">値</span><span class="sxs-lookup"><span data-stu-id="20f86-675">value</span></span>  

<!-- -->

<span data-ttu-id="20f86-676">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-676">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="20f86-677">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="20f86-677">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="20f86-678">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-678">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="20f86-679">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-679">Parameters - displayLengthMode</span></span>

<span data-ttu-id="20f86-680">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-680">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="20f86-681">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-681">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="20f86-682">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-682">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="20f86-683">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-683">Parameters - displayLengthValue</span></span>

<span data-ttu-id="20f86-684">値</span><span class="sxs-lookup"><span data-stu-id="20f86-684">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="20f86-685">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-685">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="20f86-686">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="20f86-686">Method displayTarget</span></span>

<span data-ttu-id="20f86-687">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-687">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="20f86-688">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="20f86-688">Parameters - displayTarget</span></span>

<span data-ttu-id="20f86-689">値</span><span class="sxs-lookup"><span data-stu-id="20f86-689">value</span></span>  
<span data-ttu-id="20f86-690">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-690">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="20f86-691">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="20f86-691">Return Value - displayTarget</span></span>

<span data-ttu-id="20f86-692">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="20f86-692">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="20f86-693">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="20f86-693">Method dragDrop</span></span>

<span data-ttu-id="20f86-694">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-694">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="20f86-695">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="20f86-695">Parameters - dragDrop</span></span>

<span data-ttu-id="20f86-696">値</span><span class="sxs-lookup"><span data-stu-id="20f86-696">value</span></span>  
<span data-ttu-id="20f86-697">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-697">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="20f86-698">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="20f86-698">Return Value - dragDrop</span></span>

<span data-ttu-id="20f86-699">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-699">1 if drag-and-drop operations are enabled; otherwise, 0.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="20f86-700">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="20f86-700">Remarks - dragDrop</span></span>

<span data-ttu-id="20f86-701">dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-701">Use the dragLeave Method, the dragOver Method, and the dragOverEx Method to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="20f86-702">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="20f86-702">Method dragOver</span></span>

<span data-ttu-id="20f86-703">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-703">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="20f86-704">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="20f86-704">Parameters - dragOver</span></span>

<span data-ttu-id="20f86-705">dragSource</span><span class="sxs-lookup"><span data-stu-id="20f86-705">dragSource</span></span>  
<span data-ttu-id="20f86-706">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-706">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-707">dragMode</span><span class="sxs-lookup"><span data-stu-id="20f86-707">dragMode</span></span>  
<span data-ttu-id="20f86-708">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-708">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-709">x</span><span class="sxs-lookup"><span data-stu-id="20f86-709">x</span></span>  
<span data-ttu-id="20f86-710">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-710">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-711">y</span><span class="sxs-lookup"><span data-stu-id="20f86-711">y</span></span>  
<span data-ttu-id="20f86-712">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-712">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="20f86-713">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="20f86-713">Return Value - dragOver</span></span>

<span data-ttu-id="20f86-714">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="20f86-714">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="20f86-715">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="20f86-715">Method dragOverEx</span></span>

<span data-ttu-id="20f86-716">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-716">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="20f86-717">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="20f86-717">Parameters - dragOverEx</span></span>

<span data-ttu-id="20f86-718">dragSource</span><span class="sxs-lookup"><span data-stu-id="20f86-718">dragSource</span></span>  
<span data-ttu-id="20f86-719">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-719">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-720">dragMode</span><span class="sxs-lookup"><span data-stu-id="20f86-720">dragMode</span></span>  
<span data-ttu-id="20f86-721">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-721">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-722">x</span><span class="sxs-lookup"><span data-stu-id="20f86-722">x</span></span>  
<span data-ttu-id="20f86-723">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-723">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-724">y</span><span class="sxs-lookup"><span data-stu-id="20f86-724">y</span></span>  
<span data-ttu-id="20f86-725">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-725">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="20f86-726">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="20f86-726">Return Value - dragOverEx</span></span>

<span data-ttu-id="20f86-727">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="20f86-727">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="20f86-728">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="20f86-728">Method dragText</span></span>

<span data-ttu-id="20f86-729">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-729">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="20f86-730">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="20f86-730">Return Value - dragText</span></span>

<span data-ttu-id="20f86-731">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="20f86-731">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="20f86-732">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="20f86-732">Method enabled</span></span>

<span data-ttu-id="20f86-733">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-733">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="20f86-734">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="20f86-734">Parameters - enabled</span></span>

<span data-ttu-id="20f86-735">値</span><span class="sxs-lookup"><span data-stu-id="20f86-735">value</span></span>  
<span data-ttu-id="20f86-736">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-736">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="20f86-737">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="20f86-737">Return Value - enabled</span></span>

<span data-ttu-id="20f86-738">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-738">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="20f86-739">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="20f86-739">Remarks - enabled</span></span>

<span data-ttu-id="20f86-740">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="20f86-740">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="20f86-741">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="20f86-741">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="20f86-742">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="20f86-742">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="20f86-743">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="20f86-743">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="20f86-744">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="20f86-744">Parameters - extendedDataType</span></span>

<span data-ttu-id="20f86-745">値</span><span class="sxs-lookup"><span data-stu-id="20f86-745">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="20f86-746">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="20f86-746">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="20f86-747">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="20f86-747">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="20f86-748">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="20f86-748">Parameters - fastTabSummary</span></span>

<span data-ttu-id="20f86-749">値</span><span class="sxs-lookup"><span data-stu-id="20f86-749">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="20f86-750">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="20f86-750">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="20f86-751">メソッド font</span><span class="sxs-lookup"><span data-stu-id="20f86-751">Method font</span></span>

<span data-ttu-id="20f86-752">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-752">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="20f86-753">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="20f86-753">Parameters - font</span></span>

<span data-ttu-id="20f86-754">値</span><span class="sxs-lookup"><span data-stu-id="20f86-754">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="20f86-755">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="20f86-755">Return Value - font</span></span>

<span data-ttu-id="20f86-756">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="20f86-756">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="20f86-757">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="20f86-757">Method fontSize</span></span>

<span data-ttu-id="20f86-758">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-758">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="20f86-759">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="20f86-759">Parameters - fontSize</span></span>

<span data-ttu-id="20f86-760">値</span><span class="sxs-lookup"><span data-stu-id="20f86-760">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="20f86-761">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="20f86-761">Return Value - fontSize</span></span>

<span data-ttu-id="20f86-762">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="20f86-762">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="20f86-763">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-763">Method foregroundColor</span></span>

<span data-ttu-id="20f86-764">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-764">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="20f86-765">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-765">Parameters - foregroundColor</span></span>

<span data-ttu-id="20f86-766">値</span><span class="sxs-lookup"><span data-stu-id="20f86-766">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="20f86-767">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-767">Return Value - foregroundColor</span></span>

<span data-ttu-id="20f86-768">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="20f86-768">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="20f86-769">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-769">Remarks - foregroundColor</span></span>

<span data-ttu-id="20f86-770">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="20f86-770">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="20f86-771">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="20f86-771">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="20f86-772">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="20f86-772">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="20f86-773">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="20f86-773">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="20f86-774">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="20f86-774">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="20f86-775">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-775">The maximum value for a single byte is 255.</span></span>

## <a name="method-getcursorpos"></a><span data-ttu-id="20f86-776">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="20f86-776">Method getCursorPos</span></span>

```xpp
public container getCursorPos()
```

### <a name="return-value---getcursorpos"></a><span data-ttu-id="20f86-777">戻り値 - getCursorPos</span><span class="sxs-lookup"><span data-stu-id="20f86-777">Return Value - getCursorPos</span></span>

## <a name="method-getfirstvisibleline"></a><span data-ttu-id="20f86-778">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="20f86-778">Method getFirstVisibleLine</span></span>

```xpp
public int getFirstVisibleLine()
```

### <a name="return-value---getfirstvisibleline"></a><span data-ttu-id="20f86-779">戻り値 - getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="20f86-779">Return Value - getFirstVisibleLine</span></span>

## <a name="method-getline"></a><span data-ttu-id="20f86-780">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="20f86-780">Method getLine</span></span>

```xpp
public str getLine(int lineNo)
```

### <a name="parameters---getline"></a><span data-ttu-id="20f86-781">パラメーター - getLine</span><span class="sxs-lookup"><span data-stu-id="20f86-781">Parameters - getLine</span></span>

<span data-ttu-id="20f86-782">lineNo</span><span class="sxs-lookup"><span data-stu-id="20f86-782">lineNo</span></span>  

### <a name="return-value---getline"></a><span data-ttu-id="20f86-783">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="20f86-783">Return Value - getLine</span></span>

## <a name="method-getlinecount"></a><span data-ttu-id="20f86-784">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="20f86-784">Method getLineCount</span></span>

```xpp
public int getLineCount()
```

### <a name="return-value---getlinecount"></a><span data-ttu-id="20f86-785">戻り値 - getLineCount</span><span class="sxs-lookup"><span data-stu-id="20f86-785">Return Value - getLineCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="20f86-786">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="20f86-786">Method getSelection</span></span>

```xpp
public container getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="20f86-787">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="20f86-787">Return Value - getSelection</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="20f86-788">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="20f86-788">Method hasChanged</span></span>

<span data-ttu-id="20f86-789">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-789">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="20f86-790">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="20f86-790">Parameters - hasChanged</span></span>

<span data-ttu-id="20f86-791">val</span><span class="sxs-lookup"><span data-stu-id="20f86-791">val</span></span>  
<span data-ttu-id="20f86-792">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-792">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="20f86-793">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="20f86-793">Return Value - hasChanged</span></span>

<span data-ttu-id="20f86-794">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-794">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="20f86-795">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="20f86-795">Method hasUserSetting</span></span>

<span data-ttu-id="20f86-796">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-796">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="20f86-797">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="20f86-797">Return Value - hasUserSetting</span></span>

<span data-ttu-id="20f86-798">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-798">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="20f86-799">メソッド height</span><span class="sxs-lookup"><span data-stu-id="20f86-799">Method height</span></span>

<span data-ttu-id="20f86-800">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-800">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="20f86-801">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="20f86-801">Parameters - height</span></span>

<span data-ttu-id="20f86-802">値</span><span class="sxs-lookup"><span data-stu-id="20f86-802">value</span></span>  
<span data-ttu-id="20f86-803">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-803">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="20f86-804">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-804">mode</span></span>  
<span data-ttu-id="20f86-805">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-805">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="20f86-806">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="20f86-806">Return Value - height</span></span>

<span data-ttu-id="20f86-807">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="20f86-807">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="20f86-808">備考 - height</span><span class="sxs-lookup"><span data-stu-id="20f86-808">Remarks - height</span></span>

<span data-ttu-id="20f86-809">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-809">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="20f86-810">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="20f86-810">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="20f86-811">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-811">Mode</span></span>            | <span data-ttu-id="20f86-812">高さの計算</span><span class="sxs-lookup"><span data-stu-id="20f86-812">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f86-813">-1 正確</span><span class="sxs-lookup"><span data-stu-id="20f86-813">-1 Exact</span></span>        | <span data-ttu-id="20f86-814">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-814">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="20f86-815">0 自動</span><span class="sxs-lookup"><span data-stu-id="20f86-815">0 Auto</span></span>          | <span data-ttu-id="20f86-816">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-816">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="20f86-817">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="20f86-817">1 Column height</span></span> | <span data-ttu-id="20f86-818">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="20f86-818">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="20f86-819">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="20f86-819">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="20f86-820">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-820">Method heightMode</span></span>

<span data-ttu-id="20f86-821">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-821">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="20f86-822">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-822">Parameters - heightMode</span></span>

<span data-ttu-id="20f86-823">値</span><span class="sxs-lookup"><span data-stu-id="20f86-823">value</span></span>  
<span data-ttu-id="20f86-824">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-824">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="20f86-825">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-825">Return Value - heightMode</span></span>

<span data-ttu-id="20f86-826">計算モード。</span><span class="sxs-lookup"><span data-stu-id="20f86-826">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="20f86-827">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-827">Remarks - heightMode</span></span>

<span data-ttu-id="20f86-828">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="20f86-828">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="20f86-829">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-829">Mode</span></span>          | <span data-ttu-id="20f86-830">高さの計算</span><span class="sxs-lookup"><span data-stu-id="20f86-830">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f86-831">正確</span><span class="sxs-lookup"><span data-stu-id="20f86-831">Exact</span></span>         | <span data-ttu-id="20f86-832">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-832">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="20f86-833">自動</span><span class="sxs-lookup"><span data-stu-id="20f86-833">Auto</span></span>          | <span data-ttu-id="20f86-834">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-834">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="20f86-835">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="20f86-835">Column height</span></span> | <span data-ttu-id="20f86-836">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="20f86-836">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="20f86-837">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="20f86-837">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="20f86-838">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-838">Method heightValue</span></span>

<span data-ttu-id="20f86-839">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-839">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="20f86-840">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-840">Parameters - heightValue</span></span>

<span data-ttu-id="20f86-841">値</span><span class="sxs-lookup"><span data-stu-id="20f86-841">value</span></span>  
<span data-ttu-id="20f86-842">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-842">An integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="20f86-843">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-843">Return Value - heightValue</span></span>

<span data-ttu-id="20f86-844">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="20f86-844">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="20f86-845">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-845">Remarks - heightValue</span></span>

<span data-ttu-id="20f86-846">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="20f86-846">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="20f86-847">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="20f86-847">Method helpField</span></span>

<span data-ttu-id="20f86-848">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-848">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="20f86-849">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="20f86-849">Return Value - helpField</span></span>

<span data-ttu-id="20f86-850">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="20f86-850">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="20f86-851">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="20f86-851">Remarks - helpField</span></span>

<span data-ttu-id="20f86-852">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="20f86-852">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="20f86-853">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="20f86-853">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="20f86-854">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="20f86-854">Method helpText</span></span>

<span data-ttu-id="20f86-855">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-855">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="20f86-856">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="20f86-856">Parameters - helpText</span></span>

<span data-ttu-id="20f86-857">値</span><span class="sxs-lookup"><span data-stu-id="20f86-857">value</span></span>  
<span data-ttu-id="20f86-858">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="20f86-858">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="20f86-859">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="20f86-859">Return Value - helpText</span></span>

<span data-ttu-id="20f86-860">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="20f86-860">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="20f86-861">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="20f86-861">Remarks - helpText</span></span>

<span data-ttu-id="20f86-862">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-862">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="20f86-863">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="20f86-863">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="20f86-864">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="20f86-864">Method hierarchyParent</span></span>

<span data-ttu-id="20f86-865">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-865">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="20f86-866">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="20f86-866">Parameters - hierarchyParent</span></span>

<span data-ttu-id="20f86-867">値</span><span class="sxs-lookup"><span data-stu-id="20f86-867">value</span></span>  
<span data-ttu-id="20f86-868">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="20f86-868">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="20f86-869">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="20f86-869">Return Value - hierarchyParent</span></span>

<span data-ttu-id="20f86-870">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="20f86-870">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="20f86-871">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="20f86-871">Method hWnd</span></span>

<span data-ttu-id="20f86-872">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-872">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="20f86-873">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="20f86-873">Return Value - hWnd</span></span>

<span data-ttu-id="20f86-874">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="20f86-874">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="20f86-875">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="20f86-875">Remarks - hWnd</span></span>

<span data-ttu-id="20f86-876">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="20f86-876">The handle can be used with the Windows API.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="20f86-877">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="20f86-877">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="20f86-878">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="20f86-878">Parameters - iMEMode</span></span>

<span data-ttu-id="20f86-879">値</span><span class="sxs-lookup"><span data-stu-id="20f86-879">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="20f86-880">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="20f86-880">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="20f86-881">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="20f86-881">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="20f86-882">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="20f86-882">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="20f86-883">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="20f86-883">Method isDisplayed</span></span>

<span data-ttu-id="20f86-884">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-884">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="20f86-885">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="20f86-885">Return Value - isDisplayed</span></span>

<span data-ttu-id="20f86-886">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="20f86-886">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="20f86-887">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="20f86-887">Remarks - isDisplayed</span></span>

<span data-ttu-id="20f86-888">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20f86-888">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="20f86-889">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="20f86-889">Method isRestricted</span></span>

<span data-ttu-id="20f86-890">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-890">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="20f86-891">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="20f86-891">Return Value - isRestricted</span></span>

<span data-ttu-id="20f86-892">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="20f86-892">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="20f86-893">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="20f86-893">Method isUserSetupEnabled</span></span>

<span data-ttu-id="20f86-894">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-894">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="20f86-895">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="20f86-895">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="20f86-896">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="20f86-896">neededSetupRights</span></span>  
<span data-ttu-id="20f86-897">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="20f86-897">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="20f86-898">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="20f86-898">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="20f86-899">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-899">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="20f86-900">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="20f86-900">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="20f86-901">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="20f86-901">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f86-902">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="20f86-902">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="20f86-903">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="20f86-903">No changes can be made to the control.</span></span> <span data-ttu-id="20f86-904">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-904">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="20f86-905">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="20f86-905">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="20f86-906">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="20f86-906">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="20f86-907">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="20f86-907">The user cannot move the control.</span></span>   |
| <span data-ttu-id="20f86-908">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="20f86-908">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="20f86-909">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="20f86-909">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="20f86-910">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="20f86-910">The user can also move the control.</span></span> |

<span data-ttu-id="20f86-911">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="20f86-911">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="20f86-912">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="20f86-912">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="20f86-913">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="20f86-913">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="20f86-914">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="20f86-914">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="20f86-915">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="20f86-915">Parameters - italic</span></span>

<span data-ttu-id="20f86-916">値</span><span class="sxs-lookup"><span data-stu-id="20f86-916">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="20f86-917">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="20f86-917">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="20f86-918">メソッド label</span><span class="sxs-lookup"><span data-stu-id="20f86-918">Method label</span></span>

<span data-ttu-id="20f86-919">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-919">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="20f86-920">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="20f86-920">Parameters - label</span></span>

<span data-ttu-id="20f86-921">値</span><span class="sxs-lookup"><span data-stu-id="20f86-921">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="20f86-922">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="20f86-922">Return Value - label</span></span>

<span data-ttu-id="20f86-923">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="20f86-923">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="20f86-924">備考 - label</span><span class="sxs-lookup"><span data-stu-id="20f86-924">Remarks - label</span></span>

<span data-ttu-id="20f86-925">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-925">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="20f86-926">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="20f86-926">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="20f86-927">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="20f86-927">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="20f86-928">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="20f86-928">Parameters - labelAlignment</span></span>

<span data-ttu-id="20f86-929">値</span><span class="sxs-lookup"><span data-stu-id="20f86-929">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="20f86-930">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="20f86-930">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="20f86-931">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="20f86-931">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="20f86-932">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="20f86-932">Parameters - labelBold</span></span>

<span data-ttu-id="20f86-933">値</span><span class="sxs-lookup"><span data-stu-id="20f86-933">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="20f86-934">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="20f86-934">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="20f86-935">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="20f86-935">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="20f86-936">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="20f86-936">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="20f86-937">値</span><span class="sxs-lookup"><span data-stu-id="20f86-937">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="20f86-938">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="20f86-938">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="20f86-939">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="20f86-939">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="20f86-940">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="20f86-940">Parameters - labelFont</span></span>

<span data-ttu-id="20f86-941">値</span><span class="sxs-lookup"><span data-stu-id="20f86-941">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="20f86-942">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="20f86-942">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="20f86-943">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="20f86-943">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="20f86-944">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="20f86-944">Parameters - labelFontSize</span></span>

<span data-ttu-id="20f86-945">値</span><span class="sxs-lookup"><span data-stu-id="20f86-945">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="20f86-946">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="20f86-946">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="20f86-947">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-947">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="20f86-948">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-948">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="20f86-949">値</span><span class="sxs-lookup"><span data-stu-id="20f86-949">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="20f86-950">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="20f86-950">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="20f86-951">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="20f86-951">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="20f86-952">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="20f86-952">Parameters - labelGuide</span></span>

<span data-ttu-id="20f86-953">値</span><span class="sxs-lookup"><span data-stu-id="20f86-953">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="20f86-954">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="20f86-954">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="20f86-955">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-955">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="20f86-956">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-956">Parameters - labelHeight</span></span>

<span data-ttu-id="20f86-957">値</span><span class="sxs-lookup"><span data-stu-id="20f86-957">value</span></span>  

<!-- -->

<span data-ttu-id="20f86-958">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-958">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="20f86-959">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-959">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="20f86-960">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-960">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="20f86-961">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-961">Parameters - labelHeightMode</span></span>

<span data-ttu-id="20f86-962">値</span><span class="sxs-lookup"><span data-stu-id="20f86-962">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="20f86-963">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="20f86-963">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="20f86-964">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-964">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="20f86-965">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-965">Parameters - labelHeightValue</span></span>

<span data-ttu-id="20f86-966">値</span><span class="sxs-lookup"><span data-stu-id="20f86-966">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="20f86-967">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="20f86-967">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="20f86-968">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="20f86-968">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="20f86-969">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="20f86-969">Parameters - labelItalic</span></span>

<span data-ttu-id="20f86-970">値</span><span class="sxs-lookup"><span data-stu-id="20f86-970">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="20f86-971">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="20f86-971">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="20f86-972">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="20f86-972">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="20f86-973">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="20f86-973">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="20f86-974">x</span><span class="sxs-lookup"><span data-stu-id="20f86-974">x</span></span>  

<!-- -->

<span data-ttu-id="20f86-975">y</span><span class="sxs-lookup"><span data-stu-id="20f86-975">y</span></span>  

<!-- -->

<span data-ttu-id="20f86-976">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-976">button</span></span>  

<!-- -->

<span data-ttu-id="20f86-977">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-977">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="20f86-978">Shift</span><span class="sxs-lookup"><span data-stu-id="20f86-978">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="20f86-979">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="20f86-979">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="20f86-980">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="20f86-980">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="20f86-981">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="20f86-981">Parameters - labelMouseDown</span></span>

<span data-ttu-id="20f86-982">x</span><span class="sxs-lookup"><span data-stu-id="20f86-982">x</span></span>  

<!-- -->

<span data-ttu-id="20f86-983">y</span><span class="sxs-lookup"><span data-stu-id="20f86-983">y</span></span>  

<!-- -->

<span data-ttu-id="20f86-984">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-984">button</span></span>  

<!-- -->

<span data-ttu-id="20f86-985">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-985">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="20f86-986">Shift</span><span class="sxs-lookup"><span data-stu-id="20f86-986">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="20f86-987">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="20f86-987">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="20f86-988">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="20f86-988">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="20f86-989">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="20f86-989">Parameters - labelMouseUp</span></span>

<span data-ttu-id="20f86-990">x</span><span class="sxs-lookup"><span data-stu-id="20f86-990">x</span></span>  

<!-- -->

<span data-ttu-id="20f86-991">y</span><span class="sxs-lookup"><span data-stu-id="20f86-991">y</span></span>  

<!-- -->

<span data-ttu-id="20f86-992">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-992">button</span></span>  

<!-- -->

<span data-ttu-id="20f86-993">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-993">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="20f86-994">Shift</span><span class="sxs-lookup"><span data-stu-id="20f86-994">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="20f86-995">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="20f86-995">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="20f86-996">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="20f86-996">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="20f86-997">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="20f86-997">Parameters - labelPosition</span></span>

<span data-ttu-id="20f86-998">値</span><span class="sxs-lookup"><span data-stu-id="20f86-998">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="20f86-999">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="20f86-999">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="20f86-1000">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="20f86-1000">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="20f86-1001">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="20f86-1001">Parameters - labelUnderline</span></span>

<span data-ttu-id="20f86-1002">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1002">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="20f86-1003">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="20f86-1003">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="20f86-1004">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="20f86-1004">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="20f86-1005">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="20f86-1005">Parameters - labelWidth</span></span>

<span data-ttu-id="20f86-1006">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1006">value</span></span>  

<!-- -->

<span data-ttu-id="20f86-1007">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1007">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="20f86-1008">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="20f86-1008">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="20f86-1009">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1009">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="20f86-1010">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1010">Parameters - labelWidthMode</span></span>

<span data-ttu-id="20f86-1011">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1011">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="20f86-1012">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1012">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="20f86-1013">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1013">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="20f86-1014">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1014">Parameters - labelWidthValue</span></span>

<span data-ttu-id="20f86-1015">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1015">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="20f86-1016">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1016">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="20f86-1017">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="20f86-1017">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="20f86-1018">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="20f86-1018">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="20f86-1019">メソッド left</span><span class="sxs-lookup"><span data-stu-id="20f86-1019">Method left</span></span>

<span data-ttu-id="20f86-1020">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1020">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="20f86-1021">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="20f86-1021">Parameters - left</span></span>

<span data-ttu-id="20f86-1022">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1022">value</span></span>  
<span data-ttu-id="20f86-1023">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1023">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="20f86-1024">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1024">mode</span></span>  
<span data-ttu-id="20f86-1025">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1025">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="20f86-1026">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="20f86-1026">Return Value - left</span></span>

<span data-ttu-id="20f86-1027">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="20f86-1027">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="20f86-1028">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1028">Method leftMode</span></span>

<span data-ttu-id="20f86-1029">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1029">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="20f86-1030">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1030">Parameters - leftMode</span></span>

<span data-ttu-id="20f86-1031">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1031">value</span></span>  
<span data-ttu-id="20f86-1032">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1032">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="20f86-1033">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1033">Return Value - leftMode</span></span>

<span data-ttu-id="20f86-1034">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="20f86-1034">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="20f86-1035">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1035">Method leftValue</span></span>

<span data-ttu-id="20f86-1036">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1036">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="20f86-1037">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1037">Parameters - leftValue</span></span>

<span data-ttu-id="20f86-1038">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1038">value</span></span>  
<span data-ttu-id="20f86-1039">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1039">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="20f86-1040">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1040">Return Value - leftValue</span></span>

<span data-ttu-id="20f86-1041">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="20f86-1041">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="20f86-1042">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="20f86-1042">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="20f86-1043">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="20f86-1043">Parameters - limitText</span></span>

<span data-ttu-id="20f86-1044">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1044">value</span></span>  

<!-- -->

<span data-ttu-id="20f86-1045">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1045">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="20f86-1046">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="20f86-1046">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="20f86-1047">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1047">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="20f86-1048">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1048">Parameters - limitTextMode</span></span>

<span data-ttu-id="20f86-1049">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1049">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="20f86-1050">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1050">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="20f86-1051">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1051">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="20f86-1052">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1052">Parameters - limitTextValue</span></span>

<span data-ttu-id="20f86-1053">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1053">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="20f86-1054">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1054">Return Value - limitTextValue</span></span>

## <a name="method-linefromchar"></a><span data-ttu-id="20f86-1055">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="20f86-1055">Method lineFromChar</span></span>

```xpp
public int lineFromChar(int charIndex)
```

### <a name="parameters---linefromchar"></a><span data-ttu-id="20f86-1056">パラメーター - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="20f86-1056">Parameters - lineFromChar</span></span>

<span data-ttu-id="20f86-1057">charIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-1057">charIndex</span></span>  

### <a name="return-value---linefromchar"></a><span data-ttu-id="20f86-1058">戻り値 - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="20f86-1058">Return Value - lineFromChar</span></span>

## <a name="method-lineindex"></a><span data-ttu-id="20f86-1059">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-1059">Method lineIndex</span></span>

```xpp
public int lineIndex(int lineNo)
```

### <a name="parameters---lineindex"></a><span data-ttu-id="20f86-1060">パラメーター - lineIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-1060">Parameters - lineIndex</span></span>

<span data-ttu-id="20f86-1061">lineNo</span><span class="sxs-lookup"><span data-stu-id="20f86-1061">lineNo</span></span>  

### <a name="return-value---lineindex"></a><span data-ttu-id="20f86-1062">戻り値 - lineIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-1062">Return Value - lineIndex</span></span>

## <a name="method-linelength"></a><span data-ttu-id="20f86-1063">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="20f86-1063">Method lineLength</span></span>

```xpp
public int lineLength(int lineNo)
```

### <a name="parameters---linelength"></a><span data-ttu-id="20f86-1064">パラメーター - lineLength</span><span class="sxs-lookup"><span data-stu-id="20f86-1064">Parameters - lineLength</span></span>

<span data-ttu-id="20f86-1065">lineNo</span><span class="sxs-lookup"><span data-stu-id="20f86-1065">lineNo</span></span>  

### <a name="return-value---linelength"></a><span data-ttu-id="20f86-1066">戻り値 - lineLength</span><span class="sxs-lookup"><span data-stu-id="20f86-1066">Return Value - lineLength</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="20f86-1067">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="20f86-1067">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="20f86-1068">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="20f86-1068">Parameters - lookupButton</span></span>

<span data-ttu-id="20f86-1069">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1069">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="20f86-1070">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="20f86-1070">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="20f86-1071">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="20f86-1071">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="20f86-1072">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="20f86-1072">Parameters - mandatory</span></span>

<span data-ttu-id="20f86-1073">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1073">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="20f86-1074">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="20f86-1074">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="20f86-1075">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="20f86-1075">Method markAsUserAdd</span></span>

<span data-ttu-id="20f86-1076">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="20f86-1076">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="20f86-1077">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="20f86-1077">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="20f86-1078">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1078">value</span></span>  
<span data-ttu-id="20f86-1079">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1079">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="20f86-1080">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="20f86-1080">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="20f86-1081">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-1081">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="20f86-1082">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="20f86-1082">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="20f86-1083">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="20f86-1083">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="20f86-1084">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="20f86-1084">Method mouseDblClick</span></span>

<span data-ttu-id="20f86-1085">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1085">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="20f86-1086">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="20f86-1086">Parameters - mouseDblClick</span></span>

<span data-ttu-id="20f86-1087">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1087">x</span></span>  
<span data-ttu-id="20f86-1088">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1088">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1089">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1089">y</span></span>  
<span data-ttu-id="20f86-1090">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1090">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1091">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-1091">button</span></span>  
<span data-ttu-id="20f86-1092">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1092">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1093">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-1093">Ctrl</span></span>  
<span data-ttu-id="20f86-1094">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1094">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1095">シフト</span><span class="sxs-lookup"><span data-stu-id="20f86-1095">Shift</span></span>  
<span data-ttu-id="20f86-1096">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1096">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="20f86-1097">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="20f86-1097">Return Value - mouseDblClick</span></span>

<span data-ttu-id="20f86-1098">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1098">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="20f86-1099">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="20f86-1099">Remarks - mouseDblClick</span></span>

<span data-ttu-id="20f86-1100">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1100">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="20f86-1101">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="20f86-1101">Method mouseDown</span></span>

<span data-ttu-id="20f86-1102">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1102">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="20f86-1103">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="20f86-1103">Parameters - mouseDown</span></span>

<span data-ttu-id="20f86-1104">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1104">x</span></span>  
<span data-ttu-id="20f86-1105">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1105">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1106">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1106">y</span></span>  
<span data-ttu-id="20f86-1107">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1107">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1108">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-1108">button</span></span>  
<span data-ttu-id="20f86-1109">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1109">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1110">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-1110">Ctrl</span></span>  
<span data-ttu-id="20f86-1111">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1111">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1112">シフト</span><span class="sxs-lookup"><span data-stu-id="20f86-1112">Shift</span></span>  
<span data-ttu-id="20f86-1113">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1113">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="20f86-1114">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="20f86-1114">Return Value - mouseDown</span></span>

<span data-ttu-id="20f86-1115">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1115">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="20f86-1116">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="20f86-1116">Remarks - mouseDown</span></span>

<span data-ttu-id="20f86-1117">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1117">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="20f86-1118">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1118">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="20f86-1119">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="20f86-1119">Method mouseMove</span></span>

<span data-ttu-id="20f86-1120">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1120">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="20f86-1121">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="20f86-1121">Parameters - mouseMove</span></span>

<span data-ttu-id="20f86-1122">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1122">x</span></span>  
<span data-ttu-id="20f86-1123">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1123">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1124">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1124">y</span></span>  
<span data-ttu-id="20f86-1125">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1125">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1126">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-1126">button</span></span>  
<span data-ttu-id="20f86-1127">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1127">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1128">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-1128">Ctrl</span></span>  
<span data-ttu-id="20f86-1129">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1129">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1130">シフト</span><span class="sxs-lookup"><span data-stu-id="20f86-1130">Shift</span></span>  
<span data-ttu-id="20f86-1131">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1131">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="20f86-1132">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="20f86-1132">Return Value - mouseMove</span></span>

<span data-ttu-id="20f86-1133">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1133">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="20f86-1134">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="20f86-1134">Remarks - mouseMove</span></span>

<span data-ttu-id="20f86-1135">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1135">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="20f86-1136">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="20f86-1136">Method mouseUp</span></span>

<span data-ttu-id="20f86-1137">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1137">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="20f86-1138">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="20f86-1138">Parameters - mouseUp</span></span>

<span data-ttu-id="20f86-1139">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1139">x</span></span>  
<span data-ttu-id="20f86-1140">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1140">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1141">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1141">y</span></span>  
<span data-ttu-id="20f86-1142">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1142">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1143">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-1143">button</span></span>  
<span data-ttu-id="20f86-1144">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1144">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1145">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-1145">Ctrl</span></span>  
<span data-ttu-id="20f86-1146">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1146">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1147">シフト</span><span class="sxs-lookup"><span data-stu-id="20f86-1147">Shift</span></span>  
<span data-ttu-id="20f86-1148">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1148">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="20f86-1149">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="20f86-1149">Return Value - mouseUp</span></span>

<span data-ttu-id="20f86-1150">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1150">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="20f86-1151">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="20f86-1151">Remarks - mouseUp</span></span>

<span data-ttu-id="20f86-1152">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1152">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="20f86-1153">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1153">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="20f86-1154">メソッド名</span><span class="sxs-lookup"><span data-stu-id="20f86-1154">Method name</span></span>

<span data-ttu-id="20f86-1155">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1155">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="20f86-1156">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="20f86-1156">Parameters - name</span></span>

<span data-ttu-id="20f86-1157">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1157">value</span></span>  
<span data-ttu-id="20f86-1158">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="20f86-1158">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="20f86-1159">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="20f86-1159">Return Value - name</span></span>

<span data-ttu-id="20f86-1160">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="20f86-1160">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="20f86-1161">備考 - name</span><span class="sxs-lookup"><span data-stu-id="20f86-1161">Remarks - name</span></span>

<span data-ttu-id="20f86-1162">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="20f86-1162">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="20f86-1163">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1163">Begins with a letter.</span></span>
-   <span data-ttu-id="20f86-1164">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="20f86-1164">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="20f86-1165">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1165">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="20f86-1166">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="20f86-1166">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="20f86-1167">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="20f86-1167">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="20f86-1168">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="20f86-1168">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="20f86-1169">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="20f86-1169">Parameters - neededPermission</span></span>

<span data-ttu-id="20f86-1170">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1170">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="20f86-1171">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="20f86-1171">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="20f86-1172">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="20f86-1172">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="20f86-1173">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="20f86-1173">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="20f86-1174">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="20f86-1174">Method parentControl</span></span>

<span data-ttu-id="20f86-1175">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1175">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="20f86-1176">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="20f86-1176">Return Value - parentControl</span></span>

<span data-ttu-id="20f86-1177">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="20f86-1177">The parent control for the control.</span></span>

## <a name="method-posfromchar"></a><span data-ttu-id="20f86-1178">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="20f86-1178">Method posFromChar</span></span>

```xpp
public container posFromChar(int charIndex)
```

### <a name="parameters---posfromchar"></a><span data-ttu-id="20f86-1179">パラメーター - posFromChar</span><span class="sxs-lookup"><span data-stu-id="20f86-1179">Parameters - posFromChar</span></span>

<span data-ttu-id="20f86-1180">charIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-1180">charIndex</span></span>  

### <a name="return-value---posfromchar"></a><span data-ttu-id="20f86-1181">戻り値 - posFromChar</span><span class="sxs-lookup"><span data-stu-id="20f86-1181">Return Value - posFromChar</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="20f86-1182">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="20f86-1182">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="20f86-1183">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="20f86-1183">Parameters - previewPartRef</span></span>

<span data-ttu-id="20f86-1184">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1184">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="20f86-1185">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="20f86-1185">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="20f86-1186">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="20f86-1186">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="20f86-1187">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="20f86-1187">Parameters - promptrect</span></span>

<span data-ttu-id="20f86-1188">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1188">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="20f86-1189">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="20f86-1189">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="20f86-1190">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1190">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="20f86-1191">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1191">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="20f86-1192">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1192">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="20f86-1193">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1193">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="20f86-1194">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="20f86-1194">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="20f86-1195">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="20f86-1195">Parameters - searchAfterInput</span></span>

<span data-ttu-id="20f86-1196">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1196">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="20f86-1197">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="20f86-1197">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="20f86-1198">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1198">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="20f86-1199">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1199">Parameters - searchMode</span></span>

<span data-ttu-id="20f86-1200">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1200">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="20f86-1201">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1201">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="20f86-1202">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="20f86-1202">Method securityKey</span></span>

<span data-ttu-id="20f86-1203">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1203">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="20f86-1204">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="20f86-1204">Parameters - securityKey</span></span>

<span data-ttu-id="20f86-1205">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1205">value</span></span>  
<span data-ttu-id="20f86-1206">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1206">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="20f86-1207">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="20f86-1207">Return Value - securityKey</span></span>

<span data-ttu-id="20f86-1208">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1208">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="20f86-1209">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="20f86-1209">Method showContextMenu</span></span>

<span data-ttu-id="20f86-1210">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1210">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="20f86-1211">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="20f86-1211">Parameters - showContextMenu</span></span>

<span data-ttu-id="20f86-1212">menuHandle</span><span class="sxs-lookup"><span data-stu-id="20f86-1212">menuHandle</span></span>  
<span data-ttu-id="20f86-1213">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="20f86-1213">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="20f86-1214">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="20f86-1214">Return Value - showContextMenu</span></span>

<span data-ttu-id="20f86-1215">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1215">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="20f86-1216">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="20f86-1216">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="20f86-1217">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="20f86-1217">Parameters - showLabel</span></span>

<span data-ttu-id="20f86-1218">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1218">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="20f86-1219">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="20f86-1219">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="20f86-1220">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="20f86-1220">Method skip</span></span>

<span data-ttu-id="20f86-1221">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1221">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="20f86-1222">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="20f86-1222">Parameters - skip</span></span>

<span data-ttu-id="20f86-1223">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1223">value</span></span>  
<span data-ttu-id="20f86-1224">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1224">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="20f86-1225">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="20f86-1225">Return Value - skip</span></span>

<span data-ttu-id="20f86-1226">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="20f86-1226">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="20f86-1227">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="20f86-1227">Remarks - skip</span></span>

<span data-ttu-id="20f86-1228">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1228">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="20f86-1229">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="20f86-1229">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="20f86-1230">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="20f86-1230">Parameters - sort</span></span>

<span data-ttu-id="20f86-1231">sortDirection</span><span class="sxs-lookup"><span data-stu-id="20f86-1231">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="20f86-1232">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="20f86-1232">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="20f86-1233">メソッド style</span><span class="sxs-lookup"><span data-stu-id="20f86-1233">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="20f86-1234">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="20f86-1234">Parameters - style</span></span>

<span data-ttu-id="20f86-1235">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1235">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="20f86-1236">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="20f86-1236">Return Value - style</span></span>

## <a name="method-timeformat"></a><span data-ttu-id="20f86-1237">メソッド timeFormat</span><span class="sxs-lookup"><span data-stu-id="20f86-1237">Method timeFormat</span></span>

```xpp
public int timeFormat([int value])
```

### <a name="parameters---timeformat"></a><span data-ttu-id="20f86-1238">パラメーター - timeFormat</span><span class="sxs-lookup"><span data-stu-id="20f86-1238">Parameters - timeFormat</span></span>

<span data-ttu-id="20f86-1239">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1239">value</span></span>  

### <a name="return-value---timeformat"></a><span data-ttu-id="20f86-1240">戻り値 - timeFormat</span><span class="sxs-lookup"><span data-stu-id="20f86-1240">Return Value - timeFormat</span></span>

## <a name="method-timehours"></a><span data-ttu-id="20f86-1241">メソッド timeHours</span><span class="sxs-lookup"><span data-stu-id="20f86-1241">Method timeHours</span></span>

```xpp
public int timeHours([int value])
```

### <a name="parameters---timehours"></a><span data-ttu-id="20f86-1242">パラメーター - timeHours</span><span class="sxs-lookup"><span data-stu-id="20f86-1242">Parameters - timeHours</span></span>

<span data-ttu-id="20f86-1243">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1243">value</span></span>  

### <a name="return-value---timehours"></a><span data-ttu-id="20f86-1244">戻り値 - timeHours</span><span class="sxs-lookup"><span data-stu-id="20f86-1244">Return Value - timeHours</span></span>

## <a name="method-timeminute"></a><span data-ttu-id="20f86-1245">メソッド timeMinute</span><span class="sxs-lookup"><span data-stu-id="20f86-1245">Method timeMinute</span></span>

```xpp
public int timeMinute([int value])
```

### <a name="parameters---timeminute"></a><span data-ttu-id="20f86-1246">パラメーター - timeMinute</span><span class="sxs-lookup"><span data-stu-id="20f86-1246">Parameters - timeMinute</span></span>

<span data-ttu-id="20f86-1247">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1247">value</span></span>  

### <a name="return-value---timeminute"></a><span data-ttu-id="20f86-1248">戻り値 - timeMinute</span><span class="sxs-lookup"><span data-stu-id="20f86-1248">Return Value - timeMinute</span></span>

## <a name="method-timeseconds"></a><span data-ttu-id="20f86-1249">メソッド timeSeconds</span><span class="sxs-lookup"><span data-stu-id="20f86-1249">Method timeSeconds</span></span>

```xpp
public int timeSeconds([int value])
```

### <a name="parameters---timeseconds"></a><span data-ttu-id="20f86-1250">パラメーター - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="20f86-1250">Parameters - timeSeconds</span></span>

<span data-ttu-id="20f86-1251">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1251">value</span></span>  

### <a name="return-value---timeseconds"></a><span data-ttu-id="20f86-1252">戻り値 - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="20f86-1252">Return Value - timeSeconds</span></span>

## <a name="method-timeseparator"></a><span data-ttu-id="20f86-1253">メソッド timeSeparator</span><span class="sxs-lookup"><span data-stu-id="20f86-1253">Method timeSeparator</span></span>

```xpp
public int timeSeparator([int value])
```

### <a name="parameters---timeseparator"></a><span data-ttu-id="20f86-1254">パラメーター - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="20f86-1254">Parameters - timeSeparator</span></span>

<span data-ttu-id="20f86-1255">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1255">value</span></span>  

### <a name="return-value---timeseparator"></a><span data-ttu-id="20f86-1256">戻り値 - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="20f86-1256">Return Value - timeSeparator</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="20f86-1257">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="20f86-1257">Method toolTip</span></span>

<span data-ttu-id="20f86-1258">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1258">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="20f86-1259">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="20f86-1259">Return Value - toolTip</span></span>

<span data-ttu-id="20f86-1260">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="20f86-1260">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="20f86-1261">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="20f86-1261">Remarks - toolTip</span></span>

<span data-ttu-id="20f86-1262">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1262">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="20f86-1263">メソッド top</span><span class="sxs-lookup"><span data-stu-id="20f86-1263">Method top</span></span>

<span data-ttu-id="20f86-1264">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1264">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="20f86-1265">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="20f86-1265">Parameters - top</span></span>

<span data-ttu-id="20f86-1266">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1266">value</span></span>  
<span data-ttu-id="20f86-1267">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1267">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="20f86-1268">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1268">mode</span></span>  
<span data-ttu-id="20f86-1269">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1269">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="20f86-1270">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="20f86-1270">Return Value - top</span></span>

<span data-ttu-id="20f86-1271">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="20f86-1271">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="20f86-1272">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1272">Method topMode</span></span>

<span data-ttu-id="20f86-1273">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1273">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="20f86-1274">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1274">Parameters - topMode</span></span>

<span data-ttu-id="20f86-1275">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1275">value</span></span>  
<span data-ttu-id="20f86-1276">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1276">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="20f86-1277">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1277">Return Value - topMode</span></span>

<span data-ttu-id="20f86-1278">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="20f86-1278">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="20f86-1279">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1279">Method topValue</span></span>

<span data-ttu-id="20f86-1280">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1280">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="20f86-1281">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1281">Parameters - topValue</span></span>

<span data-ttu-id="20f86-1282">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1282">value</span></span>  
<span data-ttu-id="20f86-1283">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1283">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="20f86-1284">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1284">Return Value - topValue</span></span>

<span data-ttu-id="20f86-1285">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="20f86-1285">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="20f86-1286">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="20f86-1286">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="20f86-1287">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="20f86-1287">Parameters - type</span></span>

<span data-ttu-id="20f86-1288">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1288">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="20f86-1289">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="20f86-1289">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="20f86-1290">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="20f86-1290">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="20f86-1291">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="20f86-1291">Parameters - underline</span></span>

<span data-ttu-id="20f86-1292">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1292">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="20f86-1293">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="20f86-1293">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="20f86-1294">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="20f86-1294">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="20f86-1295">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="20f86-1295">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="20f86-1296">データ</span><span class="sxs-lookup"><span data-stu-id="20f86-1296">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="20f86-1297">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="20f86-1297">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="20f86-1298">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="20f86-1298">Method userData</span></span>

<span data-ttu-id="20f86-1299">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1299">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="20f86-1300">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="20f86-1300">Parameters - userData</span></span>

<span data-ttu-id="20f86-1301">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1301">value</span></span>  
<span data-ttu-id="20f86-1302">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1302">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="20f86-1303">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="20f86-1303">Return Value - userData</span></span>

<span data-ttu-id="20f86-1304">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="20f86-1304">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="20f86-1305">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="20f86-1305">Method userDataItem</span></span>

<span data-ttu-id="20f86-1306">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1306">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="20f86-1307">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="20f86-1307">Parameters - userDataItem</span></span>

<span data-ttu-id="20f86-1308">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1308">value</span></span>  
<span data-ttu-id="20f86-1309">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1309">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="20f86-1310">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="20f86-1310">Return Value - userDataItem</span></span>

<span data-ttu-id="20f86-1311">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="20f86-1311">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="20f86-1312">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="20f86-1312">Method userDataItems</span></span>

<span data-ttu-id="20f86-1313">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1313">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="20f86-1314">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="20f86-1314">Parameters - userDataItems</span></span>

<span data-ttu-id="20f86-1315">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1315">value</span></span>  
<span data-ttu-id="20f86-1316">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1316">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="20f86-1317">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="20f86-1317">Return Value - userDataItems</span></span>

<span data-ttu-id="20f86-1318">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="20f86-1318">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="20f86-1319">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="20f86-1319">Method userDisable</span></span>

<span data-ttu-id="20f86-1320">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1320">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="20f86-1321">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="20f86-1321">Parameters - userDisable</span></span>

<span data-ttu-id="20f86-1322">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1322">value</span></span>  
<span data-ttu-id="20f86-1323">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1323">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="20f86-1324">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="20f86-1324">Return Value - userDisable</span></span>

<span data-ttu-id="20f86-1325">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1325">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="20f86-1326">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="20f86-1326">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="20f86-1327">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="20f86-1327">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="20f86-1328">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1328">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="20f86-1329">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="20f86-1329">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="20f86-1330">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-1330">Method userHeight</span></span>

<span data-ttu-id="20f86-1331">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1331">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="20f86-1332">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-1332">Parameters - userHeight</span></span>

<span data-ttu-id="20f86-1333">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1333">value</span></span>  
<span data-ttu-id="20f86-1334">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1334">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="20f86-1335">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="20f86-1335">Return Value - userHeight</span></span>

<span data-ttu-id="20f86-1336">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="20f86-1336">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="20f86-1337">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="20f86-1337">Method userHide</span></span>

<span data-ttu-id="20f86-1338">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1338">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="20f86-1339">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="20f86-1339">Parameters - userHide</span></span>

<span data-ttu-id="20f86-1340">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1340">value</span></span>  
<span data-ttu-id="20f86-1341">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1341">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="20f86-1342">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="20f86-1342">Return Value - userHide</span></span>

<span data-ttu-id="20f86-1343">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1343">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="20f86-1344">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="20f86-1344">Remarks - userHide</span></span>

<span data-ttu-id="20f86-1345">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1345">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="20f86-1346">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1346">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="20f86-1347">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1347">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="20f86-1348">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="20f86-1348">Method userOrgContainer</span></span>

<span data-ttu-id="20f86-1349">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1349">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="20f86-1350">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="20f86-1350">Parameters - userOrgContainer</span></span>

<span data-ttu-id="20f86-1351">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1351">value</span></span>  
<span data-ttu-id="20f86-1352">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1352">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="20f86-1353">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="20f86-1353">Return Value - userOrgContainer</span></span>

<span data-ttu-id="20f86-1354">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="20f86-1354">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="20f86-1355">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="20f86-1355">Method userOrgSibling</span></span>

<span data-ttu-id="20f86-1356">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1356">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="20f86-1357">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="20f86-1357">Parameters - userOrgSibling</span></span>

<span data-ttu-id="20f86-1358">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1358">value</span></span>  
<span data-ttu-id="20f86-1359">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1359">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="20f86-1360">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="20f86-1360">Return Value - userOrgSibling</span></span>

<span data-ttu-id="20f86-1361">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="20f86-1361">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="20f86-1362">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="20f86-1362">Method userPromptText</span></span>

<span data-ttu-id="20f86-1363">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1363">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="20f86-1364">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="20f86-1364">Parameters - userPromptText</span></span>

<span data-ttu-id="20f86-1365">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1365">value</span></span>  
<span data-ttu-id="20f86-1366">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1366">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="20f86-1367">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="20f86-1367">Return Value - userPromptText</span></span>

<span data-ttu-id="20f86-1368">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="20f86-1368">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="20f86-1369">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="20f86-1369">Method userSecurityLevel</span></span>

<span data-ttu-id="20f86-1370">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1370">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="20f86-1371">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="20f86-1371">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="20f86-1372">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1372">value</span></span>  
<span data-ttu-id="20f86-1373">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1373">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="20f86-1374">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="20f86-1374">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="20f86-1375">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="20f86-1375">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="20f86-1376">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="20f86-1376">Method userSkip</span></span>

<span data-ttu-id="20f86-1377">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1377">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="20f86-1378">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="20f86-1378">Parameters - userSkip</span></span>

<span data-ttu-id="20f86-1379">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1379">value</span></span>  
<span data-ttu-id="20f86-1380">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1380">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="20f86-1381">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1381">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="20f86-1382">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="20f86-1382">Return Value - userSkip</span></span>

<span data-ttu-id="20f86-1383">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="20f86-1383">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="20f86-1384">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="20f86-1384">Method userWidth</span></span>

<span data-ttu-id="20f86-1385">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1385">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="20f86-1386">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="20f86-1386">Parameters - userWidth</span></span>

<span data-ttu-id="20f86-1387">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1387">value</span></span>  
<span data-ttu-id="20f86-1388">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1388">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="20f86-1389">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="20f86-1389">Return Value - userWidth</span></span>

<span data-ttu-id="20f86-1390">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1390">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="20f86-1391">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="20f86-1391">Remarks - userWidth</span></span>

<span data-ttu-id="20f86-1392">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1392">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="20f86-1393">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="20f86-1393">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="20f86-1394">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1394">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="20f86-1395">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="20f86-1395">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="20f86-1396">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="20f86-1396">Return Value - validate</span></span>

## <a name="method-value"></a><span data-ttu-id="20f86-1397">メソッド value</span><span class="sxs-lookup"><span data-stu-id="20f86-1397">Method value</span></span>

```xpp
public int value([int value])
```

### <a name="parameters---value"></a><span data-ttu-id="20f86-1398">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="20f86-1398">Parameters - value</span></span>

<span data-ttu-id="20f86-1399">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1399">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="20f86-1400">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="20f86-1400">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="20f86-1401">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="20f86-1401">Method verticalSpacing</span></span>

<span data-ttu-id="20f86-1402">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1402">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="20f86-1403">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="20f86-1403">Parameters - verticalSpacing</span></span>

<span data-ttu-id="20f86-1404">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1404">value</span></span>  
<span data-ttu-id="20f86-1405">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1405">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="20f86-1406">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1406">mode</span></span>  
<span data-ttu-id="20f86-1407">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1407">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="20f86-1408">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="20f86-1408">Return Value - verticalSpacing</span></span>

<span data-ttu-id="20f86-1409">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="20f86-1409">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="20f86-1410">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1410">Method verticalSpacingMode</span></span>

<span data-ttu-id="20f86-1411">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1411">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="20f86-1412">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1412">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="20f86-1413">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1413">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="20f86-1414">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1414">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="20f86-1415">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="20f86-1415">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="20f86-1416">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1416">Method verticalSpacingValue</span></span>

<span data-ttu-id="20f86-1417">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1417">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="20f86-1418">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1418">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="20f86-1419">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1419">value</span></span>  
<span data-ttu-id="20f86-1420">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1420">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="20f86-1421">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1421">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="20f86-1422">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="20f86-1422">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="20f86-1423">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1423">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="20f86-1424">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1424">Parameters - viewEditMode</span></span>

<span data-ttu-id="20f86-1425">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1425">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="20f86-1426">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1426">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="20f86-1427">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="20f86-1427">Method visible</span></span>

<span data-ttu-id="20f86-1428">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1428">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="20f86-1429">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="20f86-1429">Parameters - visible</span></span>

<span data-ttu-id="20f86-1430">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1430">value</span></span>  
<span data-ttu-id="20f86-1431">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1431">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="20f86-1432">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="20f86-1432">Return Value - visible</span></span>

<span data-ttu-id="20f86-1433">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="20f86-1433">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="20f86-1434">メソッド width</span><span class="sxs-lookup"><span data-stu-id="20f86-1434">Method width</span></span>

<span data-ttu-id="20f86-1435">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1435">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="20f86-1436">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="20f86-1436">Parameters - width</span></span>

<span data-ttu-id="20f86-1437">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1437">value</span></span>  
<span data-ttu-id="20f86-1438">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1438">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="20f86-1439">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1439">mode</span></span>  
<span data-ttu-id="20f86-1440">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1440">An integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="20f86-1441">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="20f86-1441">Return Value - width</span></span>

<span data-ttu-id="20f86-1442">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="20f86-1442">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="20f86-1443">備考 - width</span><span class="sxs-lookup"><span data-stu-id="20f86-1443">Remarks - width</span></span>

<span data-ttu-id="20f86-1444">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1444">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="20f86-1445">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1445">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="20f86-1446">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1446">Mode</span></span>           | <span data-ttu-id="20f86-1447">幅計算</span><span class="sxs-lookup"><span data-stu-id="20f86-1447">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f86-1448">-1 正確</span><span class="sxs-lookup"><span data-stu-id="20f86-1448">-1 Exact</span></span>       | <span data-ttu-id="20f86-1449">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1449">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="20f86-1450">0 自動</span><span class="sxs-lookup"><span data-stu-id="20f86-1450">0 Auto</span></span>         | <span data-ttu-id="20f86-1451">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1451">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="20f86-1452">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="20f86-1452">1 Column width</span></span> | <span data-ttu-id="20f86-1453">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="20f86-1453">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="20f86-1454">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1454">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="20f86-1455">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1455">Method widthMode</span></span>

<span data-ttu-id="20f86-1456">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1456">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="20f86-1457">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1457">Parameters - widthMode</span></span>

<span data-ttu-id="20f86-1458">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1458">value</span></span>  
<span data-ttu-id="20f86-1459">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1459">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="20f86-1460">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1460">Return Value - widthMode</span></span>

<span data-ttu-id="20f86-1461">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1461">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="20f86-1462">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1462">Remarks - widthMode</span></span>

<span data-ttu-id="20f86-1463">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1463">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="20f86-1464">モード</span><span class="sxs-lookup"><span data-stu-id="20f86-1464">Mode</span></span>         | <span data-ttu-id="20f86-1465">幅計算</span><span class="sxs-lookup"><span data-stu-id="20f86-1465">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f86-1466">正確</span><span class="sxs-lookup"><span data-stu-id="20f86-1466">Exact</span></span>        | <span data-ttu-id="20f86-1467">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1467">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="20f86-1468">自動</span><span class="sxs-lookup"><span data-stu-id="20f86-1468">Auto</span></span>         | <span data-ttu-id="20f86-1469">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1469">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="20f86-1470">列の幅</span><span class="sxs-lookup"><span data-stu-id="20f86-1470">Column width</span></span> | <span data-ttu-id="20f86-1471">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="20f86-1471">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="20f86-1472">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="20f86-1472">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="20f86-1473">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1473">Method widthValue</span></span>

<span data-ttu-id="20f86-1474">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1474">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="20f86-1475">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1475">Parameters - widthValue</span></span>

<span data-ttu-id="20f86-1476">値</span><span class="sxs-lookup"><span data-stu-id="20f86-1476">value</span></span>  
<span data-ttu-id="20f86-1477">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="20f86-1477">An integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="20f86-1478">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1478">Return Value - widthValue</span></span>

<span data-ttu-id="20f86-1479">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="20f86-1479">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="20f86-1480">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="20f86-1480">Remarks - widthValue</span></span>

<span data-ttu-id="20f86-1481">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1481">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-performtypelookup"></a><span data-ttu-id="20f86-1482">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1482">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="20f86-1483">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1483">Parameters - performTypeLookup</span></span>

<span data-ttu-id="20f86-1484">userType</span><span class="sxs-lookup"><span data-stu-id="20f86-1484">userType</span></span>  

<!-- -->

<span data-ttu-id="20f86-1485">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="20f86-1485">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="20f86-1486">会社</span><span class="sxs-lookup"><span data-stu-id="20f86-1486">company</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="20f86-1487">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="20f86-1487">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="20f86-1488">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="20f86-1488">Parameters - OnLostFocus</span></span>

<span data-ttu-id="20f86-1489">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1489">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1490">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1490">e</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="20f86-1491">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="20f86-1491">Method endDrag</span></span>

<span data-ttu-id="20f86-1492">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1492">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="20f86-1493">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="20f86-1493">Remarks - endDrag</span></span>

<span data-ttu-id="20f86-1494">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="20f86-1494">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="20f86-1495">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1495">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-textchange"></a><span data-ttu-id="20f86-1496">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="20f86-1496">Method textChange</span></span>

```xpp
public void textChange()
```

## <a name="method-lookup"></a><span data-ttu-id="20f86-1497">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1497">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-onenter"></a><span data-ttu-id="20f86-1498">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="20f86-1498">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="20f86-1499">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="20f86-1499">Parameters - OnEnter</span></span>

<span data-ttu-id="20f86-1500">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1500">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1501">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1501">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="20f86-1502">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="20f86-1502">Method mouseLeave</span></span>

<span data-ttu-id="20f86-1503">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1503">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-undo"></a><span data-ttu-id="20f86-1504">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="20f86-1504">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-setcursorpos"></a><span data-ttu-id="20f86-1505">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="20f86-1505">Method setCursorPos</span></span>

```xpp
public void setCursorPos(int x, int y)
```

### <a name="parameters---setcursorpos"></a><span data-ttu-id="20f86-1506">パラメーター - setCursorPos</span><span class="sxs-lookup"><span data-stu-id="20f86-1506">Parameters - setCursorPos</span></span>

<span data-ttu-id="20f86-1507">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1507">x</span></span>  

<!-- -->

<span data-ttu-id="20f86-1508">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1508">y</span></span>  

## <a name="method-performdblookup"></a><span data-ttu-id="20f86-1509">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1509">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="20f86-1510">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1510">Parameters - performDBLookup</span></span>

<span data-ttu-id="20f86-1511">fieldId</span><span class="sxs-lookup"><span data-stu-id="20f86-1511">fieldId</span></span>  

<!-- -->

<span data-ttu-id="20f86-1512">tableId</span><span class="sxs-lookup"><span data-stu-id="20f86-1512">tableId</span></span>  

<!-- -->

<span data-ttu-id="20f86-1513">会社</span><span class="sxs-lookup"><span data-stu-id="20f86-1513">company</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="20f86-1514">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="20f86-1514">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="20f86-1515">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="20f86-1515">Parameters - OnValidated</span></span>

<span data-ttu-id="20f86-1516">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1516">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1517">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1517">e</span></span>  

## <a name="method-context"></a><span data-ttu-id="20f86-1518">メソッド context</span><span class="sxs-lookup"><span data-stu-id="20f86-1518">Method context</span></span>

<span data-ttu-id="20f86-1519">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1519">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-dropex"></a><span data-ttu-id="20f86-1520">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="20f86-1520">Method dropEx</span></span>

<span data-ttu-id="20f86-1521">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1521">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="20f86-1522">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="20f86-1522">Parameters - dropEx</span></span>

<span data-ttu-id="20f86-1523">dragSource</span><span class="sxs-lookup"><span data-stu-id="20f86-1523">dragSource</span></span>  
<span data-ttu-id="20f86-1524">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1524">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-1525">dragMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1525">dragMode</span></span>  
<span data-ttu-id="20f86-1526">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1526">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-1527">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1527">x</span></span>  
<span data-ttu-id="20f86-1528">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1528">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-1529">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1529">y</span></span>  
<span data-ttu-id="20f86-1530">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1530">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="20f86-1531">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="20f86-1531">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="20f86-1532">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="20f86-1532">Parameters - OnLeaving</span></span>

<span data-ttu-id="20f86-1533">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1533">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1534">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1534">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="20f86-1535">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="20f86-1535">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="20f86-1536">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="20f86-1536">Parameters - filter</span></span>

<span data-ttu-id="20f86-1537">filterStr</span><span class="sxs-lookup"><span data-stu-id="20f86-1537">filterStr</span></span>  

## <a name="method-onlookup"></a><span data-ttu-id="20f86-1538">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1538">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="20f86-1539">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1539">Parameters - OnLookup</span></span>

<span data-ttu-id="20f86-1540">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1540">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1541">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1541">e</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="20f86-1542">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="20f86-1542">Method resetUserSetting</span></span>

<span data-ttu-id="20f86-1543">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="20f86-1543">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="20f86-1544">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="20f86-1544">Method displayControl</span></span>

<span data-ttu-id="20f86-1545">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1545">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-enter"></a><span data-ttu-id="20f86-1546">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="20f86-1546">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-inputsearch"></a><span data-ttu-id="20f86-1547">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="20f86-1547">Method inputSearch</span></span>

<span data-ttu-id="20f86-1548">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1548">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="20f86-1549">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="20f86-1549">Parameters - inputSearch</span></span>

<span data-ttu-id="20f86-1550">searchStr</span><span class="sxs-lookup"><span data-stu-id="20f86-1550">searchStr</span></span>  
<span data-ttu-id="20f86-1551">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="20f86-1551">The string value to use to filter data; optional.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="20f86-1552">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="20f86-1552">Method setFocus</span></span>

<span data-ttu-id="20f86-1553">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1553">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-gotfocus"></a><span data-ttu-id="20f86-1554">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="20f86-1554">Method gotFocus</span></span>

<span data-ttu-id="20f86-1555">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1555">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-copy"></a><span data-ttu-id="20f86-1556">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="20f86-1556">Method copy</span></span>

<span data-ttu-id="20f86-1557">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="20f86-1557">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-dragleave"></a><span data-ttu-id="20f86-1558">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="20f86-1558">Method dragLeave</span></span>

<span data-ttu-id="20f86-1559">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1559">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-linescroll"></a><span data-ttu-id="20f86-1560">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="20f86-1560">Method lineScroll</span></span>

```xpp
public void lineScroll(int dx, int dy)
```

### <a name="parameters---linescroll"></a><span data-ttu-id="20f86-1561">パラメーター - lineScroll</span><span class="sxs-lookup"><span data-stu-id="20f86-1561">Parameters - lineScroll</span></span>

<span data-ttu-id="20f86-1562">dx</span><span class="sxs-lookup"><span data-stu-id="20f86-1562">dx</span></span>  

<!-- -->

<span data-ttu-id="20f86-1563">dy</span><span class="sxs-lookup"><span data-stu-id="20f86-1563">dy</span></span>  

## <a name="method-cut"></a><span data-ttu-id="20f86-1564">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="20f86-1564">Method cut</span></span>

<span data-ttu-id="20f86-1565">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="20f86-1565">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="20f86-1566">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="20f86-1566">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="20f86-1567">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="20f86-1567">Parameters - OnGotFocus</span></span>

<span data-ttu-id="20f86-1568">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1568">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1569">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1569">e</span></span>  

## <a name="method-performformlookup"></a><span data-ttu-id="20f86-1570">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1570">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="20f86-1571">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="20f86-1571">Parameters - performFormLookup</span></span>

<span data-ttu-id="20f86-1572">フォーム</span><span class="sxs-lookup"><span data-stu-id="20f86-1572">form</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="20f86-1573">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="20f86-1573">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="20f86-1574">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="20f86-1574">Parameters - OnModified</span></span>

<span data-ttu-id="20f86-1575">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1575">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1576">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1576">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="20f86-1577">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="20f86-1577">Method paste</span></span>

<span data-ttu-id="20f86-1578">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1578">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="20f86-1579">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="20f86-1579">Method prefColumnSize</span></span>

<span data-ttu-id="20f86-1580">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1580">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="20f86-1581">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="20f86-1581">Parameters - prefColumnSize</span></span>

<span data-ttu-id="20f86-1582">width</span><span class="sxs-lookup"><span data-stu-id="20f86-1582">width</span></span>  
<span data-ttu-id="20f86-1583">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="20f86-1583">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="20f86-1584">height</span><span class="sxs-lookup"><span data-stu-id="20f86-1584">height</span></span>  
<span data-ttu-id="20f86-1585">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="20f86-1585">The preferred height of the control.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="20f86-1586">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-1586">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="20f86-1587">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="20f86-1587">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="20f86-1588">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="20f86-1588">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="20f86-1589">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="20f86-1589">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="20f86-1590">overrideObject</span><span class="sxs-lookup"><span data-stu-id="20f86-1590">overrideObject</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="20f86-1591">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="20f86-1591">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-lostfocus"></a><span data-ttu-id="20f86-1592">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="20f86-1592">Method lostFocus</span></span>

<span data-ttu-id="20f86-1593">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="20f86-1593">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="20f86-1594">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="20f86-1594">Method mouseEnter</span></span>

<span data-ttu-id="20f86-1595">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1595">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="20f86-1596">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="20f86-1596">Parameters - mouseEnter</span></span>

<span data-ttu-id="20f86-1597">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1597">x</span></span>  
<span data-ttu-id="20f86-1598">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1598">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1599">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1599">y</span></span>  
<span data-ttu-id="20f86-1600">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1600">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1601">ボタン</span><span class="sxs-lookup"><span data-stu-id="20f86-1601">button</span></span>  
<span data-ttu-id="20f86-1602">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1602">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1603">Ctrl</span><span class="sxs-lookup"><span data-stu-id="20f86-1603">Ctrl</span></span>  
<span data-ttu-id="20f86-1604">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1604">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="20f86-1605">シフト</span><span class="sxs-lookup"><span data-stu-id="20f86-1605">Shift</span></span>  
<span data-ttu-id="20f86-1606">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1606">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-scrollcursor"></a><span data-ttu-id="20f86-1607">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="20f86-1607">Method scrollCursor</span></span>

```xpp
public void scrollCursor()
```

## <a name="method-pastetext"></a><span data-ttu-id="20f86-1608">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="20f86-1608">Method pasteText</span></span>

```xpp
public void pasteText(str pasteStr, [boolean InsertSel])
```

### <a name="parameters---pastetext"></a><span data-ttu-id="20f86-1609">パラメーター - pasteText</span><span class="sxs-lookup"><span data-stu-id="20f86-1609">Parameters - pasteText</span></span>

<span data-ttu-id="20f86-1610">pasteStr</span><span class="sxs-lookup"><span data-stu-id="20f86-1610">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="20f86-1611">InsertSel</span><span class="sxs-lookup"><span data-stu-id="20f86-1611">InsertSel</span></span>  

## <a name="method-onvalidating"></a><span data-ttu-id="20f86-1612">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="20f86-1612">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="20f86-1613">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="20f86-1613">Parameters - OnValidating</span></span>

<span data-ttu-id="20f86-1614">sender</span><span class="sxs-lookup"><span data-stu-id="20f86-1614">sender</span></span>  

<!-- -->

<span data-ttu-id="20f86-1615">e</span><span class="sxs-lookup"><span data-stu-id="20f86-1615">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="20f86-1616">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="20f86-1616">Method drop</span></span>

<span data-ttu-id="20f86-1617">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="20f86-1617">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="20f86-1618">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="20f86-1618">Parameters - drop</span></span>

<span data-ttu-id="20f86-1619">dragSource</span><span class="sxs-lookup"><span data-stu-id="20f86-1619">dragSource</span></span>  
<span data-ttu-id="20f86-1620">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1620">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-1621">dragMode</span><span class="sxs-lookup"><span data-stu-id="20f86-1621">dragMode</span></span>  
<span data-ttu-id="20f86-1622">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1622">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-1623">x</span><span class="sxs-lookup"><span data-stu-id="20f86-1623">x</span></span>  
<span data-ttu-id="20f86-1624">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1624">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="20f86-1625">y</span><span class="sxs-lookup"><span data-stu-id="20f86-1625">y</span></span>  
<span data-ttu-id="20f86-1626">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="20f86-1626">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-setselection"></a><span data-ttu-id="20f86-1627">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="20f86-1627">Method setSelection</span></span>

```xpp
public void setSelection(int charIndexFrom, int charIndexTo)
```

### <a name="parameters---setselection"></a><span data-ttu-id="20f86-1628">パラメーター - setSelection</span><span class="sxs-lookup"><span data-stu-id="20f86-1628">Parameters - setSelection</span></span>

<span data-ttu-id="20f86-1629">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="20f86-1629">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="20f86-1630">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="20f86-1630">charIndexTo</span></span>  

