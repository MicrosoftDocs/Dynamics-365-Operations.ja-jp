---
title: FormGuidControl クラス
description: このトピックでは、FormGuidControl クラスについて説明します。
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
ms.openlocfilehash: 5689a041d3cb334d5ee6fcbee3067302a99cef87
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502937"
---
# <a name="class-formguidcontrol"></a><span data-ttu-id="079a7-103">クラス FormGuidControl</span><span class="sxs-lookup"><span data-stu-id="079a7-103">Class FormGuidControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormGuidControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="079a7-104">備考</span><span class="sxs-lookup"><span data-stu-id="079a7-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="079a7-105">例</span><span class="sxs-lookup"><span data-stu-id="079a7-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="079a7-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="079a7-106">Methods</span></span>

| <span data-ttu-id="079a7-107">方法</span><span class="sxs-lookup"><span data-stu-id="079a7-107">Method</span></span>                                                                                                      | <span data-ttu-id="079a7-108">説明</span><span class="sxs-lookup"><span data-stu-id="079a7-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="079a7-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="079a7-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="079a7-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="079a7-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="079a7-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="079a7-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="079a7-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="079a7-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="079a7-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="079a7-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="079a7-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="079a7-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="079a7-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="079a7-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="079a7-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="079a7-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="079a7-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="079a7-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="079a7-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-126">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="079a7-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="079a7-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="079a7-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="079a7-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="079a7-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="079a7-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="079a7-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="079a7-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-133">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="079a7-134">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="079a7-134">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-135">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-135">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="079a7-136">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-136">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="079a7-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="079a7-138">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-138">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="079a7-139">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="079a7-139">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="079a7-140">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-140">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="079a7-141">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-141">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="079a7-142">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-142">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="079a7-143">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-143">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-144">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-144">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-145">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="079a7-145">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-146">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="079a7-146">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-147">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-147">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-148">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-148">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="079a7-149">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-149">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="079a7-150">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-150">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="079a7-151">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-151">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="079a7-152">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-152">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="079a7-153">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-153">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-154">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-154">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-155">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-155">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-156">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-156">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-157">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-157">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-158">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-158">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-159">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-159">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="079a7-160">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-160">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="079a7-161">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-161">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="079a7-162">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-162">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="079a7-163">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="079a7-163">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="079a7-164">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-164">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="079a7-165">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="079a7-165">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="079a7-166">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-166">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="079a7-167">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="079a7-167">public str dragText()</span></span>                                                                                       | <span data-ttu-id="079a7-168">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-168">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="079a7-169">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-169">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="079a7-170">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-170">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="079a7-171">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-171">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-172">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-172">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-173">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-173">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="079a7-174">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-174">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="079a7-175">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-175">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="079a7-176">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-176">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="079a7-177">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-177">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="079a7-178">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-178">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="079a7-179">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="079a7-179">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="079a7-180">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="079a7-180">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-181">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="079a7-181">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="079a7-182">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="079a7-182">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="079a7-183">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="079a7-183">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="079a7-184">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="079a7-184">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="079a7-185">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-185">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="079a7-186">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="079a7-186">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="079a7-187">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-187">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="079a7-188">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-188">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="079a7-189">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-189">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="079a7-190">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-190">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="079a7-191">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-191">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="079a7-192">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-192">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="079a7-193">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-193">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="079a7-194">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="079a7-194">public str helpField()</span></span>                                                                                      | <span data-ttu-id="079a7-195">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-195">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="079a7-196">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-196">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="079a7-197">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-197">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="079a7-198">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-198">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="079a7-199">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-199">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="079a7-200">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="079a7-200">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="079a7-201">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-201">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="079a7-202">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-202">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="079a7-203">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="079a7-203">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-204">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="079a7-204">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="079a7-205">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-205">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="079a7-206">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="079a7-206">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="079a7-207">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-207">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="079a7-208">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="079a7-208">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="079a7-209">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-209">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="079a7-210">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="079a7-210">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-211">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-211">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-212">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-212">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="079a7-213">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-213">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="079a7-214">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-214">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-215">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-215">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="079a7-216">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-216">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-217">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-217">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="079a7-218">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-218">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="079a7-219">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-219">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="079a7-220">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-220">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-221">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-221">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="079a7-222">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-222">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="079a7-223">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-223">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-224">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-224">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="079a7-225">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-225">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-226">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-226">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-227">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-227">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="079a7-228">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-228">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="079a7-229">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-229">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-230">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-230">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="079a7-231">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-231">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-232">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-232">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="079a7-233">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="079a7-233">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="079a7-234">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-234">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="079a7-235">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-235">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="079a7-236">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-236">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="079a7-237">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-237">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="079a7-238">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-238">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="079a7-239">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-239">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="079a7-240">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-240">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="079a7-241">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-241">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-242">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-242">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-243">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="079a7-243">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="079a7-244">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="079a7-244">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="079a7-245">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="079a7-245">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="079a7-246">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-246">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="079a7-247">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-247">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-248">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-248">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="079a7-249">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="079a7-249">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="079a7-250">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="079a7-250">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="079a7-251">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-251">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="079a7-252">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-252">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="079a7-253">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-253">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="079a7-254">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-254">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="079a7-255">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-255">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="079a7-256">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-256">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="079a7-257">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-257">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="079a7-258">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-258">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="079a7-259">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-259">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="079a7-260">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-260">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="079a7-261">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-261">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-262">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="079a7-262">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="079a7-263">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="079a7-263">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="079a7-264">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-264">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="079a7-265">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="079a7-265">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-266">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-266">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-267">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-267">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-268">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-268">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="079a7-269">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-269">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-270">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-270">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="079a7-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="079a7-272">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-272">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="079a7-273">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="079a7-273">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="079a7-274">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-274">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="079a7-275">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-275">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-276">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-276">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="079a7-277">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-277">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="079a7-278">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="079a7-278">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-279">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-279">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="079a7-280">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="079a7-280">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="079a7-281">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-281">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="079a7-282">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-282">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="079a7-283">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-283">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="079a7-284">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-284">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="079a7-285">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-285">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="079a7-286">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-286">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="079a7-287">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-287">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="079a7-288">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-288">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="079a7-289">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-289">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="079a7-290">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-290">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="079a7-291">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="079a7-291">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="079a7-292">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-292">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="079a7-293">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-293">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="079a7-294">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-294">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="079a7-295">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-295">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="079a7-296">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-296">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="079a7-297">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-297">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="079a7-298">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-298">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="079a7-299">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-299">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="079a7-300">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-300">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-301">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-301">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="079a7-302">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-302">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="079a7-303">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-303">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="079a7-304">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-304">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="079a7-305">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-305">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="079a7-306">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-306">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="079a7-307">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-307">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="079a7-308">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-308">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="079a7-309">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-309">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="079a7-310">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-310">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="079a7-311">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-311">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="079a7-312">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-312">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="079a7-313">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-313">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="079a7-314">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-314">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="079a7-315">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-315">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="079a7-316">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-316">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="079a7-317">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="079a7-317">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="079a7-318">public Guid value(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-318">public Guid value(\[Guid value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="079a7-319">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-319">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="079a7-320">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-320">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="079a7-321">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-321">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="079a7-322">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-322">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="079a7-323">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-323">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="079a7-324">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-324">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="079a7-325">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-325">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="079a7-326">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-326">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="079a7-327">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-327">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="079a7-328">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="079a7-328">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="079a7-329">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-329">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="079a7-330">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-330">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="079a7-331">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-331">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="079a7-332">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="079a7-332">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="079a7-333">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-333">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="079a7-334">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-334">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-335">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="079a7-335">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="079a7-336">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-336">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="079a7-337">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="079a7-337">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="079a7-338">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-338">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="079a7-339">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="079a7-339">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="079a7-340">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-340">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="079a7-341">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="079a7-341">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="079a7-342">public void context()</span><span class="sxs-lookup"><span data-stu-id="079a7-342">public void context()</span></span>                                                                                       | <span data-ttu-id="079a7-343">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-343">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="079a7-344">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-344">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-345">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="079a7-345">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="079a7-346">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="079a7-346">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="079a7-347">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="079a7-347">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="079a7-348">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="079a7-348">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="079a7-349">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="079a7-349">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="079a7-350">public void enter()</span><span class="sxs-lookup"><span data-stu-id="079a7-350">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="079a7-351">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="079a7-351">public void displayControl()</span></span>                                                                                | <span data-ttu-id="079a7-352">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-352">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="079a7-353">public void undo()</span><span class="sxs-lookup"><span data-stu-id="079a7-353">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="079a7-354">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="079a7-354">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="079a7-355">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-355">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="079a7-356">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-356">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-357">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="079a7-357">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="079a7-358">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-358">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="079a7-359">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-359">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-360">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="079a7-360">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="079a7-361">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-361">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="079a7-362">public void copy()</span><span class="sxs-lookup"><span data-stu-id="079a7-362">public void copy()</span></span>                                                                                          | <span data-ttu-id="079a7-363">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="079a7-363">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="079a7-364">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-364">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="079a7-365">public void paste()</span><span class="sxs-lookup"><span data-stu-id="079a7-365">public void paste()</span></span>                                                                                         | <span data-ttu-id="079a7-366">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="079a7-366">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="079a7-367">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="079a7-367">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="079a7-368">public void cut()</span><span class="sxs-lookup"><span data-stu-id="079a7-368">public void cut()</span></span>                                                                                           | <span data-ttu-id="079a7-369">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="079a7-369">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="079a7-370">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="079a7-370">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-371">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="079a7-371">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="079a7-372">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-372">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="079a7-373">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="079a7-373">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="079a7-374">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-374">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="079a7-375">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="079a7-375">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="079a7-376">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-376">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="079a7-377">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="079a7-377">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="079a7-378">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="079a7-378">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="079a7-379">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="079a7-379">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-380">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-380">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-381">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="079a7-381">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="079a7-382">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="079a7-382">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="079a7-383">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-383">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="079a7-384">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="079a7-384">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="079a7-385">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="079a7-385">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="079a7-386">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="079a7-386">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="079a7-387">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-387">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="079a7-388">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="079a7-388">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="079a7-389">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="079a7-389">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="079a7-390">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="079a7-390">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="079a7-391">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="079a7-391">Method alignControl</span></span>

<span data-ttu-id="079a7-392">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-392">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="079a7-393">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="079a7-393">Parameters - alignControl</span></span>

<span data-ttu-id="079a7-394">値</span><span class="sxs-lookup"><span data-stu-id="079a7-394">value</span></span>  
<span data-ttu-id="079a7-395">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-395">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="079a7-396">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="079a7-396">Return Value - alignControl</span></span>

<span data-ttu-id="079a7-397">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="079a7-397">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="079a7-398">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="079a7-398">Remarks - alignControl</span></span>

<span data-ttu-id="079a7-399">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-399">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="079a7-400">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="079a7-400">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="079a7-401">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="079a7-401">Parameters - alignment</span></span>

<span data-ttu-id="079a7-402">値</span><span class="sxs-lookup"><span data-stu-id="079a7-402">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="079a7-403">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="079a7-403">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="079a7-404">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="079a7-404">Method allowEdit</span></span>

<span data-ttu-id="079a7-405">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-405">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="079a7-406">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="079a7-406">Parameters - allowEdit</span></span>

<span data-ttu-id="079a7-407">値</span><span class="sxs-lookup"><span data-stu-id="079a7-407">value</span></span>  
<span data-ttu-id="079a7-408">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="079a7-408">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="079a7-409">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="079a7-409">Return Value - allowEdit</span></span>

<span data-ttu-id="079a7-410">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-410">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="079a7-411">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="079a7-411">Remarks - allowEdit</span></span>

<span data-ttu-id="079a7-412">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="079a7-412">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="079a7-413">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="079a7-413">Method allowSysSetup</span></span>

<span data-ttu-id="079a7-414">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-414">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="079a7-415">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="079a7-415">Return Value - allowSysSetup</span></span>

<span data-ttu-id="079a7-416">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-416">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="079a7-417">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-417">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="079a7-418">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-418">Parameters - arrayIndex</span></span>

<span data-ttu-id="079a7-419">値</span><span class="sxs-lookup"><span data-stu-id="079a7-419">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="079a7-420">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-420">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="079a7-421">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="079a7-421">Method autoDeclaration</span></span>

<span data-ttu-id="079a7-422">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-422">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="079a7-423">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="079a7-423">Parameters - autoDeclaration</span></span>

<span data-ttu-id="079a7-424">値</span><span class="sxs-lookup"><span data-stu-id="079a7-424">value</span></span>  
<span data-ttu-id="079a7-425">プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="079a7-425">The value to assign to the property.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="079a7-426">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="079a7-426">Return Value - autoDeclaration</span></span>

<span data-ttu-id="079a7-427">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-427">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="079a7-428">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="079a7-428">Remarks - autoDeclaration</span></span>

<span data-ttu-id="079a7-429">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="079a7-429">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="079a7-430">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-430">Method backgroundColor</span></span>

<span data-ttu-id="079a7-431">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-431">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="079a7-432">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-432">Parameters - backgroundColor</span></span>

<span data-ttu-id="079a7-433">値</span><span class="sxs-lookup"><span data-stu-id="079a7-433">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="079a7-434">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-434">Return Value - backgroundColor</span></span>

<span data-ttu-id="079a7-435">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="079a7-435">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="079a7-436">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-436">Remarks - backgroundColor</span></span>

<span data-ttu-id="079a7-437">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="079a7-437">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="079a7-438">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="079a7-438">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="079a7-439">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="079a7-439">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="079a7-440">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="079a7-440">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="079a7-441">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="079a7-441">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="079a7-442">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="079a7-442">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="079a7-443">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="079a7-443">Method backStyle</span></span>

<span data-ttu-id="079a7-444">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-444">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="079a7-445">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="079a7-445">Parameters - backStyle</span></span>

<span data-ttu-id="079a7-446">値</span><span class="sxs-lookup"><span data-stu-id="079a7-446">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="079a7-447">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="079a7-447">Return Value - backStyle</span></span>

<span data-ttu-id="079a7-448">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="079a7-448">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="079a7-449">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="079a7-449">Method beginDrag</span></span>

<span data-ttu-id="079a7-450">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-450">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="079a7-451">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="079a7-451">Parameters - beginDrag</span></span>

<span data-ttu-id="079a7-452">x</span><span class="sxs-lookup"><span data-stu-id="079a7-452">x</span></span>  
<span data-ttu-id="079a7-453">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-453">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="079a7-454">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="079a7-454">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="079a7-455">y</span><span class="sxs-lookup"><span data-stu-id="079a7-455">y</span></span>  
<span data-ttu-id="079a7-456">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-456">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="079a7-457">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="079a7-457">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="079a7-458">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="079a7-458">Return Value - beginDrag</span></span>

<span data-ttu-id="079a7-459">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="079a7-459">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="079a7-460">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="079a7-460">Remarks - beginDrag</span></span>

<span data-ttu-id="079a7-461">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="079a7-461">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="079a7-462">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="079a7-462">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="079a7-463">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="079a7-463">Method bold</span></span>

<span data-ttu-id="079a7-464">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-464">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="079a7-465">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="079a7-465">Parameters - bold</span></span>

<span data-ttu-id="079a7-466">値</span><span class="sxs-lookup"><span data-stu-id="079a7-466">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="079a7-467">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="079a7-467">Return Value - bold</span></span>

<span data-ttu-id="079a7-468">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-468">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="079a7-469">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="079a7-469">Remarks - bold</span></span>

<span data-ttu-id="079a7-470">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="079a7-470">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="079a7-471">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="079a7-471">0 Use the default font weight.</span></span>
-   <span data-ttu-id="079a7-472">1 シン。</span><span class="sxs-lookup"><span data-stu-id="079a7-472">1 Thin.</span></span>
-   <span data-ttu-id="079a7-473">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="079a7-473">2 Extra-light.</span></span>
-   <span data-ttu-id="079a7-474">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="079a7-474">3 Light.</span></span>
-   <span data-ttu-id="079a7-475">4 標準。</span><span class="sxs-lookup"><span data-stu-id="079a7-475">4 Normal.</span></span>
-   <span data-ttu-id="079a7-476">5 中。</span><span class="sxs-lookup"><span data-stu-id="079a7-476">5 Medium.</span></span>
-   <span data-ttu-id="079a7-477">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="079a7-477">6 Semibold.</span></span>
-   <span data-ttu-id="079a7-478">7 太字。</span><span class="sxs-lookup"><span data-stu-id="079a7-478">7 Bold.</span></span>
-   <span data-ttu-id="079a7-479">8 極太。</span><span class="sxs-lookup"><span data-stu-id="079a7-479">8 Extra-bold.</span></span>
-   <span data-ttu-id="079a7-480">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="079a7-480">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="079a7-481">メソッド border</span><span class="sxs-lookup"><span data-stu-id="079a7-481">Method border</span></span>

<span data-ttu-id="079a7-482">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-482">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="079a7-483">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="079a7-483">Parameters - border</span></span>

<span data-ttu-id="079a7-484">値</span><span class="sxs-lookup"><span data-stu-id="079a7-484">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="079a7-485">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="079a7-485">Return Value - border</span></span>

<span data-ttu-id="079a7-486">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="079a7-486">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="079a7-487">備考 - border</span><span class="sxs-lookup"><span data-stu-id="079a7-487">Remarks - border</span></span>

<span data-ttu-id="079a7-488">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="079a7-488">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="079a7-489">値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-489">Value.</span></span> | <span data-ttu-id="079a7-490">説明。</span><span class="sxs-lookup"><span data-stu-id="079a7-490">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="079a7-491">0</span><span class="sxs-lookup"><span data-stu-id="079a7-491">0</span></span>      | <span data-ttu-id="079a7-492">自動。</span><span class="sxs-lookup"><span data-stu-id="079a7-492">Auto.</span></span>        |
| <span data-ttu-id="079a7-493">1</span><span class="sxs-lookup"><span data-stu-id="079a7-493">1</span></span>      | <span data-ttu-id="079a7-494">3D。</span><span class="sxs-lookup"><span data-stu-id="079a7-494">3D.</span></span>          |
| <span data-ttu-id="079a7-495">2</span><span class="sxs-lookup"><span data-stu-id="079a7-495">2</span></span>      | <span data-ttu-id="079a7-496">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="079a7-496">Single line.</span></span> |
| <span data-ttu-id="079a7-497">3</span><span class="sxs-lookup"><span data-stu-id="079a7-497">3</span></span>      | <span data-ttu-id="079a7-498">均一。</span><span class="sxs-lookup"><span data-stu-id="079a7-498">Flat.</span></span>        |
| <span data-ttu-id="079a7-499">4</span><span class="sxs-lookup"><span data-stu-id="079a7-499">4</span></span>      | <span data-ttu-id="079a7-500">なし。</span><span class="sxs-lookup"><span data-stu-id="079a7-500">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="079a7-501">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-501">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="079a7-502">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-502">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="079a7-503">値</span><span class="sxs-lookup"><span data-stu-id="079a7-503">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="079a7-504">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-504">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="079a7-505">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="079a7-505">Method calcControlSize</span></span>

<span data-ttu-id="079a7-506">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-506">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="079a7-507">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="079a7-507">Parameters - calcControlSize</span></span>

<span data-ttu-id="079a7-508">chars</span><span class="sxs-lookup"><span data-stu-id="079a7-508">chars</span></span>  
<span data-ttu-id="079a7-509">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="079a7-509">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="079a7-510">明細行</span><span class="sxs-lookup"><span data-stu-id="079a7-510">lines</span></span>  
<span data-ttu-id="079a7-511">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="079a7-511">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="079a7-512">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="079a7-512">Return Value - calcControlSize</span></span>

<span data-ttu-id="079a7-513">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="079a7-513">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="079a7-514">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="079a7-514">Method characterSet</span></span>

<span data-ttu-id="079a7-515">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-515">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="079a7-516">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="079a7-516">Parameters - characterSet</span></span>

<span data-ttu-id="079a7-517">値</span><span class="sxs-lookup"><span data-stu-id="079a7-517">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="079a7-518">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="079a7-518">Return Value - characterSet</span></span>

<span data-ttu-id="079a7-519">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-519">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="079a7-520">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="079a7-520">Remarks - characterSet</span></span>

<span data-ttu-id="079a7-521">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-521">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="079a7-522">値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-522">Value.</span></span> | <span data-ttu-id="079a7-523">説明。</span><span class="sxs-lookup"><span data-stu-id="079a7-523">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="079a7-524">0</span><span class="sxs-lookup"><span data-stu-id="079a7-524">0</span></span>      | <span data-ttu-id="079a7-525">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-525">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="079a7-526">1</span><span class="sxs-lookup"><span data-stu-id="079a7-526">1</span></span>      | <span data-ttu-id="079a7-527">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-527">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="079a7-528">2</span><span class="sxs-lookup"><span data-stu-id="079a7-528">2</span></span>      | <span data-ttu-id="079a7-529">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-529">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="079a7-530">77</span><span class="sxs-lookup"><span data-stu-id="079a7-530">77</span></span>     | <span data-ttu-id="079a7-531">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-531">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="079a7-532">128</span><span class="sxs-lookup"><span data-stu-id="079a7-532">128</span></span>    | <span data-ttu-id="079a7-533">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-533">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="079a7-534">129</span><span class="sxs-lookup"><span data-stu-id="079a7-534">129</span></span>    | <span data-ttu-id="079a7-535">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-535">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="079a7-536">134</span><span class="sxs-lookup"><span data-stu-id="079a7-536">134</span></span>    | <span data-ttu-id="079a7-537">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-537">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="079a7-538">136</span><span class="sxs-lookup"><span data-stu-id="079a7-538">136</span></span>    | <span data-ttu-id="079a7-539">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-539">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="079a7-540">161</span><span class="sxs-lookup"><span data-stu-id="079a7-540">161</span></span>    | <span data-ttu-id="079a7-541">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-541">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="079a7-542">162</span><span class="sxs-lookup"><span data-stu-id="079a7-542">162</span></span>    | <span data-ttu-id="079a7-543">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-543">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="079a7-544">163</span><span class="sxs-lookup"><span data-stu-id="079a7-544">163</span></span>    | <span data-ttu-id="079a7-545">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-545">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="079a7-546">186</span><span class="sxs-lookup"><span data-stu-id="079a7-546">186</span></span>    | <span data-ttu-id="079a7-547">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-547">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="079a7-548">204</span><span class="sxs-lookup"><span data-stu-id="079a7-548">204</span></span>    | <span data-ttu-id="079a7-549">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-549">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="079a7-550">238</span><span class="sxs-lookup"><span data-stu-id="079a7-550">238</span></span>    | <span data-ttu-id="079a7-551">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-551">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="079a7-552">255</span><span class="sxs-lookup"><span data-stu-id="079a7-552">255</span></span>    | <span data-ttu-id="079a7-553">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-553">OEM\_CHARSET</span></span>         |

<span data-ttu-id="079a7-554">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-554">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="079a7-555">値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-555">Value.</span></span> | <span data-ttu-id="079a7-556">説明。</span><span class="sxs-lookup"><span data-stu-id="079a7-556">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="079a7-557">130</span><span class="sxs-lookup"><span data-stu-id="079a7-557">130</span></span>    | <span data-ttu-id="079a7-558">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-558">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="079a7-559">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-559">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="079a7-560">値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-560">Value.</span></span> | <span data-ttu-id="079a7-561">説明。</span><span class="sxs-lookup"><span data-stu-id="079a7-561">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="079a7-562">177</span><span class="sxs-lookup"><span data-stu-id="079a7-562">177</span></span>    | <span data-ttu-id="079a7-563">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-563">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="079a7-564">178</span><span class="sxs-lookup"><span data-stu-id="079a7-564">178</span></span>    | <span data-ttu-id="079a7-565">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-565">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="079a7-566">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-566">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="079a7-567">値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-567">Value.</span></span> | <span data-ttu-id="079a7-568">説明。</span><span class="sxs-lookup"><span data-stu-id="079a7-568">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="079a7-569">222</span><span class="sxs-lookup"><span data-stu-id="079a7-569">222</span></span>    | <span data-ttu-id="079a7-570">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="079a7-570">THAI\_CHARSET</span></span> |

<span data-ttu-id="079a7-571">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-571">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="079a7-572">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-572">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="079a7-573">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="079a7-573">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-charfrompos"></a><span data-ttu-id="079a7-574">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="079a7-574">Method charFromPos</span></span>

```xpp
public int charFromPos(int x, int y)
```

### <a name="parameters---charfrompos"></a><span data-ttu-id="079a7-575">パラメーター - charFromPos</span><span class="sxs-lookup"><span data-stu-id="079a7-575">Parameters - charFromPos</span></span>

<span data-ttu-id="079a7-576">x</span><span class="sxs-lookup"><span data-stu-id="079a7-576">x</span></span>  

<!-- -->

<span data-ttu-id="079a7-577">y</span><span class="sxs-lookup"><span data-stu-id="079a7-577">y</span></span>  

### <a name="return-value---charfrompos"></a><span data-ttu-id="079a7-578">戻り値 - charFromPos</span><span class="sxs-lookup"><span data-stu-id="079a7-578">Return Value - charFromPos</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="079a7-579">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="079a7-579">Method colorScheme</span></span>

<span data-ttu-id="079a7-580">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-580">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="079a7-581">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="079a7-581">Parameters - colorScheme</span></span>

<span data-ttu-id="079a7-582">値</span><span class="sxs-lookup"><span data-stu-id="079a7-582">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="079a7-583">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="079a7-583">Return Value - colorScheme</span></span>

<span data-ttu-id="079a7-584">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="079a7-584">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="079a7-585">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="079a7-585">Remarks - colorScheme</span></span>

<span data-ttu-id="079a7-586">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-586">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="079a7-587">値です。</span><span class="sxs-lookup"><span data-stu-id="079a7-587">Value.</span></span> | <span data-ttu-id="079a7-588">スタイル。</span><span class="sxs-lookup"><span data-stu-id="079a7-588">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="079a7-589">0</span><span class="sxs-lookup"><span data-stu-id="079a7-589">0</span></span>      | <span data-ttu-id="079a7-590">既定。</span><span class="sxs-lookup"><span data-stu-id="079a7-590">Default.</span></span>               |
| <span data-ttu-id="079a7-591">1</span><span class="sxs-lookup"><span data-stu-id="079a7-591">1</span></span>      | <span data-ttu-id="079a7-592">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="079a7-592">The Windows palette.</span></span>   |
| <span data-ttu-id="079a7-593">2</span><span class="sxs-lookup"><span data-stu-id="079a7-593">2</span></span>      | <span data-ttu-id="079a7-594">真の配色。</span><span class="sxs-lookup"><span data-stu-id="079a7-594">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="079a7-595">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="079a7-595">Method configurationKey</span></span>

<span data-ttu-id="079a7-596">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-596">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="079a7-597">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="079a7-597">Parameters - configurationKey</span></span>

<span data-ttu-id="079a7-598">値</span><span class="sxs-lookup"><span data-stu-id="079a7-598">value</span></span>  
<span data-ttu-id="079a7-599">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-599">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="079a7-600">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="079a7-600">Return Value - configurationKey</span></span>

<span data-ttu-id="079a7-601">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="079a7-601">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="079a7-602">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="079a7-602">Remarks - configurationKey</span></span>

<span data-ttu-id="079a7-603">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-603">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="079a7-604">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="079a7-604">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="079a7-605">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="079a7-605">Method configurationKeyEx</span></span>

<span data-ttu-id="079a7-606">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-606">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="079a7-607">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="079a7-607">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="079a7-608">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="079a7-608">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="079a7-609">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="079a7-609">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="079a7-610">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="079a7-610">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="079a7-611">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="079a7-611">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="079a7-612">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="079a7-612">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="079a7-613">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="079a7-613">Method countryRegionCodes</span></span>

<span data-ttu-id="079a7-614">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-614">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="079a7-615">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="079a7-615">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="079a7-616">値</span><span class="sxs-lookup"><span data-stu-id="079a7-616">value</span></span>  
<span data-ttu-id="079a7-617">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-617">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="079a7-618">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="079a7-618">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="079a7-619">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="079a7-619">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="079a7-620">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="079a7-620">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="079a7-621">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="079a7-621">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="079a7-622">値</span><span class="sxs-lookup"><span data-stu-id="079a7-622">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="079a7-623">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="079a7-623">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="079a7-624">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="079a7-624">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="079a7-625">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="079a7-625">Parameters - dataField</span></span>

<span data-ttu-id="079a7-626">値</span><span class="sxs-lookup"><span data-stu-id="079a7-626">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="079a7-627">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="079a7-627">Return Value - dataField</span></span>

## <a name="method-datafieldarrayindex"></a><span data-ttu-id="079a7-628">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-628">Method dataFieldArrayIndex</span></span>

```xpp
public int dataFieldArrayIndex()
```

### <a name="return-value---datafieldarrayindex"></a><span data-ttu-id="079a7-629">戻り値 - dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-629">Return Value - dataFieldArrayIndex</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="079a7-630">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="079a7-630">Method dataFieldName</span></span>

```xpp
public FieldName dataFieldName()
```

### <a name="return-value---datafieldname"></a><span data-ttu-id="079a7-631">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="079a7-631">Return Value - dataFieldName</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="079a7-632">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-632">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="079a7-633">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-633">Parameters - dataMethod</span></span>

<span data-ttu-id="079a7-634">値</span><span class="sxs-lookup"><span data-stu-id="079a7-634">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="079a7-635">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-635">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="079a7-636">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="079a7-636">Method dataRelationPath</span></span>

<span data-ttu-id="079a7-637">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-637">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="079a7-638">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="079a7-638">Parameters - dataRelationPath</span></span>

<span data-ttu-id="079a7-639">値</span><span class="sxs-lookup"><span data-stu-id="079a7-639">value</span></span>  
<span data-ttu-id="079a7-640">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-640">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="079a7-641">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="079a7-641">Return Value - dataRelationPath</span></span>

<span data-ttu-id="079a7-642">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="079a7-642">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="079a7-643">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="079a7-643">Remarks - dataRelationPath</span></span>

<span data-ttu-id="079a7-644">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="079a7-644">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="079a7-645">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="079a7-645">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="079a7-646">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="079a7-646">Method dataSource</span></span>

<span data-ttu-id="079a7-647">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-647">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="079a7-648">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="079a7-648">Parameters - dataSource</span></span>

<span data-ttu-id="079a7-649">値</span><span class="sxs-lookup"><span data-stu-id="079a7-649">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="079a7-650">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="079a7-650">Return Value - dataSource</span></span>

<span data-ttu-id="079a7-651">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="079a7-651">The identifier of the data source to be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="079a7-652">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="079a7-652">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="079a7-653">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="079a7-653">Parameters - direction</span></span>

<span data-ttu-id="079a7-654">値</span><span class="sxs-lookup"><span data-stu-id="079a7-654">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="079a7-655">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="079a7-655">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="079a7-656">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-656">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="079a7-657">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-657">Parameters - displayHeight</span></span>

<span data-ttu-id="079a7-658">値</span><span class="sxs-lookup"><span data-stu-id="079a7-658">value</span></span>  

<!-- -->

<span data-ttu-id="079a7-659">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-659">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="079a7-660">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-660">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="079a7-661">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-661">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="079a7-662">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-662">Parameters - displayHeightMode</span></span>

<span data-ttu-id="079a7-663">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-663">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="079a7-664">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-664">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="079a7-665">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-665">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="079a7-666">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-666">Parameters - displayHeightValue</span></span>

<span data-ttu-id="079a7-667">値</span><span class="sxs-lookup"><span data-stu-id="079a7-667">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="079a7-668">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-668">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="079a7-669">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="079a7-669">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="079a7-670">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="079a7-670">Parameters - displayLength</span></span>

<span data-ttu-id="079a7-671">値</span><span class="sxs-lookup"><span data-stu-id="079a7-671">value</span></span>  

<!-- -->

<span data-ttu-id="079a7-672">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-672">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="079a7-673">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="079a7-673">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="079a7-674">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-674">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="079a7-675">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-675">Parameters - displayLengthMode</span></span>

<span data-ttu-id="079a7-676">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-676">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="079a7-677">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-677">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="079a7-678">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-678">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="079a7-679">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-679">Parameters - displayLengthValue</span></span>

<span data-ttu-id="079a7-680">値</span><span class="sxs-lookup"><span data-stu-id="079a7-680">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="079a7-681">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-681">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="079a7-682">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="079a7-682">Method displayTarget</span></span>

<span data-ttu-id="079a7-683">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-683">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="079a7-684">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="079a7-684">Parameters - displayTarget</span></span>

<span data-ttu-id="079a7-685">値</span><span class="sxs-lookup"><span data-stu-id="079a7-685">value</span></span>  
<span data-ttu-id="079a7-686">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-686">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="079a7-687">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="079a7-687">Return Value - displayTarget</span></span>

<span data-ttu-id="079a7-688">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="079a7-688">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="079a7-689">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="079a7-689">Method dragDrop</span></span>

<span data-ttu-id="079a7-690">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-690">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="079a7-691">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="079a7-691">Parameters - dragDrop</span></span>

<span data-ttu-id="079a7-692">値</span><span class="sxs-lookup"><span data-stu-id="079a7-692">value</span></span>  
<span data-ttu-id="079a7-693">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-693">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="079a7-694">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="079a7-694">Return Value - dragDrop</span></span>

<span data-ttu-id="079a7-695">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="079a7-695">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="079a7-696">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="079a7-696">Remarks - dragDrop</span></span>

<span data-ttu-id="079a7-697">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-697">Use the dragLeave, the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="079a7-698">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="079a7-698">Method dragOver</span></span>

<span data-ttu-id="079a7-699">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-699">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="079a7-700">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="079a7-700">Parameters - dragOver</span></span>

<span data-ttu-id="079a7-701">dragSource</span><span class="sxs-lookup"><span data-stu-id="079a7-701">dragSource</span></span>  
<span data-ttu-id="079a7-702">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-702">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-703">dragMode</span><span class="sxs-lookup"><span data-stu-id="079a7-703">dragMode</span></span>  
<span data-ttu-id="079a7-704">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-704">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-705">x</span><span class="sxs-lookup"><span data-stu-id="079a7-705">x</span></span>  
<span data-ttu-id="079a7-706">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-706">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-707">y</span><span class="sxs-lookup"><span data-stu-id="079a7-707">y</span></span>  
<span data-ttu-id="079a7-708">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-708">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="079a7-709">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="079a7-709">Return Value - dragOver</span></span>

<span data-ttu-id="079a7-710">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="079a7-710">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="079a7-711">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="079a7-711">Method dragOverEx</span></span>

<span data-ttu-id="079a7-712">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-712">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="079a7-713">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="079a7-713">Parameters - dragOverEx</span></span>

<span data-ttu-id="079a7-714">dragSource</span><span class="sxs-lookup"><span data-stu-id="079a7-714">dragSource</span></span>  
<span data-ttu-id="079a7-715">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-715">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-716">dragMode</span><span class="sxs-lookup"><span data-stu-id="079a7-716">dragMode</span></span>  
<span data-ttu-id="079a7-717">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-717">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-718">x</span><span class="sxs-lookup"><span data-stu-id="079a7-718">x</span></span>  
<span data-ttu-id="079a7-719">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-719">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-720">y</span><span class="sxs-lookup"><span data-stu-id="079a7-720">y</span></span>  
<span data-ttu-id="079a7-721">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-721">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="079a7-722">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="079a7-722">Return Value - dragOverEx</span></span>

<span data-ttu-id="079a7-723">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="079a7-723">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="079a7-724">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="079a7-724">Method dragText</span></span>

<span data-ttu-id="079a7-725">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-725">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="079a7-726">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="079a7-726">Return Value - dragText</span></span>

<span data-ttu-id="079a7-727">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="079a7-727">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="079a7-728">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="079a7-728">Method enabled</span></span>

<span data-ttu-id="079a7-729">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-729">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="079a7-730">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="079a7-730">Parameters - enabled</span></span>

<span data-ttu-id="079a7-731">値</span><span class="sxs-lookup"><span data-stu-id="079a7-731">value</span></span>  
<span data-ttu-id="079a7-732">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-732">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="079a7-733">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="079a7-733">Return Value - enabled</span></span>

<span data-ttu-id="079a7-734">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-734">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="079a7-735">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="079a7-735">Remarks - enabled</span></span>

<span data-ttu-id="079a7-736">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="079a7-736">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="079a7-737">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="079a7-737">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="079a7-738">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="079a7-738">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="079a7-739">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="079a7-739">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="079a7-740">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="079a7-740">Parameters - extendedDataType</span></span>

<span data-ttu-id="079a7-741">値</span><span class="sxs-lookup"><span data-stu-id="079a7-741">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="079a7-742">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="079a7-742">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="079a7-743">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="079a7-743">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="079a7-744">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="079a7-744">Parameters - fastTabSummary</span></span>

<span data-ttu-id="079a7-745">値</span><span class="sxs-lookup"><span data-stu-id="079a7-745">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="079a7-746">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="079a7-746">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="079a7-747">メソッド font</span><span class="sxs-lookup"><span data-stu-id="079a7-747">Method font</span></span>

<span data-ttu-id="079a7-748">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-748">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="079a7-749">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="079a7-749">Parameters - font</span></span>

<span data-ttu-id="079a7-750">値</span><span class="sxs-lookup"><span data-stu-id="079a7-750">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="079a7-751">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="079a7-751">Return Value - font</span></span>

<span data-ttu-id="079a7-752">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="079a7-752">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="079a7-753">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="079a7-753">Method fontSize</span></span>

<span data-ttu-id="079a7-754">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-754">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="079a7-755">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="079a7-755">Parameters - fontSize</span></span>

<span data-ttu-id="079a7-756">値</span><span class="sxs-lookup"><span data-stu-id="079a7-756">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="079a7-757">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="079a7-757">Return Value - fontSize</span></span>

<span data-ttu-id="079a7-758">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="079a7-758">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="079a7-759">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-759">Method foregroundColor</span></span>

<span data-ttu-id="079a7-760">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-760">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="079a7-761">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-761">Parameters - foregroundColor</span></span>

<span data-ttu-id="079a7-762">値</span><span class="sxs-lookup"><span data-stu-id="079a7-762">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="079a7-763">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-763">Return Value - foregroundColor</span></span>

<span data-ttu-id="079a7-764">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="079a7-764">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="079a7-765">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-765">Remarks - foregroundColor</span></span>

<span data-ttu-id="079a7-766">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="079a7-766">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="079a7-767">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="079a7-767">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="079a7-768">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="079a7-768">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="079a7-769">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="079a7-769">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="079a7-770">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="079a7-770">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="079a7-771">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="079a7-771">The maximum value for a single byte is 255.</span></span>

## <a name="method-getcursorpos"></a><span data-ttu-id="079a7-772">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="079a7-772">Method getCursorPos</span></span>

```xpp
public container getCursorPos()
```

### <a name="return-value---getcursorpos"></a><span data-ttu-id="079a7-773">戻り値 - getCursorPos</span><span class="sxs-lookup"><span data-stu-id="079a7-773">Return Value - getCursorPos</span></span>

## <a name="method-getfirstvisibleline"></a><span data-ttu-id="079a7-774">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="079a7-774">Method getFirstVisibleLine</span></span>

```xpp
public int getFirstVisibleLine()
```

### <a name="return-value---getfirstvisibleline"></a><span data-ttu-id="079a7-775">戻り値 - getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="079a7-775">Return Value - getFirstVisibleLine</span></span>

## <a name="method-getline"></a><span data-ttu-id="079a7-776">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="079a7-776">Method getLine</span></span>

```xpp
public str getLine(int lineNo)
```

### <a name="parameters---getline"></a><span data-ttu-id="079a7-777">パラメーター - getLine</span><span class="sxs-lookup"><span data-stu-id="079a7-777">Parameters - getLine</span></span>

<span data-ttu-id="079a7-778">lineNo</span><span class="sxs-lookup"><span data-stu-id="079a7-778">lineNo</span></span>  

### <a name="return-value---getline"></a><span data-ttu-id="079a7-779">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="079a7-779">Return Value - getLine</span></span>

## <a name="method-getlinecount"></a><span data-ttu-id="079a7-780">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="079a7-780">Method getLineCount</span></span>

```xpp
public int getLineCount()
```

### <a name="return-value---getlinecount"></a><span data-ttu-id="079a7-781">戻り値 - getLineCount</span><span class="sxs-lookup"><span data-stu-id="079a7-781">Return Value - getLineCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="079a7-782">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="079a7-782">Method getSelection</span></span>

```xpp
public container getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="079a7-783">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="079a7-783">Return Value - getSelection</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="079a7-784">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="079a7-784">Method hasChanged</span></span>

<span data-ttu-id="079a7-785">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-785">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="079a7-786">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="079a7-786">Parameters - hasChanged</span></span>

<span data-ttu-id="079a7-787">val</span><span class="sxs-lookup"><span data-stu-id="079a7-787">val</span></span>  
<span data-ttu-id="079a7-788">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-788">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="079a7-789">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="079a7-789">Return Value - hasChanged</span></span>

<span data-ttu-id="079a7-790">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-790">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="079a7-791">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="079a7-791">Method hasUserSetting</span></span>

<span data-ttu-id="079a7-792">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-792">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="079a7-793">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="079a7-793">Return Value - hasUserSetting</span></span>

<span data-ttu-id="079a7-794">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-794">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="079a7-795">メソッド height</span><span class="sxs-lookup"><span data-stu-id="079a7-795">Method height</span></span>

<span data-ttu-id="079a7-796">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-796">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="079a7-797">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="079a7-797">Parameters - height</span></span>

<span data-ttu-id="079a7-798">値</span><span class="sxs-lookup"><span data-stu-id="079a7-798">value</span></span>  
<span data-ttu-id="079a7-799">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-799">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="079a7-800">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-800">mode</span></span>  
<span data-ttu-id="079a7-801">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-801">An Integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="079a7-802">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="079a7-802">Return Value - height</span></span>

<span data-ttu-id="079a7-803">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="079a7-803">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="079a7-804">備考 - height</span><span class="sxs-lookup"><span data-stu-id="079a7-804">Remarks - height</span></span>

<span data-ttu-id="079a7-805">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-805">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="079a7-806">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="079a7-806">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="079a7-807">モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-807">Mode.</span></span>            | <span data-ttu-id="079a7-808">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="079a7-808">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="079a7-809">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="079a7-809">-1 Exact.</span></span>        | <span data-ttu-id="079a7-810">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-810">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="079a7-811">0 自動。</span><span class="sxs-lookup"><span data-stu-id="079a7-811">0 Auto.</span></span>          | <span data-ttu-id="079a7-812">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-812">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="079a7-813">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="079a7-813">1 Column height.</span></span> | <span data-ttu-id="079a7-814">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="079a7-814">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="079a7-815">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="079a7-815">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="079a7-816">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-816">Method heightMode</span></span>

<span data-ttu-id="079a7-817">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-817">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="079a7-818">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-818">Parameters - heightMode</span></span>

<span data-ttu-id="079a7-819">値</span><span class="sxs-lookup"><span data-stu-id="079a7-819">value</span></span>  
<span data-ttu-id="079a7-820">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-820">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="079a7-821">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-821">Return Value - heightMode</span></span>

<span data-ttu-id="079a7-822">計算モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-822">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="079a7-823">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-823">Remarks - heightMode</span></span>

<span data-ttu-id="079a7-824">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="079a7-824">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="079a7-825">モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-825">Mode.</span></span>          | <span data-ttu-id="079a7-826">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="079a7-826">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="079a7-827">正確。</span><span class="sxs-lookup"><span data-stu-id="079a7-827">Exact.</span></span>         | <span data-ttu-id="079a7-828">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-828">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="079a7-829">自動。</span><span class="sxs-lookup"><span data-stu-id="079a7-829">Auto.</span></span>          | <span data-ttu-id="079a7-830">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-830">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="079a7-831">列の高さ</span><span class="sxs-lookup"><span data-stu-id="079a7-831">Column height.</span></span> | <span data-ttu-id="079a7-832">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="079a7-832">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="079a7-833">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="079a7-833">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="079a7-834">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-834">Method heightValue</span></span>

<span data-ttu-id="079a7-835">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-835">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="079a7-836">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-836">Parameters - heightValue</span></span>

<span data-ttu-id="079a7-837">値</span><span class="sxs-lookup"><span data-stu-id="079a7-837">value</span></span>  
<span data-ttu-id="079a7-838">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-838">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="079a7-839">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-839">Return Value - heightValue</span></span>

<span data-ttu-id="079a7-840">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="079a7-840">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="079a7-841">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-841">Remarks - heightValue</span></span>

<span data-ttu-id="079a7-842">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="079a7-842">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="079a7-843">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="079a7-843">Method helpField</span></span>

<span data-ttu-id="079a7-844">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-844">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="079a7-845">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="079a7-845">Return Value - helpField</span></span>

<span data-ttu-id="079a7-846">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="079a7-846">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="079a7-847">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="079a7-847">Remarks - helpField</span></span>

<span data-ttu-id="079a7-848">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="079a7-848">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="079a7-849">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="079a7-849">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="079a7-850">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="079a7-850">Method helpText</span></span>

<span data-ttu-id="079a7-851">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-851">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="079a7-852">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="079a7-852">Parameters - helpText</span></span>

<span data-ttu-id="079a7-853">値</span><span class="sxs-lookup"><span data-stu-id="079a7-853">value</span></span>  
<span data-ttu-id="079a7-854">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="079a7-854">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="079a7-855">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="079a7-855">Return Value - helpText</span></span>

<span data-ttu-id="079a7-856">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="079a7-856">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="079a7-857">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="079a7-857">Remarks - helpText</span></span>

<span data-ttu-id="079a7-858">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-858">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="079a7-859">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="079a7-859">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="079a7-860">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="079a7-860">Method hierarchyParent</span></span>

<span data-ttu-id="079a7-861">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-861">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="079a7-862">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="079a7-862">Parameters - hierarchyParent</span></span>

<span data-ttu-id="079a7-863">値</span><span class="sxs-lookup"><span data-stu-id="079a7-863">value</span></span>  
<span data-ttu-id="079a7-864">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="079a7-864">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="079a7-865">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="079a7-865">Return Value - hierarchyParent</span></span>

<span data-ttu-id="079a7-866">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="079a7-866">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="079a7-867">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="079a7-867">Method hWnd</span></span>

<span data-ttu-id="079a7-868">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-868">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="079a7-869">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="079a7-869">Return Value - hWnd</span></span>

<span data-ttu-id="079a7-870">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="079a7-870">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="079a7-871">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="079a7-871">Remarks - hWnd</span></span>

<span data-ttu-id="079a7-872">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="079a7-872">The handle can be used with the Windows API.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="079a7-873">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="079a7-873">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="079a7-874">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="079a7-874">Parameters - iMEMode</span></span>

<span data-ttu-id="079a7-875">値</span><span class="sxs-lookup"><span data-stu-id="079a7-875">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="079a7-876">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="079a7-876">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="079a7-877">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="079a7-877">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="079a7-878">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="079a7-878">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="079a7-879">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="079a7-879">Method isDisplayed</span></span>

<span data-ttu-id="079a7-880">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-880">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="079a7-881">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="079a7-881">Return Value - isDisplayed</span></span>

<span data-ttu-id="079a7-882">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="079a7-882">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="079a7-883">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="079a7-883">Remarks - isDisplayed</span></span>

<span data-ttu-id="079a7-884">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="079a7-884">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="079a7-885">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="079a7-885">Method isRestricted</span></span>

<span data-ttu-id="079a7-886">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-886">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="079a7-887">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="079a7-887">Return Value - isRestricted</span></span>

<span data-ttu-id="079a7-888">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="079a7-888">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="079a7-889">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="079a7-889">Method isUserSetupEnabled</span></span>

<span data-ttu-id="079a7-890">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-890">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="079a7-891">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="079a7-891">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="079a7-892">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="079a7-892">neededSetupRights</span></span>  
<span data-ttu-id="079a7-893">コントロールに要求されているカスタマイズのレベルを指定する FormAllowUserSetup 列挙値。</span><span class="sxs-lookup"><span data-stu-id="079a7-893">A FormAllowUserSetup enumeration value that specifies the level of customization that is being requested for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="079a7-894">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="079a7-894">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="079a7-895">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-895">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="079a7-896">「true」を返すこのメソッドについては、デザインおよびすべての親コンテナの AllowUserSetup プロパティが少なくとも neededSetupRights パラメータで指定されたレベル以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="079a7-896">For this method to return true, the AllowUserSetup property for the design and all parent containers must be at least as high as the level that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="079a7-897">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="079a7-897">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="079a7-898">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="079a7-898">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="079a7-899">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="079a7-899">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="079a7-900">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="079a7-900">No changes can be made to the control.</span></span> <span data-ttu-id="079a7-901">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-901">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="079a7-902">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="079a7-902">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="079a7-903">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="079a7-903">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="079a7-904">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="079a7-904">The user cannot move the control.</span></span>   |
| <span data-ttu-id="079a7-905">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="079a7-905">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="079a7-906">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="079a7-906">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="079a7-907">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="079a7-907">The user can also move the control.</span></span> |

## <a name="method-isvalid"></a><span data-ttu-id="079a7-908">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="079a7-908">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="079a7-909">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="079a7-909">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="079a7-910">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="079a7-910">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="079a7-911">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="079a7-911">Parameters - italic</span></span>

<span data-ttu-id="079a7-912">値</span><span class="sxs-lookup"><span data-stu-id="079a7-912">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="079a7-913">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="079a7-913">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="079a7-914">メソッド label</span><span class="sxs-lookup"><span data-stu-id="079a7-914">Method label</span></span>

<span data-ttu-id="079a7-915">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-915">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="079a7-916">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="079a7-916">Parameters - label</span></span>

<span data-ttu-id="079a7-917">値</span><span class="sxs-lookup"><span data-stu-id="079a7-917">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="079a7-918">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="079a7-918">Return Value - label</span></span>

<span data-ttu-id="079a7-919">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="079a7-919">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="079a7-920">備考 - label</span><span class="sxs-lookup"><span data-stu-id="079a7-920">Remarks - label</span></span>

<span data-ttu-id="079a7-921">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-921">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="079a7-922">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="079a7-922">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="079a7-923">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="079a7-923">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="079a7-924">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="079a7-924">Parameters - labelAlignment</span></span>

<span data-ttu-id="079a7-925">値</span><span class="sxs-lookup"><span data-stu-id="079a7-925">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="079a7-926">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="079a7-926">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="079a7-927">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="079a7-927">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="079a7-928">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="079a7-928">Parameters - labelBold</span></span>

<span data-ttu-id="079a7-929">値</span><span class="sxs-lookup"><span data-stu-id="079a7-929">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="079a7-930">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="079a7-930">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="079a7-931">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="079a7-931">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="079a7-932">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="079a7-932">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="079a7-933">値</span><span class="sxs-lookup"><span data-stu-id="079a7-933">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="079a7-934">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="079a7-934">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="079a7-935">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="079a7-935">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="079a7-936">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="079a7-936">Parameters - labelFont</span></span>

<span data-ttu-id="079a7-937">値</span><span class="sxs-lookup"><span data-stu-id="079a7-937">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="079a7-938">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="079a7-938">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="079a7-939">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="079a7-939">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="079a7-940">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="079a7-940">Parameters - labelFontSize</span></span>

<span data-ttu-id="079a7-941">値</span><span class="sxs-lookup"><span data-stu-id="079a7-941">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="079a7-942">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="079a7-942">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="079a7-943">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-943">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="079a7-944">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-944">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="079a7-945">値</span><span class="sxs-lookup"><span data-stu-id="079a7-945">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="079a7-946">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="079a7-946">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="079a7-947">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="079a7-947">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="079a7-948">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="079a7-948">Parameters - labelGuide</span></span>

<span data-ttu-id="079a7-949">値</span><span class="sxs-lookup"><span data-stu-id="079a7-949">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="079a7-950">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="079a7-950">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="079a7-951">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-951">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="079a7-952">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-952">Parameters - labelHeight</span></span>

<span data-ttu-id="079a7-953">値</span><span class="sxs-lookup"><span data-stu-id="079a7-953">value</span></span>  

<!-- -->

<span data-ttu-id="079a7-954">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-954">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="079a7-955">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-955">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="079a7-956">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-956">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="079a7-957">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-957">Parameters - labelHeightMode</span></span>

<span data-ttu-id="079a7-958">値</span><span class="sxs-lookup"><span data-stu-id="079a7-958">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="079a7-959">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="079a7-959">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="079a7-960">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-960">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="079a7-961">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-961">Parameters - labelHeightValue</span></span>

<span data-ttu-id="079a7-962">値</span><span class="sxs-lookup"><span data-stu-id="079a7-962">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="079a7-963">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="079a7-963">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="079a7-964">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="079a7-964">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="079a7-965">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="079a7-965">Parameters - labelItalic</span></span>

<span data-ttu-id="079a7-966">値</span><span class="sxs-lookup"><span data-stu-id="079a7-966">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="079a7-967">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="079a7-967">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="079a7-968">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="079a7-968">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="079a7-969">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="079a7-969">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="079a7-970">x</span><span class="sxs-lookup"><span data-stu-id="079a7-970">x</span></span>  

<!-- -->

<span data-ttu-id="079a7-971">y</span><span class="sxs-lookup"><span data-stu-id="079a7-971">y</span></span>  

<!-- -->

<span data-ttu-id="079a7-972">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-972">button</span></span>  

<!-- -->

<span data-ttu-id="079a7-973">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-973">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="079a7-974">Shift</span><span class="sxs-lookup"><span data-stu-id="079a7-974">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="079a7-975">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="079a7-975">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="079a7-976">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="079a7-976">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="079a7-977">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="079a7-977">Parameters - labelMouseDown</span></span>

<span data-ttu-id="079a7-978">x</span><span class="sxs-lookup"><span data-stu-id="079a7-978">x</span></span>  

<!-- -->

<span data-ttu-id="079a7-979">y</span><span class="sxs-lookup"><span data-stu-id="079a7-979">y</span></span>  

<!-- -->

<span data-ttu-id="079a7-980">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-980">button</span></span>  

<!-- -->

<span data-ttu-id="079a7-981">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-981">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="079a7-982">Shift</span><span class="sxs-lookup"><span data-stu-id="079a7-982">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="079a7-983">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="079a7-983">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="079a7-984">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="079a7-984">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="079a7-985">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="079a7-985">Parameters - labelMouseUp</span></span>

<span data-ttu-id="079a7-986">x</span><span class="sxs-lookup"><span data-stu-id="079a7-986">x</span></span>  

<!-- -->

<span data-ttu-id="079a7-987">y</span><span class="sxs-lookup"><span data-stu-id="079a7-987">y</span></span>  

<!-- -->

<span data-ttu-id="079a7-988">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-988">button</span></span>  

<!-- -->

<span data-ttu-id="079a7-989">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-989">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="079a7-990">Shift</span><span class="sxs-lookup"><span data-stu-id="079a7-990">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="079a7-991">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="079a7-991">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="079a7-992">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="079a7-992">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="079a7-993">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="079a7-993">Parameters - labelPosition</span></span>

<span data-ttu-id="079a7-994">値</span><span class="sxs-lookup"><span data-stu-id="079a7-994">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="079a7-995">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="079a7-995">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="079a7-996">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="079a7-996">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="079a7-997">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="079a7-997">Parameters - labelUnderline</span></span>

<span data-ttu-id="079a7-998">値</span><span class="sxs-lookup"><span data-stu-id="079a7-998">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="079a7-999">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="079a7-999">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="079a7-1000">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="079a7-1000">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="079a7-1001">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="079a7-1001">Parameters - labelWidth</span></span>

<span data-ttu-id="079a7-1002">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1002">value</span></span>  

<!-- -->

<span data-ttu-id="079a7-1003">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1003">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="079a7-1004">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="079a7-1004">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="079a7-1005">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1005">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="079a7-1006">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1006">Parameters - labelWidthMode</span></span>

<span data-ttu-id="079a7-1007">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1007">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="079a7-1008">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1008">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="079a7-1009">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1009">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="079a7-1010">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1010">Parameters - labelWidthValue</span></span>

<span data-ttu-id="079a7-1011">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1011">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="079a7-1012">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1012">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="079a7-1013">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="079a7-1013">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="079a7-1014">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="079a7-1014">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="079a7-1015">メソッド left</span><span class="sxs-lookup"><span data-stu-id="079a7-1015">Method left</span></span>

<span data-ttu-id="079a7-1016">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1016">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="079a7-1017">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="079a7-1017">Parameters - left</span></span>

<span data-ttu-id="079a7-1018">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1018">value</span></span>  
<span data-ttu-id="079a7-1019">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1019">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="079a7-1020">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1020">mode</span></span>  
<span data-ttu-id="079a7-1021">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1021">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="079a7-1022">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="079a7-1022">Return Value - left</span></span>

<span data-ttu-id="079a7-1023">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="079a7-1023">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="079a7-1024">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1024">Method leftMode</span></span>

<span data-ttu-id="079a7-1025">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1025">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="079a7-1026">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1026">Parameters - leftMode</span></span>

<span data-ttu-id="079a7-1027">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1027">value</span></span>  
<span data-ttu-id="079a7-1028">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1028">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="079a7-1029">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1029">Return Value - leftMode</span></span>

<span data-ttu-id="079a7-1030">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-1030">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="079a7-1031">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1031">Method leftValue</span></span>

<span data-ttu-id="079a7-1032">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1032">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="079a7-1033">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1033">Parameters - leftValue</span></span>

<span data-ttu-id="079a7-1034">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1034">value</span></span>  
<span data-ttu-id="079a7-1035">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1035">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="079a7-1036">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1036">Return Value - leftValue</span></span>

<span data-ttu-id="079a7-1037">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="079a7-1037">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="079a7-1038">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="079a7-1038">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="079a7-1039">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="079a7-1039">Parameters - limitText</span></span>

<span data-ttu-id="079a7-1040">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1040">value</span></span>  

<!-- -->

<span data-ttu-id="079a7-1041">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1041">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="079a7-1042">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="079a7-1042">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="079a7-1043">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1043">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="079a7-1044">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1044">Parameters - limitTextMode</span></span>

<span data-ttu-id="079a7-1045">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1045">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="079a7-1046">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1046">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="079a7-1047">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1047">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="079a7-1048">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1048">Parameters - limitTextValue</span></span>

<span data-ttu-id="079a7-1049">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1049">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="079a7-1050">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1050">Return Value - limitTextValue</span></span>

## <a name="method-linefromchar"></a><span data-ttu-id="079a7-1051">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="079a7-1051">Method lineFromChar</span></span>

```xpp
public int lineFromChar(int charIndex)
```

### <a name="parameters---linefromchar"></a><span data-ttu-id="079a7-1052">パラメーター - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="079a7-1052">Parameters - lineFromChar</span></span>

<span data-ttu-id="079a7-1053">charIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-1053">charIndex</span></span>  

### <a name="return-value---linefromchar"></a><span data-ttu-id="079a7-1054">戻り値 - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="079a7-1054">Return Value - lineFromChar</span></span>

## <a name="method-lineindex"></a><span data-ttu-id="079a7-1055">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-1055">Method lineIndex</span></span>

```xpp
public int lineIndex(int lineNo)
```

### <a name="parameters---lineindex"></a><span data-ttu-id="079a7-1056">パラメーター - lineIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-1056">Parameters - lineIndex</span></span>

<span data-ttu-id="079a7-1057">lineNo</span><span class="sxs-lookup"><span data-stu-id="079a7-1057">lineNo</span></span>  

### <a name="return-value---lineindex"></a><span data-ttu-id="079a7-1058">戻り値 - lineIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-1058">Return Value - lineIndex</span></span>

## <a name="method-linelength"></a><span data-ttu-id="079a7-1059">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="079a7-1059">Method lineLength</span></span>

```xpp
public int lineLength(int lineNo)
```

### <a name="parameters---linelength"></a><span data-ttu-id="079a7-1060">パラメーター - lineLength</span><span class="sxs-lookup"><span data-stu-id="079a7-1060">Parameters - lineLength</span></span>

<span data-ttu-id="079a7-1061">lineNo</span><span class="sxs-lookup"><span data-stu-id="079a7-1061">lineNo</span></span>  

### <a name="return-value---linelength"></a><span data-ttu-id="079a7-1062">戻り値 - lineLength</span><span class="sxs-lookup"><span data-stu-id="079a7-1062">Return Value - lineLength</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="079a7-1063">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="079a7-1063">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="079a7-1064">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="079a7-1064">Parameters - lookupButton</span></span>

<span data-ttu-id="079a7-1065">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1065">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="079a7-1066">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="079a7-1066">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="079a7-1067">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="079a7-1067">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="079a7-1068">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="079a7-1068">Parameters - mandatory</span></span>

<span data-ttu-id="079a7-1069">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1069">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="079a7-1070">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="079a7-1070">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="079a7-1071">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="079a7-1071">Method markAsUserAdd</span></span>

<span data-ttu-id="079a7-1072">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="079a7-1072">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="079a7-1073">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="079a7-1073">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="079a7-1074">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1074">value</span></span>  
<span data-ttu-id="079a7-1075">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1075">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="079a7-1076">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="079a7-1076">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="079a7-1077">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-1077">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="079a7-1078">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="079a7-1078">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="079a7-1079">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="079a7-1079">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="079a7-1080">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="079a7-1080">Method mouseDblClick</span></span>

<span data-ttu-id="079a7-1081">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1081">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="079a7-1082">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="079a7-1082">Parameters - mouseDblClick</span></span>

<span data-ttu-id="079a7-1083">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1083">x</span></span>  
<span data-ttu-id="079a7-1084">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1084">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1085">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1085">y</span></span>  
<span data-ttu-id="079a7-1086">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1086">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1087">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-1087">button</span></span>  
<span data-ttu-id="079a7-1088">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1088">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1089">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-1089">Ctrl</span></span>  
<span data-ttu-id="079a7-1090">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1090">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1091">シフト</span><span class="sxs-lookup"><span data-stu-id="079a7-1091">Shift</span></span>  
<span data-ttu-id="079a7-1092">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1092">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="079a7-1093">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="079a7-1093">Return Value - mouseDblClick</span></span>

<span data-ttu-id="079a7-1094">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1094">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="079a7-1095">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="079a7-1095">Remarks - mouseDblClick</span></span>

<span data-ttu-id="079a7-1096">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1096">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="079a7-1097">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="079a7-1097">Method mouseDown</span></span>

<span data-ttu-id="079a7-1098">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1098">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="079a7-1099">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="079a7-1099">Parameters - mouseDown</span></span>

<span data-ttu-id="079a7-1100">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1100">x</span></span>  
<span data-ttu-id="079a7-1101">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1101">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1102">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1102">y</span></span>  
<span data-ttu-id="079a7-1103">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1103">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1104">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-1104">button</span></span>  
<span data-ttu-id="079a7-1105">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1105">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1106">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-1106">Ctrl</span></span>  
<span data-ttu-id="079a7-1107">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1107">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1108">シフト</span><span class="sxs-lookup"><span data-stu-id="079a7-1108">Shift</span></span>  
<span data-ttu-id="079a7-1109">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1109">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="079a7-1110">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="079a7-1110">Return Value - mouseDown</span></span>

<span data-ttu-id="079a7-1111">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1111">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="079a7-1112">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="079a7-1112">Remarks - mouseDown</span></span>

<span data-ttu-id="079a7-1113">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1113">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="079a7-1114">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1114">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="079a7-1115">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="079a7-1115">Method mouseMove</span></span>

<span data-ttu-id="079a7-1116">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1116">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="079a7-1117">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="079a7-1117">Parameters - mouseMove</span></span>

<span data-ttu-id="079a7-1118">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1118">x</span></span>  
<span data-ttu-id="079a7-1119">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1119">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1120">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1120">y</span></span>  
<span data-ttu-id="079a7-1121">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1121">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1122">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-1122">button</span></span>  
<span data-ttu-id="079a7-1123">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1123">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1124">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-1124">Ctrl</span></span>  
<span data-ttu-id="079a7-1125">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1125">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1126">シフト</span><span class="sxs-lookup"><span data-stu-id="079a7-1126">Shift</span></span>  
<span data-ttu-id="079a7-1127">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1127">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="079a7-1128">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="079a7-1128">Return Value - mouseMove</span></span>

<span data-ttu-id="079a7-1129">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1129">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="079a7-1130">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="079a7-1130">Remarks - mouseMove</span></span>

<span data-ttu-id="079a7-1131">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1131">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="079a7-1132">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="079a7-1132">Method mouseUp</span></span>

<span data-ttu-id="079a7-1133">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1133">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="079a7-1134">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="079a7-1134">Parameters - mouseUp</span></span>

<span data-ttu-id="079a7-1135">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1135">x</span></span>  
<span data-ttu-id="079a7-1136">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1136">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1137">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1137">y</span></span>  
<span data-ttu-id="079a7-1138">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1138">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1139">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-1139">button</span></span>  
<span data-ttu-id="079a7-1140">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1140">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1141">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-1141">Ctrl</span></span>  
<span data-ttu-id="079a7-1142">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1142">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1143">シフト</span><span class="sxs-lookup"><span data-stu-id="079a7-1143">Shift</span></span>  
<span data-ttu-id="079a7-1144">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1144">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="079a7-1145">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="079a7-1145">Return Value - mouseUp</span></span>

<span data-ttu-id="079a7-1146">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1146">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="079a7-1147">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="079a7-1147">Remarks - mouseUp</span></span>

<span data-ttu-id="079a7-1148">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1148">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="079a7-1149">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1149">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="079a7-1150">メソッド名</span><span class="sxs-lookup"><span data-stu-id="079a7-1150">Method name</span></span>

<span data-ttu-id="079a7-1151">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1151">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="079a7-1152">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="079a7-1152">Parameters - name</span></span>

<span data-ttu-id="079a7-1153">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1153">value</span></span>  
<span data-ttu-id="079a7-1154">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1154">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="079a7-1155">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="079a7-1155">Return Value - name</span></span>

<span data-ttu-id="079a7-1156">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="079a7-1156">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="079a7-1157">備考 - name</span><span class="sxs-lookup"><span data-stu-id="079a7-1157">Remarks - name</span></span>

<span data-ttu-id="079a7-1158">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="079a7-1158">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="079a7-1159">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="079a7-1159">It must start with a letter.</span></span>
-   <span data-ttu-id="079a7-1160">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="079a7-1160">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="079a7-1161">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1161">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="079a7-1162">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="079a7-1162">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="079a7-1163">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="079a7-1163">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="079a7-1164">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="079a7-1164">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="079a7-1165">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="079a7-1165">Parameters - neededPermission</span></span>

<span data-ttu-id="079a7-1166">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1166">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="079a7-1167">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="079a7-1167">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="079a7-1168">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="079a7-1168">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="079a7-1169">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="079a7-1169">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="079a7-1170">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="079a7-1170">Method parentControl</span></span>

<span data-ttu-id="079a7-1171">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1171">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="079a7-1172">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="079a7-1172">Return Value - parentControl</span></span>

<span data-ttu-id="079a7-1173">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="079a7-1173">The parent control for the control.</span></span>

## <a name="method-posfromchar"></a><span data-ttu-id="079a7-1174">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="079a7-1174">Method posFromChar</span></span>

```xpp
public container posFromChar(int charIndex)
```

### <a name="parameters---posfromchar"></a><span data-ttu-id="079a7-1175">パラメーター - posFromChar</span><span class="sxs-lookup"><span data-stu-id="079a7-1175">Parameters - posFromChar</span></span>

<span data-ttu-id="079a7-1176">charIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-1176">charIndex</span></span>  

### <a name="return-value---posfromchar"></a><span data-ttu-id="079a7-1177">戻り値 - posFromChar</span><span class="sxs-lookup"><span data-stu-id="079a7-1177">Return Value - posFromChar</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="079a7-1178">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="079a7-1178">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="079a7-1179">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="079a7-1179">Parameters - previewPartRef</span></span>

<span data-ttu-id="079a7-1180">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1180">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="079a7-1181">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="079a7-1181">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="079a7-1182">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="079a7-1182">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="079a7-1183">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="079a7-1183">Parameters - promptrect</span></span>

<span data-ttu-id="079a7-1184">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1184">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="079a7-1185">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="079a7-1185">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="079a7-1186">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1186">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="079a7-1187">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1187">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="079a7-1188">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1188">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="079a7-1189">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1189">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="079a7-1190">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="079a7-1190">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="079a7-1191">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="079a7-1191">Parameters - searchAfterInput</span></span>

<span data-ttu-id="079a7-1192">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1192">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="079a7-1193">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="079a7-1193">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="079a7-1194">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1194">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="079a7-1195">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1195">Parameters - searchMode</span></span>

<span data-ttu-id="079a7-1196">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1196">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="079a7-1197">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1197">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="079a7-1198">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="079a7-1198">Method securityKey</span></span>

<span data-ttu-id="079a7-1199">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1199">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="079a7-1200">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="079a7-1200">Parameters - securityKey</span></span>

<span data-ttu-id="079a7-1201">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1201">value</span></span>  
<span data-ttu-id="079a7-1202">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1202">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="079a7-1203">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="079a7-1203">Return Value - securityKey</span></span>

<span data-ttu-id="079a7-1204">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1204">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="079a7-1205">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="079a7-1205">Method showContextMenu</span></span>

<span data-ttu-id="079a7-1206">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1206">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="079a7-1207">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="079a7-1207">Parameters - showContextMenu</span></span>

<span data-ttu-id="079a7-1208">menuHandle</span><span class="sxs-lookup"><span data-stu-id="079a7-1208">menuHandle</span></span>  
<span data-ttu-id="079a7-1209">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="079a7-1209">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="079a7-1210">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="079a7-1210">Return Value - showContextMenu</span></span>

<span data-ttu-id="079a7-1211">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1211">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="079a7-1212">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="079a7-1212">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="079a7-1213">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="079a7-1213">Parameters - showLabel</span></span>

<span data-ttu-id="079a7-1214">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1214">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="079a7-1215">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="079a7-1215">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="079a7-1216">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="079a7-1216">Method skip</span></span>

<span data-ttu-id="079a7-1217">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1217">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="079a7-1218">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="079a7-1218">Parameters - skip</span></span>

<span data-ttu-id="079a7-1219">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1219">value</span></span>  
<span data-ttu-id="079a7-1220">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1220">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="079a7-1221">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="079a7-1221">Return Value - skip</span></span>

<span data-ttu-id="079a7-1222">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-1222">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="079a7-1223">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="079a7-1223">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="079a7-1224">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="079a7-1224">Parameters - sort</span></span>

<span data-ttu-id="079a7-1225">sortDirection</span><span class="sxs-lookup"><span data-stu-id="079a7-1225">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="079a7-1226">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="079a7-1226">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="079a7-1227">メソッド style</span><span class="sxs-lookup"><span data-stu-id="079a7-1227">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="079a7-1228">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="079a7-1228">Parameters - style</span></span>

<span data-ttu-id="079a7-1229">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1229">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="079a7-1230">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="079a7-1230">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="079a7-1231">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="079a7-1231">Method toolTip</span></span>

<span data-ttu-id="079a7-1232">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1232">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="079a7-1233">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="079a7-1233">Return Value - toolTip</span></span>

<span data-ttu-id="079a7-1234">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="079a7-1234">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="079a7-1235">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="079a7-1235">Remarks - toolTip</span></span>

<span data-ttu-id="079a7-1236">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1236">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="079a7-1237">メソッド top</span><span class="sxs-lookup"><span data-stu-id="079a7-1237">Method top</span></span>

<span data-ttu-id="079a7-1238">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1238">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="079a7-1239">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="079a7-1239">Parameters - top</span></span>

<span data-ttu-id="079a7-1240">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1240">value</span></span>  
<span data-ttu-id="079a7-1241">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1241">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="079a7-1242">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1242">mode</span></span>  
<span data-ttu-id="079a7-1243">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1243">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="079a7-1244">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="079a7-1244">Return Value - top</span></span>

<span data-ttu-id="079a7-1245">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="079a7-1245">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="079a7-1246">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1246">Method topMode</span></span>

<span data-ttu-id="079a7-1247">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1247">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="079a7-1248">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1248">Parameters - topMode</span></span>

<span data-ttu-id="079a7-1249">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1249">value</span></span>  
<span data-ttu-id="079a7-1250">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1250">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="079a7-1251">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1251">Return Value - topMode</span></span>

<span data-ttu-id="079a7-1252">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-1252">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="079a7-1253">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1253">Method topValue</span></span>

<span data-ttu-id="079a7-1254">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1254">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="079a7-1255">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1255">Parameters - topValue</span></span>

<span data-ttu-id="079a7-1256">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1256">value</span></span>  
<span data-ttu-id="079a7-1257">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1257">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="079a7-1258">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1258">Return Value - topValue</span></span>

<span data-ttu-id="079a7-1259">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="079a7-1259">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="079a7-1260">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="079a7-1260">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="079a7-1261">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="079a7-1261">Parameters - type</span></span>

<span data-ttu-id="079a7-1262">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1262">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="079a7-1263">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="079a7-1263">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="079a7-1264">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="079a7-1264">Method underline</span></span>

<span data-ttu-id="079a7-1265">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1265">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="079a7-1266">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="079a7-1266">Parameters - underline</span></span>

<span data-ttu-id="079a7-1267">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1267">value</span></span>  
<span data-ttu-id="079a7-1268">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1268">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="079a7-1269">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="079a7-1269">Return Value - underline</span></span>

<span data-ttu-id="079a7-1270">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="079a7-1270">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="079a7-1271">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="079a7-1271">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="079a7-1272">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="079a7-1272">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="079a7-1273">データ</span><span class="sxs-lookup"><span data-stu-id="079a7-1273">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="079a7-1274">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="079a7-1274">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="079a7-1275">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="079a7-1275">Method userData</span></span>

<span data-ttu-id="079a7-1276">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1276">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="079a7-1277">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="079a7-1277">Parameters - userData</span></span>

<span data-ttu-id="079a7-1278">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1278">value</span></span>  
<span data-ttu-id="079a7-1279">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1279">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="079a7-1280">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="079a7-1280">Return Value - userData</span></span>

<span data-ttu-id="079a7-1281">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="079a7-1281">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="079a7-1282">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="079a7-1282">Method userDataItem</span></span>

<span data-ttu-id="079a7-1283">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1283">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="079a7-1284">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="079a7-1284">Parameters - userDataItem</span></span>

<span data-ttu-id="079a7-1285">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1285">value</span></span>  
<span data-ttu-id="079a7-1286">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1286">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="079a7-1287">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="079a7-1287">Return Value - userDataItem</span></span>

<span data-ttu-id="079a7-1288">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="079a7-1288">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="079a7-1289">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="079a7-1289">Method userDataItems</span></span>

<span data-ttu-id="079a7-1290">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1290">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="079a7-1291">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="079a7-1291">Parameters - userDataItems</span></span>

<span data-ttu-id="079a7-1292">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1292">value</span></span>  
<span data-ttu-id="079a7-1293">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1293">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="079a7-1294">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="079a7-1294">Return Value - userDataItems</span></span>

<span data-ttu-id="079a7-1295">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="079a7-1295">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="079a7-1296">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="079a7-1296">Method userDisable</span></span>

<span data-ttu-id="079a7-1297">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1297">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="079a7-1298">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="079a7-1298">Parameters - userDisable</span></span>

<span data-ttu-id="079a7-1299">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1299">value</span></span>  
<span data-ttu-id="079a7-1300">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1300">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="079a7-1301">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="079a7-1301">Return Value - userDisable</span></span>

<span data-ttu-id="079a7-1302">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1302">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="079a7-1303">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="079a7-1303">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="079a7-1304">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="079a7-1304">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="079a7-1305">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1305">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="079a7-1306">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="079a7-1306">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="079a7-1307">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-1307">Method userHeight</span></span>

<span data-ttu-id="079a7-1308">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1308">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="079a7-1309">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-1309">Parameters - userHeight</span></span>

<span data-ttu-id="079a7-1310">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1310">value</span></span>  
<span data-ttu-id="079a7-1311">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1311">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="079a7-1312">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="079a7-1312">Return Value - userHeight</span></span>

<span data-ttu-id="079a7-1313">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="079a7-1313">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="079a7-1314">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="079a7-1314">Method userHide</span></span>

<span data-ttu-id="079a7-1315">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1315">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="079a7-1316">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="079a7-1316">Parameters - userHide</span></span>

<span data-ttu-id="079a7-1317">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1317">value</span></span>  
<span data-ttu-id="079a7-1318">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1318">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="079a7-1319">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="079a7-1319">Return Value - userHide</span></span>

<span data-ttu-id="079a7-1320">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1320">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="079a7-1321">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="079a7-1321">Remarks - userHide</span></span>

<span data-ttu-id="079a7-1322">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1322">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="079a7-1323">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1323">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="079a7-1324">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1324">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="079a7-1325">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="079a7-1325">Method userOrgContainer</span></span>

<span data-ttu-id="079a7-1326">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1326">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="079a7-1327">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="079a7-1327">Parameters - userOrgContainer</span></span>

<span data-ttu-id="079a7-1328">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1328">value</span></span>  
<span data-ttu-id="079a7-1329">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1329">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="079a7-1330">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="079a7-1330">Return Value - userOrgContainer</span></span>

<span data-ttu-id="079a7-1331">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="079a7-1331">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="079a7-1332">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="079a7-1332">Method userOrgSibling</span></span>

<span data-ttu-id="079a7-1333">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1333">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="079a7-1334">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="079a7-1334">Parameters - userOrgSibling</span></span>

<span data-ttu-id="079a7-1335">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1335">value</span></span>  
<span data-ttu-id="079a7-1336">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1336">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="079a7-1337">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="079a7-1337">Return Value - userOrgSibling</span></span>

<span data-ttu-id="079a7-1338">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="079a7-1338">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="079a7-1339">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="079a7-1339">Method userPromptText</span></span>

<span data-ttu-id="079a7-1340">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1340">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="079a7-1341">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="079a7-1341">Parameters - userPromptText</span></span>

<span data-ttu-id="079a7-1342">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1342">value</span></span>  
<span data-ttu-id="079a7-1343">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1343">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="079a7-1344">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="079a7-1344">Return Value - userPromptText</span></span>

<span data-ttu-id="079a7-1345">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="079a7-1345">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="079a7-1346">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="079a7-1346">Method userSecurityLevel</span></span>

<span data-ttu-id="079a7-1347">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1347">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="079a7-1348">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="079a7-1348">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="079a7-1349">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1349">value</span></span>  
<span data-ttu-id="079a7-1350">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1350">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="079a7-1351">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="079a7-1351">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="079a7-1352">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="079a7-1352">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="079a7-1353">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="079a7-1353">Method userSkip</span></span>

<span data-ttu-id="079a7-1354">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1354">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="079a7-1355">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="079a7-1355">Parameters - userSkip</span></span>

<span data-ttu-id="079a7-1356">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1356">value</span></span>  
<span data-ttu-id="079a7-1357">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1357">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="079a7-1358">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1358">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="079a7-1359">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="079a7-1359">Return Value - userSkip</span></span>

<span data-ttu-id="079a7-1360">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="079a7-1360">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="079a7-1361">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="079a7-1361">Method userWidth</span></span>

<span data-ttu-id="079a7-1362">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1362">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="079a7-1363">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="079a7-1363">Parameters - userWidth</span></span>

<span data-ttu-id="079a7-1364">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1364">value</span></span>  
<span data-ttu-id="079a7-1365">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1365">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="079a7-1366">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="079a7-1366">Return Value - userWidth</span></span>

<span data-ttu-id="079a7-1367">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1367">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="079a7-1368">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="079a7-1368">Remarks - userWidth</span></span>

<span data-ttu-id="079a7-1369">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1369">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="079a7-1370">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="079a7-1370">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="079a7-1371">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1371">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="079a7-1372">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="079a7-1372">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="079a7-1373">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="079a7-1373">Return Value - validate</span></span>

## <a name="method-value"></a><span data-ttu-id="079a7-1374">メソッド value</span><span class="sxs-lookup"><span data-stu-id="079a7-1374">Method value</span></span>

```xpp
public Guid value([Guid value])
```

### <a name="parameters---value"></a><span data-ttu-id="079a7-1375">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="079a7-1375">Parameters - value</span></span>

<span data-ttu-id="079a7-1376">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1376">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="079a7-1377">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="079a7-1377">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="079a7-1378">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="079a7-1378">Method verticalSpacing</span></span>

<span data-ttu-id="079a7-1379">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1379">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="079a7-1380">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="079a7-1380">Parameters - verticalSpacing</span></span>

<span data-ttu-id="079a7-1381">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1381">value</span></span>  
<span data-ttu-id="079a7-1382">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1382">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="079a7-1383">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1383">mode</span></span>  
<span data-ttu-id="079a7-1384">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1384">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="079a7-1385">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="079a7-1385">Return Value - verticalSpacing</span></span>

<span data-ttu-id="079a7-1386">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="079a7-1386">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="079a7-1387">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1387">Method verticalSpacingMode</span></span>

<span data-ttu-id="079a7-1388">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1388">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="079a7-1389">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1389">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="079a7-1390">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1390">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="079a7-1391">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1391">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="079a7-1392">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-1392">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="079a7-1393">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1393">Method verticalSpacingValue</span></span>

<span data-ttu-id="079a7-1394">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1394">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="079a7-1395">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1395">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="079a7-1396">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1396">value</span></span>  
<span data-ttu-id="079a7-1397">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1397">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="079a7-1398">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1398">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="079a7-1399">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="079a7-1399">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="079a7-1400">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1400">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="079a7-1401">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1401">Parameters - viewEditMode</span></span>

<span data-ttu-id="079a7-1402">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1402">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="079a7-1403">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1403">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="079a7-1404">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="079a7-1404">Method visible</span></span>

<span data-ttu-id="079a7-1405">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1405">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="079a7-1406">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="079a7-1406">Parameters - visible</span></span>

<span data-ttu-id="079a7-1407">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1407">value</span></span>  
<span data-ttu-id="079a7-1408">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1408">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="079a7-1409">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="079a7-1409">Return Value - visible</span></span>

<span data-ttu-id="079a7-1410">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="079a7-1410">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="079a7-1411">メソッド width</span><span class="sxs-lookup"><span data-stu-id="079a7-1411">Method width</span></span>

<span data-ttu-id="079a7-1412">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1412">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="079a7-1413">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="079a7-1413">Parameters - width</span></span>

<span data-ttu-id="079a7-1414">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1414">value</span></span>  
<span data-ttu-id="079a7-1415">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1415">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="079a7-1416">モード</span><span class="sxs-lookup"><span data-stu-id="079a7-1416">mode</span></span>  
<span data-ttu-id="079a7-1417">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1417">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="079a7-1418">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="079a7-1418">Return Value - width</span></span>

<span data-ttu-id="079a7-1419">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="079a7-1419">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="079a7-1420">備考 - width</span><span class="sxs-lookup"><span data-stu-id="079a7-1420">Remarks - width</span></span>

<span data-ttu-id="079a7-1421">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1421">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="079a7-1422">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="079a7-1422">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="079a7-1423">モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-1423">Mode.</span></span>           | <span data-ttu-id="079a7-1424">幅計算。</span><span class="sxs-lookup"><span data-stu-id="079a7-1424">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="079a7-1425">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="079a7-1425">-1 Exact.</span></span>       | <span data-ttu-id="079a7-1426">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1426">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="079a7-1427">0 自動。</span><span class="sxs-lookup"><span data-stu-id="079a7-1427">0 Auto.</span></span>         | <span data-ttu-id="079a7-1428">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1428">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="079a7-1429">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="079a7-1429">1 Column width.</span></span> | <span data-ttu-id="079a7-1430">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="079a7-1430">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="079a7-1431">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1431">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="079a7-1432">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1432">Method widthMode</span></span>

<span data-ttu-id="079a7-1433">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1433">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="079a7-1434">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1434">Parameters - widthMode</span></span>

<span data-ttu-id="079a7-1435">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1435">value</span></span>  
<span data-ttu-id="079a7-1436">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="079a7-1436">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="079a7-1437">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1437">Return Value - widthMode</span></span>

<span data-ttu-id="079a7-1438">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1438">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="079a7-1439">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1439">Remarks - widthMode</span></span>

<span data-ttu-id="079a7-1440">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="079a7-1440">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="079a7-1441">モード。</span><span class="sxs-lookup"><span data-stu-id="079a7-1441">Mode.</span></span>         | <span data-ttu-id="079a7-1442">幅計算。</span><span class="sxs-lookup"><span data-stu-id="079a7-1442">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="079a7-1443">正確。</span><span class="sxs-lookup"><span data-stu-id="079a7-1443">Exact.</span></span>        | <span data-ttu-id="079a7-1444">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1444">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="079a7-1445">自動。</span><span class="sxs-lookup"><span data-stu-id="079a7-1445">Auto.</span></span>         | <span data-ttu-id="079a7-1446">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1446">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="079a7-1447">列の幅。</span><span class="sxs-lookup"><span data-stu-id="079a7-1447">Column width.</span></span> | <span data-ttu-id="079a7-1448">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="079a7-1448">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="079a7-1449">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="079a7-1449">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="079a7-1450">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1450">Method widthValue</span></span>

<span data-ttu-id="079a7-1451">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1451">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="079a7-1452">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1452">Parameters - widthValue</span></span>

<span data-ttu-id="079a7-1453">値</span><span class="sxs-lookup"><span data-stu-id="079a7-1453">value</span></span>  
<span data-ttu-id="079a7-1454">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1454">An Integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="079a7-1455">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1455">Return Value - widthValue</span></span>

<span data-ttu-id="079a7-1456">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="079a7-1456">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="079a7-1457">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="079a7-1457">Remarks - widthValue</span></span>

<span data-ttu-id="079a7-1458">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1458">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="079a7-1459">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="079a7-1459">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="079a7-1460">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="079a7-1460">Parameters - OnLostFocus</span></span>

<span data-ttu-id="079a7-1461">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1461">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1462">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1462">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="079a7-1463">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="079a7-1463">Method mouseLeave</span></span>

<span data-ttu-id="079a7-1464">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1464">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-setcursorpos"></a><span data-ttu-id="079a7-1465">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="079a7-1465">Method setCursorPos</span></span>

```xpp
public void setCursorPos(int x, int y)
```

### <a name="parameters---setcursorpos"></a><span data-ttu-id="079a7-1466">パラメーター - setCursorPos</span><span class="sxs-lookup"><span data-stu-id="079a7-1466">Parameters - setCursorPos</span></span>

<span data-ttu-id="079a7-1467">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1467">x</span></span>  

<!-- -->

<span data-ttu-id="079a7-1468">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1468">y</span></span>  

## <a name="method-onvalidating"></a><span data-ttu-id="079a7-1469">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="079a7-1469">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="079a7-1470">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="079a7-1470">Parameters - OnValidating</span></span>

<span data-ttu-id="079a7-1471">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1471">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1472">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1472">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="079a7-1473">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="079a7-1473">Method dropEx</span></span>

<span data-ttu-id="079a7-1474">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1474">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="079a7-1475">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="079a7-1475">Parameters - dropEx</span></span>

<span data-ttu-id="079a7-1476">dragSource</span><span class="sxs-lookup"><span data-stu-id="079a7-1476">dragSource</span></span>  
<span data-ttu-id="079a7-1477">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1477">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-1478">dragMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1478">dragMode</span></span>  
<span data-ttu-id="079a7-1479">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1479">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-1480">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1480">x</span></span>  
<span data-ttu-id="079a7-1481">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1481">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-1482">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1482">y</span></span>  
<span data-ttu-id="079a7-1483">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1483">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-performdblookup"></a><span data-ttu-id="079a7-1484">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1484">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="079a7-1485">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1485">Parameters - performDBLookup</span></span>

<span data-ttu-id="079a7-1486">fieldId</span><span class="sxs-lookup"><span data-stu-id="079a7-1486">fieldId</span></span>  

<!-- -->

<span data-ttu-id="079a7-1487">tableId</span><span class="sxs-lookup"><span data-stu-id="079a7-1487">tableId</span></span>  

<!-- -->

<span data-ttu-id="079a7-1488">会社</span><span class="sxs-lookup"><span data-stu-id="079a7-1488">company</span></span>  

## <a name="method-context"></a><span data-ttu-id="079a7-1489">メソッド context</span><span class="sxs-lookup"><span data-stu-id="079a7-1489">Method context</span></span>

<span data-ttu-id="079a7-1490">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1490">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-onenter"></a><span data-ttu-id="079a7-1491">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="079a7-1491">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="079a7-1492">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="079a7-1492">Parameters - OnEnter</span></span>

<span data-ttu-id="079a7-1493">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1493">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1494">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1494">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="079a7-1495">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="079a7-1495">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="079a7-1496">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="079a7-1496">Parameters - filter</span></span>

<span data-ttu-id="079a7-1497">filterStr</span><span class="sxs-lookup"><span data-stu-id="079a7-1497">filterStr</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="079a7-1498">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="079a7-1498">Method resetUserSetting</span></span>

<span data-ttu-id="079a7-1499">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="079a7-1499">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-inputsearch"></a><span data-ttu-id="079a7-1500">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="079a7-1500">Method inputSearch</span></span>

<span data-ttu-id="079a7-1501">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1501">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="079a7-1502">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="079a7-1502">Parameters - inputSearch</span></span>

<span data-ttu-id="079a7-1503">searchStr</span><span class="sxs-lookup"><span data-stu-id="079a7-1503">searchStr</span></span>  
<span data-ttu-id="079a7-1504">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="079a7-1504">The string value to use to filter data; optional.</span></span>

## <a name="method-enter"></a><span data-ttu-id="079a7-1505">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="079a7-1505">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="079a7-1506">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="079a7-1506">Method displayControl</span></span>

<span data-ttu-id="079a7-1507">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1507">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-undo"></a><span data-ttu-id="079a7-1508">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="079a7-1508">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-setfocus"></a><span data-ttu-id="079a7-1509">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="079a7-1509">Method setFocus</span></span>

<span data-ttu-id="079a7-1510">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1510">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-onvalidated"></a><span data-ttu-id="079a7-1511">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="079a7-1511">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="079a7-1512">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="079a7-1512">Parameters - OnValidated</span></span>

<span data-ttu-id="079a7-1513">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1513">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1514">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1514">e</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="079a7-1515">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="079a7-1515">Method gotFocus</span></span>

<span data-ttu-id="079a7-1516">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1516">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-onleaving"></a><span data-ttu-id="079a7-1517">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="079a7-1517">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="079a7-1518">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="079a7-1518">Parameters - OnLeaving</span></span>

<span data-ttu-id="079a7-1519">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1519">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1520">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1520">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="079a7-1521">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="079a7-1521">Method dragLeave</span></span>

<span data-ttu-id="079a7-1522">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1522">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-copy"></a><span data-ttu-id="079a7-1523">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="079a7-1523">Method copy</span></span>

<span data-ttu-id="079a7-1524">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="079a7-1524">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-onlookup"></a><span data-ttu-id="079a7-1525">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1525">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="079a7-1526">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1526">Parameters - OnLookup</span></span>

<span data-ttu-id="079a7-1527">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1527">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1528">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1528">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="079a7-1529">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="079a7-1529">Method paste</span></span>

<span data-ttu-id="079a7-1530">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1530">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-linescroll"></a><span data-ttu-id="079a7-1531">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="079a7-1531">Method lineScroll</span></span>

```xpp
public void lineScroll(int dx, int dy)
```

### <a name="parameters---linescroll"></a><span data-ttu-id="079a7-1532">パラメーター - lineScroll</span><span class="sxs-lookup"><span data-stu-id="079a7-1532">Parameters - lineScroll</span></span>

<span data-ttu-id="079a7-1533">dx</span><span class="sxs-lookup"><span data-stu-id="079a7-1533">dx</span></span>  

<!-- -->

<span data-ttu-id="079a7-1534">dy</span><span class="sxs-lookup"><span data-stu-id="079a7-1534">dy</span></span>  

## <a name="method-cut"></a><span data-ttu-id="079a7-1535">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="079a7-1535">Method cut</span></span>

<span data-ttu-id="079a7-1536">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="079a7-1536">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-performformlookup"></a><span data-ttu-id="079a7-1537">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1537">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="079a7-1538">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1538">Parameters - performFormLookup</span></span>

<span data-ttu-id="079a7-1539">フォーム</span><span class="sxs-lookup"><span data-stu-id="079a7-1539">form</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="079a7-1540">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="079a7-1540">Method prefColumnSize</span></span>

<span data-ttu-id="079a7-1541">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1541">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="079a7-1542">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="079a7-1542">Parameters - prefColumnSize</span></span>

<span data-ttu-id="079a7-1543">width</span><span class="sxs-lookup"><span data-stu-id="079a7-1543">width</span></span>  
<span data-ttu-id="079a7-1544">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="079a7-1544">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="079a7-1545">height</span><span class="sxs-lookup"><span data-stu-id="079a7-1545">height</span></span>  
<span data-ttu-id="079a7-1546">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="079a7-1546">The preferred height of the control.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="079a7-1547">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="079a7-1547">Method lostFocus</span></span>

<span data-ttu-id="079a7-1548">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1548">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="079a7-1549">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="079a7-1549">Method mouseEnter</span></span>

<span data-ttu-id="079a7-1550">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1550">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="079a7-1551">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="079a7-1551">Parameters - mouseEnter</span></span>

<span data-ttu-id="079a7-1552">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1552">x</span></span>  
<span data-ttu-id="079a7-1553">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1553">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1554">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1554">y</span></span>  
<span data-ttu-id="079a7-1555">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1555">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1556">ボタン</span><span class="sxs-lookup"><span data-stu-id="079a7-1556">button</span></span>  
<span data-ttu-id="079a7-1557">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1557">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1558">Ctrl</span><span class="sxs-lookup"><span data-stu-id="079a7-1558">Ctrl</span></span>  
<span data-ttu-id="079a7-1559">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1559">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="079a7-1560">シフト</span><span class="sxs-lookup"><span data-stu-id="079a7-1560">Shift</span></span>  
<span data-ttu-id="079a7-1561">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1561">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-jumpref"></a><span data-ttu-id="079a7-1562">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="079a7-1562">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="079a7-1563">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-1563">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="079a7-1564">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="079a7-1564">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="079a7-1565">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="079a7-1565">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="079a7-1566">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="079a7-1566">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="079a7-1567">overrideObject</span><span class="sxs-lookup"><span data-stu-id="079a7-1567">overrideObject</span></span>  

## <a name="method-scrollcursor"></a><span data-ttu-id="079a7-1568">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="079a7-1568">Method scrollCursor</span></span>

```xpp
public void scrollCursor()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="079a7-1569">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="079a7-1569">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="079a7-1570">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="079a7-1570">Parameters - OnGotFocus</span></span>

<span data-ttu-id="079a7-1571">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1571">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1572">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1572">e</span></span>  

## <a name="method-setselection"></a><span data-ttu-id="079a7-1573">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="079a7-1573">Method setSelection</span></span>

```xpp
public void setSelection(int charIndexFrom, int charIndexTo)
```

### <a name="parameters---setselection"></a><span data-ttu-id="079a7-1574">パラメーター - setSelection</span><span class="sxs-lookup"><span data-stu-id="079a7-1574">Parameters - setSelection</span></span>

<span data-ttu-id="079a7-1575">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="079a7-1575">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="079a7-1576">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="079a7-1576">charIndexTo</span></span>  

## <a name="method-drop"></a><span data-ttu-id="079a7-1577">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="079a7-1577">Method drop</span></span>

<span data-ttu-id="079a7-1578">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1578">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="079a7-1579">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="079a7-1579">Parameters - drop</span></span>

<span data-ttu-id="079a7-1580">dragSource</span><span class="sxs-lookup"><span data-stu-id="079a7-1580">dragSource</span></span>  
<span data-ttu-id="079a7-1581">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1581">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-1582">dragMode</span><span class="sxs-lookup"><span data-stu-id="079a7-1582">dragMode</span></span>  
<span data-ttu-id="079a7-1583">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1583">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-1584">x</span><span class="sxs-lookup"><span data-stu-id="079a7-1584">x</span></span>  
<span data-ttu-id="079a7-1585">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1585">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="079a7-1586">y</span><span class="sxs-lookup"><span data-stu-id="079a7-1586">y</span></span>  
<span data-ttu-id="079a7-1587">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="079a7-1587">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-pastetext"></a><span data-ttu-id="079a7-1588">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="079a7-1588">Method pasteText</span></span>

```xpp
public void pasteText(str pasteStr, [boolean InsertSel])
```

### <a name="parameters---pastetext"></a><span data-ttu-id="079a7-1589">パラメーター - pasteText</span><span class="sxs-lookup"><span data-stu-id="079a7-1589">Parameters - pasteText</span></span>

<span data-ttu-id="079a7-1590">pasteStr</span><span class="sxs-lookup"><span data-stu-id="079a7-1590">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="079a7-1591">InsertSel</span><span class="sxs-lookup"><span data-stu-id="079a7-1591">InsertSel</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="079a7-1592">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="079a7-1592">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="079a7-1593">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="079a7-1593">Parameters - OnModified</span></span>

<span data-ttu-id="079a7-1594">sender</span><span class="sxs-lookup"><span data-stu-id="079a7-1594">sender</span></span>  

<!-- -->

<span data-ttu-id="079a7-1595">e</span><span class="sxs-lookup"><span data-stu-id="079a7-1595">e</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="079a7-1596">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="079a7-1596">Method endDrag</span></span>

<span data-ttu-id="079a7-1597">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079a7-1597">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="079a7-1598">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="079a7-1598">Remarks - endDrag</span></span>

<span data-ttu-id="079a7-1599">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="079a7-1599">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="079a7-1600">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="079a7-1600">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-performtypelookup"></a><span data-ttu-id="079a7-1601">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1601">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="079a7-1602">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1602">Parameters - performTypeLookup</span></span>

<span data-ttu-id="079a7-1603">userType</span><span class="sxs-lookup"><span data-stu-id="079a7-1603">userType</span></span>  

<!-- -->

<span data-ttu-id="079a7-1604">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="079a7-1604">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="079a7-1605">会社</span><span class="sxs-lookup"><span data-stu-id="079a7-1605">company</span></span>  

## <a name="method-textchange"></a><span data-ttu-id="079a7-1606">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="079a7-1606">Method textChange</span></span>

```xpp
public void textChange()
```

## <a name="method-lookup"></a><span data-ttu-id="079a7-1607">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="079a7-1607">Method lookup</span></span>

```xpp
public void lookup()
```

