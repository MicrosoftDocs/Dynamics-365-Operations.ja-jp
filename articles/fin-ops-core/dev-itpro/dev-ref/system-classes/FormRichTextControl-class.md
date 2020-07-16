---
title: FormRichTextControl クラス
description: このトピックでは、FormRichTextControl クラスについて説明します。
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
ms.openlocfilehash: 65f4f9506cc4b9e09b3af89bddaf5b4455711f17
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502623"
---
# <a name="class-formrichtextcontrol"></a><span data-ttu-id="7d98d-103">クラス FormRichTextControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-103">Class FormRichTextControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormRichTextControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="7d98d-104">備考</span><span class="sxs-lookup"><span data-stu-id="7d98d-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7d98d-105">例</span><span class="sxs-lookup"><span data-stu-id="7d98d-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7d98d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="7d98d-106">Methods</span></span>

| <span data-ttu-id="7d98d-107">方法</span><span class="sxs-lookup"><span data-stu-id="7d98d-107">Method</span></span>                                                                                                      | <span data-ttu-id="7d98d-108">説明</span><span class="sxs-lookup"><span data-stu-id="7d98d-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d98d-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="7d98d-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7d98d-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="7d98d-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="7d98d-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="7d98d-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="7d98d-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="7d98d-115">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-115">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="7d98d-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="7d98d-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="7d98d-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-119">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="7d98d-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="7d98d-121">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-121">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="7d98d-122">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7d98d-122">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="7d98d-123">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-123">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="7d98d-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-124">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="7d98d-125">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-125">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="7d98d-126">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-126">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="7d98d-127">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-127">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="7d98d-128">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-128">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-129">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="7d98d-129">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="7d98d-130">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-130">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="7d98d-131">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-131">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="7d98d-132">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-132">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="7d98d-133">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7d98d-133">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-134">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-134">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="7d98d-135">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-135">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7d98d-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="7d98d-137">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-137">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="7d98d-138">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="7d98d-138">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="7d98d-139">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-139">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="7d98d-140">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-140">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="7d98d-141">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-141">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="7d98d-142">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-142">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-143">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-143">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-144">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="7d98d-144">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-145">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="7d98d-145">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-146">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-146">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-147">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-147">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="7d98d-148">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-148">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="7d98d-149">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-149">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="7d98d-150">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-150">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="7d98d-151">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-151">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-152">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-152">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-153">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-153">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-154">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-154">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-155">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-155">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-156">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-156">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-157">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-157">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-158">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-158">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="7d98d-159">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-159">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="7d98d-160">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-160">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="7d98d-161">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-161">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="7d98d-162">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7d98d-162">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="7d98d-163">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-163">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="7d98d-164">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7d98d-164">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="7d98d-165">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-165">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="7d98d-166">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="7d98d-166">public str dragText()</span></span>                                                                                       | <span data-ttu-id="7d98d-167">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-167">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="7d98d-168">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-168">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="7d98d-169">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-169">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="7d98d-170">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-170">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-171">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-171">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-172">public int find(\[str findStr\], \[int start\], \[int end\], \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-172">public int find(\[str findStr\], \[int start\], \[int end\], \[int flags\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-173">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-173">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="7d98d-174">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-174">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="7d98d-175">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-175">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="7d98d-176">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-176">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="7d98d-177">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-177">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="7d98d-178">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-178">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="7d98d-179">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="7d98d-179">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-180">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="7d98d-180">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-181">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="7d98d-181">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-182">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="7d98d-182">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-183">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="7d98d-183">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-184">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-184">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="7d98d-185">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-185">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="7d98d-186">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="7d98d-186">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="7d98d-187">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-187">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="7d98d-188">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-188">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="7d98d-189">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-189">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7d98d-190">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-190">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="7d98d-191">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-191">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="7d98d-192">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-192">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="7d98d-193">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-193">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7d98d-194">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="7d98d-194">public str helpField()</span></span>                                                                                      | <span data-ttu-id="7d98d-195">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-195">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7d98d-196">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-196">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="7d98d-197">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-197">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="7d98d-198">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-198">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="7d98d-199">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-199">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="7d98d-200">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="7d98d-200">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="7d98d-201">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-201">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7d98d-202">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-202">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-203">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="7d98d-203">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-204">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="7d98d-204">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="7d98d-205">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-205">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="7d98d-206">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="7d98d-206">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="7d98d-207">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-207">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="7d98d-208">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="7d98d-208">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="7d98d-209">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-209">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="7d98d-210">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-210">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-211">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-211">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="7d98d-212">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-212">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="7d98d-213">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-213">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-214">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-214">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-215">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-215">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-216">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-216">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-217">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-217">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-218">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-218">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-219">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-219">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-220">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-220">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-221">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-221">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-222">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-222">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-223">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-223">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-224">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-224">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-225">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-225">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-226">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-226">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-227">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-227">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-228">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-228">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-229">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-229">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-230">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-230">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-231">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-231">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-232">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="7d98d-232">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-233">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-233">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="7d98d-234">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-234">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="7d98d-235">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-235">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="7d98d-236">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-236">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7d98d-237">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-237">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="7d98d-238">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-238">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="7d98d-239">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-239">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-240">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-240">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-241">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-241">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-242">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="7d98d-242">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-243">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="7d98d-243">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-244">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="7d98d-244">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-245">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-245">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-246">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-246">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-247">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-247">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="7d98d-248">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-248">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="7d98d-249">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="7d98d-249">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-250">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-250">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="7d98d-251">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-251">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="7d98d-252">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-252">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="7d98d-253">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-253">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="7d98d-254">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-254">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="7d98d-255">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-255">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="7d98d-256">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-256">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="7d98d-257">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-257">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="7d98d-258">public boolean multiLine(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-258">public boolean multiLine(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-259">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-259">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="7d98d-260">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-260">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="7d98d-261">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-261">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-262">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="7d98d-262">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-263">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="7d98d-263">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="7d98d-264">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-264">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7d98d-265">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="7d98d-265">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-266">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-266">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-267">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-267">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-268">public int replaceText(\[str findStr\], \[str replaceStr\], \[int start\], \[int end\], \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-268">public int replaceText(\[str findStr\], \[str replaceStr\], \[int start\], \[int end\], \[int flags\])</span></span>      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-269">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-269">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-270">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-270">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-271">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="7d98d-272">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-272">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="7d98d-273">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="7d98d-273">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="7d98d-274">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-274">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7d98d-275">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-275">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-276">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-276">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="7d98d-277">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-277">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="7d98d-278">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-278">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-279">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-279">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-280">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-280">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-281">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="7d98d-281">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="7d98d-282">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-282">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="7d98d-283">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-283">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="7d98d-284">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-284">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="7d98d-285">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-285">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="7d98d-286">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-286">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="7d98d-287">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-287">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="7d98d-288">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-288">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="7d98d-289">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-289">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-290">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-290">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-291">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="7d98d-291">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-292">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-292">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="7d98d-293">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-293">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="7d98d-294">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-294">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="7d98d-295">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-295">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="7d98d-296">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-296">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="7d98d-297">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-297">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="7d98d-298">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-298">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="7d98d-299">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-299">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="7d98d-300">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-300">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-301">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-301">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="7d98d-302">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-302">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="7d98d-303">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-303">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="7d98d-304">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-304">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="7d98d-305">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-305">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="7d98d-306">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-306">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="7d98d-307">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-307">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="7d98d-308">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-308">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7d98d-309">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-309">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="7d98d-310">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-310">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="7d98d-311">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-311">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="7d98d-312">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-312">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="7d98d-313">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-313">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="7d98d-314">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-314">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="7d98d-315">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-315">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="7d98d-316">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-316">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="7d98d-317">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="7d98d-317">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-318">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-318">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="7d98d-319">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-319">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7d98d-320">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-320">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="7d98d-321">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-321">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="7d98d-322">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-322">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="7d98d-323">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-323">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7d98d-324">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-324">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-325">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-325">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="7d98d-326">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-326">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="7d98d-327">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-327">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="7d98d-328">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-328">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="7d98d-329">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-329">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="7d98d-330">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-330">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="7d98d-331">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-331">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="7d98d-332">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-332">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="7d98d-333">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="7d98d-333">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-334">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="7d98d-334">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="7d98d-335">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-335">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="7d98d-336">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="7d98d-336">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="7d98d-337">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-337">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="7d98d-338">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="7d98d-338">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-339">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7d98d-339">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="7d98d-340">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-340">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="7d98d-341">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-341">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-342">public void paste()</span><span class="sxs-lookup"><span data-stu-id="7d98d-342">public void paste()</span></span>                                                                                         | <span data-ttu-id="7d98d-343">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-343">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7d98d-344">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="7d98d-344">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-345">public void undo()</span><span class="sxs-lookup"><span data-stu-id="7d98d-345">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-346">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="7d98d-346">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="7d98d-347">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-347">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7d98d-348">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-348">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-349">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7d98d-349">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="7d98d-350">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-350">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="7d98d-351">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="7d98d-351">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-352">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-352">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-353">public void context()</span><span class="sxs-lookup"><span data-stu-id="7d98d-353">public void context()</span></span>                                                                                       | <span data-ttu-id="7d98d-354">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-354">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7d98d-355">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-355">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-356">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-356">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-357">public void enter()</span><span class="sxs-lookup"><span data-stu-id="7d98d-357">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-358">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="7d98d-358">public void displayControl()</span></span>                                                                                | <span data-ttu-id="7d98d-359">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-359">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="7d98d-360">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-360">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-361">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-361">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-362">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7d98d-362">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-363">public void copy()</span><span class="sxs-lookup"><span data-stu-id="7d98d-363">public void copy()</span></span>                                                                                          | <span data-ttu-id="7d98d-364">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-364">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="7d98d-365">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-365">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-366">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="7d98d-366">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="7d98d-367">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-367">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="7d98d-368">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="7d98d-368">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-369">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-369">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-370">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-370">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-371">public void cut()</span><span class="sxs-lookup"><span data-stu-id="7d98d-371">public void cut()</span></span>                                                                                           | <span data-ttu-id="7d98d-372">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-372">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="7d98d-373">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="7d98d-373">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="7d98d-374">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-374">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="7d98d-375">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-375">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-376">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="7d98d-376">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-377">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="7d98d-377">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="7d98d-378">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-378">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="7d98d-379">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="7d98d-379">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="7d98d-380">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-380">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="7d98d-381">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-381">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-382">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7d98d-382">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="7d98d-383">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-383">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="7d98d-384">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="7d98d-384">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="7d98d-385">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-385">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="7d98d-386">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7d98d-386">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="7d98d-387">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="7d98d-387">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="7d98d-388">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-388">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="7d98d-389">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="7d98d-389">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="7d98d-390">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-390">Method alignControl</span></span>

<span data-ttu-id="7d98d-391">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-391">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="7d98d-392">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-392">Parameters - alignControl</span></span>

<span data-ttu-id="7d98d-393">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-393">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="7d98d-394">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-394">Return Value - alignControl</span></span>

<span data-ttu-id="7d98d-395">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-395">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="7d98d-396">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-396">Remarks - alignControl</span></span>

<span data-ttu-id="7d98d-397">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-397">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="7d98d-398">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="7d98d-398">Method allowEdit</span></span>

<span data-ttu-id="7d98d-399">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-399">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="7d98d-400">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7d98d-400">Parameters - allowEdit</span></span>

<span data-ttu-id="7d98d-401">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-401">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="7d98d-402">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7d98d-402">Return Value - allowEdit</span></span>

<span data-ttu-id="7d98d-403">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-403">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="7d98d-404">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7d98d-404">Remarks - allowEdit</span></span>

<span data-ttu-id="7d98d-405">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-405">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="7d98d-406">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="7d98d-406">Method allowSysSetup</span></span>

<span data-ttu-id="7d98d-407">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-407">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="7d98d-408">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="7d98d-408">Return Value - allowSysSetup</span></span>

<span data-ttu-id="7d98d-409">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-409">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="7d98d-410">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-410">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="7d98d-411">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-411">Parameters - arrayIndex</span></span>

<span data-ttu-id="7d98d-412">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-412">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="7d98d-413">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-413">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="7d98d-414">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7d98d-414">Method autoDeclaration</span></span>

<span data-ttu-id="7d98d-415">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-415">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="7d98d-416">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7d98d-416">Parameters - autoDeclaration</span></span>

<span data-ttu-id="7d98d-417">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-417">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="7d98d-418">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7d98d-418">Return Value - autoDeclaration</span></span>

<span data-ttu-id="7d98d-419">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-419">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="7d98d-420">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7d98d-420">Remarks - autoDeclaration</span></span>

<span data-ttu-id="7d98d-421">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-421">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="7d98d-422">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-422">Method backgroundColor</span></span>

<span data-ttu-id="7d98d-423">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-423">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="7d98d-424">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-424">Parameters - backgroundColor</span></span>

<span data-ttu-id="7d98d-425">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-425">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="7d98d-426">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-426">Return Value - backgroundColor</span></span>

<span data-ttu-id="7d98d-427">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="7d98d-427">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="7d98d-428">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-428">Remarks - backgroundColor</span></span>

<span data-ttu-id="7d98d-429">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-429">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="7d98d-430">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-430">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="7d98d-431">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-431">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="7d98d-432">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-432">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="7d98d-433">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-433">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="7d98d-434">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-434">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="7d98d-435">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="7d98d-435">Method backStyle</span></span>

<span data-ttu-id="7d98d-436">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-436">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="7d98d-437">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="7d98d-437">Parameters - backStyle</span></span>

<span data-ttu-id="7d98d-438">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-438">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="7d98d-439">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="7d98d-439">Return Value - backStyle</span></span>

<span data-ttu-id="7d98d-440">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-440">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="7d98d-441">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="7d98d-441">Method beginDrag</span></span>

<span data-ttu-id="7d98d-442">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-442">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="7d98d-443">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7d98d-443">Parameters - beginDrag</span></span>

<span data-ttu-id="7d98d-444">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-444">x</span></span>  
<span data-ttu-id="7d98d-445">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-445">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="7d98d-446">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-446">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="7d98d-447">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-447">y</span></span>  
<span data-ttu-id="7d98d-448">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-448">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="7d98d-449">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-449">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="7d98d-450">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7d98d-450">Return Value - beginDrag</span></span>

<span data-ttu-id="7d98d-451">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-451">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="7d98d-452">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7d98d-452">Remarks - beginDrag</span></span>

<span data-ttu-id="7d98d-453">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-453">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="7d98d-454">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-454">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="7d98d-455">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="7d98d-455">Method bold</span></span>

<span data-ttu-id="7d98d-456">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-456">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="7d98d-457">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="7d98d-457">Parameters - bold</span></span>

<span data-ttu-id="7d98d-458">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-458">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="7d98d-459">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="7d98d-459">Return Value - bold</span></span>

<span data-ttu-id="7d98d-460">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-460">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="7d98d-461">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="7d98d-461">Remarks - bold</span></span>

<span data-ttu-id="7d98d-462">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-462">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="7d98d-463">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-463">0 Use the default font weight.</span></span>
-   <span data-ttu-id="7d98d-464">1 シン。</span><span class="sxs-lookup"><span data-stu-id="7d98d-464">1 Thin.</span></span>
-   <span data-ttu-id="7d98d-465">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="7d98d-465">2 Extra-light.</span></span>
-   <span data-ttu-id="7d98d-466">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="7d98d-466">3 Light.</span></span>
-   <span data-ttu-id="7d98d-467">4 標準。</span><span class="sxs-lookup"><span data-stu-id="7d98d-467">4 Normal.</span></span>
-   <span data-ttu-id="7d98d-468">5 中。</span><span class="sxs-lookup"><span data-stu-id="7d98d-468">5 Medium.</span></span>
-   <span data-ttu-id="7d98d-469">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="7d98d-469">6 Semibold.</span></span>
-   <span data-ttu-id="7d98d-470">7 太字。</span><span class="sxs-lookup"><span data-stu-id="7d98d-470">7 Bold.</span></span>
-   <span data-ttu-id="7d98d-471">8 極太。</span><span class="sxs-lookup"><span data-stu-id="7d98d-471">8 Extra-bold.</span></span>
-   <span data-ttu-id="7d98d-472">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="7d98d-472">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="7d98d-473">メソッド border</span><span class="sxs-lookup"><span data-stu-id="7d98d-473">Method border</span></span>

<span data-ttu-id="7d98d-474">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-474">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="7d98d-475">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="7d98d-475">Parameters - border</span></span>

<span data-ttu-id="7d98d-476">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-476">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="7d98d-477">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="7d98d-477">Return Value - border</span></span>

<span data-ttu-id="7d98d-478">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="7d98d-478">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="7d98d-479">備考 - border</span><span class="sxs-lookup"><span data-stu-id="7d98d-479">Remarks - border</span></span>

<span data-ttu-id="7d98d-480">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-480">The integer that is returned contains the style of the borderline of the control as follows.</span></span>

| <span data-ttu-id="7d98d-481">先頭値</span><span class="sxs-lookup"><span data-stu-id="7d98d-481">Value</span></span> | <span data-ttu-id="7d98d-482">説明</span><span class="sxs-lookup"><span data-stu-id="7d98d-482">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="7d98d-483">0</span><span class="sxs-lookup"><span data-stu-id="7d98d-483">0</span></span>     | <span data-ttu-id="7d98d-484">自動</span><span class="sxs-lookup"><span data-stu-id="7d98d-484">Auto</span></span>        |
| <span data-ttu-id="7d98d-485">1</span><span class="sxs-lookup"><span data-stu-id="7d98d-485">1</span></span>     | <span data-ttu-id="7d98d-486">3D</span><span class="sxs-lookup"><span data-stu-id="7d98d-486">3D</span></span>          |
| <span data-ttu-id="7d98d-487">2</span><span class="sxs-lookup"><span data-stu-id="7d98d-487">2</span></span>     | <span data-ttu-id="7d98d-488">1 行</span><span class="sxs-lookup"><span data-stu-id="7d98d-488">Single line</span></span> |
| <span data-ttu-id="7d98d-489">3</span><span class="sxs-lookup"><span data-stu-id="7d98d-489">3</span></span>     | <span data-ttu-id="7d98d-490">集合住宅</span><span class="sxs-lookup"><span data-stu-id="7d98d-490">Flat</span></span>        |
| <span data-ttu-id="7d98d-491">4</span><span class="sxs-lookup"><span data-stu-id="7d98d-491">4</span></span>     | <span data-ttu-id="7d98d-492">None</span><span class="sxs-lookup"><span data-stu-id="7d98d-492">None</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="7d98d-493">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-493">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="7d98d-494">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-494">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="7d98d-495">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-495">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="7d98d-496">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-496">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="7d98d-497">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-497">Method calcControlSize</span></span>

<span data-ttu-id="7d98d-498">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-498">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="7d98d-499">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-499">Parameters - calcControlSize</span></span>

<span data-ttu-id="7d98d-500">chars</span><span class="sxs-lookup"><span data-stu-id="7d98d-500">chars</span></span>  
<span data-ttu-id="7d98d-501">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="7d98d-501">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="7d98d-502">明細行</span><span class="sxs-lookup"><span data-stu-id="7d98d-502">lines</span></span>  
<span data-ttu-id="7d98d-503">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="7d98d-503">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="7d98d-504">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-504">Return Value - calcControlSize</span></span>

<span data-ttu-id="7d98d-505">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="7d98d-505">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="7d98d-506">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="7d98d-506">Method characterSet</span></span>

<span data-ttu-id="7d98d-507">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-507">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="7d98d-508">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="7d98d-508">Parameters - characterSet</span></span>

<span data-ttu-id="7d98d-509">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-509">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="7d98d-510">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="7d98d-510">Return Value - characterSet</span></span>

<span data-ttu-id="7d98d-511">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-511">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="7d98d-512">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="7d98d-512">Remarks - characterSet</span></span>

<span data-ttu-id="7d98d-513">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-513">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="7d98d-514">先頭値</span><span class="sxs-lookup"><span data-stu-id="7d98d-514">Value</span></span> | <span data-ttu-id="7d98d-515">説明</span><span class="sxs-lookup"><span data-stu-id="7d98d-515">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="7d98d-516">0</span><span class="sxs-lookup"><span data-stu-id="7d98d-516">0</span></span>     | <span data-ttu-id="7d98d-517">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-517">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="7d98d-518">1</span><span class="sxs-lookup"><span data-stu-id="7d98d-518">1</span></span>     | <span data-ttu-id="7d98d-519">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-519">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="7d98d-520">2</span><span class="sxs-lookup"><span data-stu-id="7d98d-520">2</span></span>     | <span data-ttu-id="7d98d-521">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-521">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="7d98d-522">77</span><span class="sxs-lookup"><span data-stu-id="7d98d-522">77</span></span>    | <span data-ttu-id="7d98d-523">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-523">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="7d98d-524">128</span><span class="sxs-lookup"><span data-stu-id="7d98d-524">128</span></span>   | <span data-ttu-id="7d98d-525">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-525">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="7d98d-526">129</span><span class="sxs-lookup"><span data-stu-id="7d98d-526">129</span></span>   | <span data-ttu-id="7d98d-527">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-527">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="7d98d-528">134</span><span class="sxs-lookup"><span data-stu-id="7d98d-528">134</span></span>   | <span data-ttu-id="7d98d-529">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-529">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="7d98d-530">136</span><span class="sxs-lookup"><span data-stu-id="7d98d-530">136</span></span>   | <span data-ttu-id="7d98d-531">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-531">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="7d98d-532">161</span><span class="sxs-lookup"><span data-stu-id="7d98d-532">161</span></span>   | <span data-ttu-id="7d98d-533">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-533">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="7d98d-534">162</span><span class="sxs-lookup"><span data-stu-id="7d98d-534">162</span></span>   | <span data-ttu-id="7d98d-535">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-535">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="7d98d-536">163</span><span class="sxs-lookup"><span data-stu-id="7d98d-536">163</span></span>   | <span data-ttu-id="7d98d-537">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-537">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="7d98d-538">186</span><span class="sxs-lookup"><span data-stu-id="7d98d-538">186</span></span>   | <span data-ttu-id="7d98d-539">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-539">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="7d98d-540">204</span><span class="sxs-lookup"><span data-stu-id="7d98d-540">204</span></span>   | <span data-ttu-id="7d98d-541">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-541">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="7d98d-542">238</span><span class="sxs-lookup"><span data-stu-id="7d98d-542">238</span></span>   | <span data-ttu-id="7d98d-543">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-543">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="7d98d-544">255</span><span class="sxs-lookup"><span data-stu-id="7d98d-544">255</span></span>   | <span data-ttu-id="7d98d-545">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-545">OEM\_CHARSET</span></span>         |

<span data-ttu-id="7d98d-546">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-546">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="7d98d-547">金額</span><span class="sxs-lookup"><span data-stu-id="7d98d-547">Value</span></span> | <span data-ttu-id="7d98d-548">説明</span><span class="sxs-lookup"><span data-stu-id="7d98d-548">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="7d98d-549">130</span><span class="sxs-lookup"><span data-stu-id="7d98d-549">130</span></span>   | <span data-ttu-id="7d98d-550">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-550">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="7d98d-551">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-551">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="7d98d-552">先頭値</span><span class="sxs-lookup"><span data-stu-id="7d98d-552">Value</span></span> | <span data-ttu-id="7d98d-553">説明</span><span class="sxs-lookup"><span data-stu-id="7d98d-553">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="7d98d-554">177</span><span class="sxs-lookup"><span data-stu-id="7d98d-554">177</span></span>   | <span data-ttu-id="7d98d-555">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-555">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="7d98d-556">178</span><span class="sxs-lookup"><span data-stu-id="7d98d-556">178</span></span>   | <span data-ttu-id="7d98d-557">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-557">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="7d98d-558">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-558">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="7d98d-559">先頭値</span><span class="sxs-lookup"><span data-stu-id="7d98d-559">Value</span></span> | <span data-ttu-id="7d98d-560">説明</span><span class="sxs-lookup"><span data-stu-id="7d98d-560">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="7d98d-561">222</span><span class="sxs-lookup"><span data-stu-id="7d98d-561">222</span></span>   | <span data-ttu-id="7d98d-562">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7d98d-562">THAI\_CHARSET</span></span> |

<span data-ttu-id="7d98d-563">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-563">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="7d98d-564">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-564">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="7d98d-565">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d98d-565">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-charfrompos"></a><span data-ttu-id="7d98d-566">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="7d98d-566">Method charFromPos</span></span>

```xpp
public int charFromPos(int x, int y)
```

### <a name="parameters---charfrompos"></a><span data-ttu-id="7d98d-567">パラメーター - charFromPos</span><span class="sxs-lookup"><span data-stu-id="7d98d-567">Parameters - charFromPos</span></span>

<span data-ttu-id="7d98d-568">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-568">x</span></span>  

<!-- -->

<span data-ttu-id="7d98d-569">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-569">y</span></span>  

### <a name="return-value---charfrompos"></a><span data-ttu-id="7d98d-570">戻り値 - charFromPos</span><span class="sxs-lookup"><span data-stu-id="7d98d-570">Return Value - charFromPos</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="7d98d-571">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="7d98d-571">Method colorScheme</span></span>

<span data-ttu-id="7d98d-572">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-572">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="7d98d-573">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7d98d-573">Parameters - colorScheme</span></span>

<span data-ttu-id="7d98d-574">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-574">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="7d98d-575">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7d98d-575">Return Value - colorScheme</span></span>

<span data-ttu-id="7d98d-576">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="7d98d-576">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="7d98d-577">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7d98d-577">Remarks - colorScheme</span></span>

<span data-ttu-id="7d98d-578">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-578">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="7d98d-579">先頭値</span><span class="sxs-lookup"><span data-stu-id="7d98d-579">Value</span></span> | <span data-ttu-id="7d98d-580">スタイル</span><span class="sxs-lookup"><span data-stu-id="7d98d-580">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="7d98d-581">0</span><span class="sxs-lookup"><span data-stu-id="7d98d-581">0</span></span>     | <span data-ttu-id="7d98d-582">既定</span><span class="sxs-lookup"><span data-stu-id="7d98d-582">Default</span></span>               |
| <span data-ttu-id="7d98d-583">1</span><span class="sxs-lookup"><span data-stu-id="7d98d-583">1</span></span>     | <span data-ttu-id="7d98d-584">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="7d98d-584">The Windows palette</span></span>   |
| <span data-ttu-id="7d98d-585">2</span><span class="sxs-lookup"><span data-stu-id="7d98d-585">2</span></span>     | <span data-ttu-id="7d98d-586">真の配色</span><span class="sxs-lookup"><span data-stu-id="7d98d-586">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="7d98d-587">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="7d98d-587">Method configurationKey</span></span>

<span data-ttu-id="7d98d-588">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-588">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="7d98d-589">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7d98d-589">Parameters - configurationKey</span></span>

<span data-ttu-id="7d98d-590">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-590">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="7d98d-591">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7d98d-591">Return Value - configurationKey</span></span>

<span data-ttu-id="7d98d-592">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="7d98d-592">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="7d98d-593">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7d98d-593">Remarks - configurationKey</span></span>

<span data-ttu-id="7d98d-594">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-594">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="7d98d-595">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-595">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="7d98d-596">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-596">Method configurationKeyEx</span></span>

<span data-ttu-id="7d98d-597">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-597">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="7d98d-598">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-598">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="7d98d-599">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="7d98d-599">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="7d98d-600">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-600">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="7d98d-601">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-601">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="7d98d-602">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-602">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="7d98d-603">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-603">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="7d98d-604">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7d98d-604">Method countryRegionCodes</span></span>

<span data-ttu-id="7d98d-605">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-605">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="7d98d-606">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7d98d-606">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="7d98d-607">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-607">value</span></span>  
<span data-ttu-id="7d98d-608">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-608">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="7d98d-609">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7d98d-609">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="7d98d-610">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="7d98d-610">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="7d98d-611">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7d98d-611">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="7d98d-612">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7d98d-612">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="7d98d-613">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-613">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="7d98d-614">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7d98d-614">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="7d98d-615">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="7d98d-615">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="7d98d-616">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="7d98d-616">Parameters - dataField</span></span>

<span data-ttu-id="7d98d-617">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-617">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="7d98d-618">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="7d98d-618">Return Value - dataField</span></span>

## <a name="method-datafieldarrayindex"></a><span data-ttu-id="7d98d-619">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-619">Method dataFieldArrayIndex</span></span>

```xpp
public int dataFieldArrayIndex()
```

### <a name="return-value---datafieldarrayindex"></a><span data-ttu-id="7d98d-620">戻り値 - dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-620">Return Value - dataFieldArrayIndex</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="7d98d-621">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="7d98d-621">Method dataFieldName</span></span>

```xpp
public FieldName dataFieldName()
```

### <a name="return-value---datafieldname"></a><span data-ttu-id="7d98d-622">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="7d98d-622">Return Value - dataFieldName</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="7d98d-623">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-623">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="7d98d-624">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-624">Parameters - dataMethod</span></span>

<span data-ttu-id="7d98d-625">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-625">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="7d98d-626">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-626">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="7d98d-627">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7d98d-627">Method dataRelationPath</span></span>

<span data-ttu-id="7d98d-628">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-628">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="7d98d-629">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7d98d-629">Parameters - dataRelationPath</span></span>

<span data-ttu-id="7d98d-630">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-630">value</span></span>  
<span data-ttu-id="7d98d-631">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-631">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="7d98d-632">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7d98d-632">Return Value - dataRelationPath</span></span>

<span data-ttu-id="7d98d-633">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="7d98d-633">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="7d98d-634">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7d98d-634">Remarks - dataRelationPath</span></span>

<span data-ttu-id="7d98d-635">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-635">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="7d98d-636">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="7d98d-636">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="7d98d-637">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="7d98d-637">Method dataSource</span></span>

<span data-ttu-id="7d98d-638">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-638">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="7d98d-639">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="7d98d-639">Parameters - dataSource</span></span>

<span data-ttu-id="7d98d-640">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-640">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="7d98d-641">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="7d98d-641">Return Value - dataSource</span></span>

<span data-ttu-id="7d98d-642">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="7d98d-642">The identifier of the data source to be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="7d98d-643">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="7d98d-643">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="7d98d-644">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="7d98d-644">Parameters - direction</span></span>

<span data-ttu-id="7d98d-645">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-645">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="7d98d-646">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="7d98d-646">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="7d98d-647">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-647">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="7d98d-648">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-648">Parameters - displayHeight</span></span>

<span data-ttu-id="7d98d-649">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-649">value</span></span>  

<!-- -->

<span data-ttu-id="7d98d-650">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-650">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="7d98d-651">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-651">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="7d98d-652">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-652">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="7d98d-653">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-653">Parameters - displayHeightMode</span></span>

<span data-ttu-id="7d98d-654">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-654">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="7d98d-655">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-655">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="7d98d-656">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-656">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="7d98d-657">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-657">Parameters - displayHeightValue</span></span>

<span data-ttu-id="7d98d-658">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-658">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="7d98d-659">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-659">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="7d98d-660">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="7d98d-660">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="7d98d-661">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="7d98d-661">Parameters - displayLength</span></span>

<span data-ttu-id="7d98d-662">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-662">value</span></span>  

<!-- -->

<span data-ttu-id="7d98d-663">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-663">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="7d98d-664">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="7d98d-664">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="7d98d-665">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-665">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="7d98d-666">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-666">Parameters - displayLengthMode</span></span>

<span data-ttu-id="7d98d-667">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-667">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="7d98d-668">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-668">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="7d98d-669">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-669">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="7d98d-670">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-670">Parameters - displayLengthValue</span></span>

<span data-ttu-id="7d98d-671">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-671">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="7d98d-672">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-672">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="7d98d-673">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="7d98d-673">Method displayTarget</span></span>

<span data-ttu-id="7d98d-674">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-674">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="7d98d-675">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="7d98d-675">Parameters - displayTarget</span></span>

<span data-ttu-id="7d98d-676">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-676">value</span></span>  
<span data-ttu-id="7d98d-677">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-677">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="7d98d-678">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="7d98d-678">Return Value - displayTarget</span></span>

<span data-ttu-id="7d98d-679">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-679">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="7d98d-680">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="7d98d-680">Method dragDrop</span></span>

<span data-ttu-id="7d98d-681">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-681">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="7d98d-682">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7d98d-682">Parameters - dragDrop</span></span>

<span data-ttu-id="7d98d-683">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-683">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="7d98d-684">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7d98d-684">Return Value - dragDrop</span></span>

<span data-ttu-id="7d98d-685">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-685">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="7d98d-686">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="7d98d-686">Method dragOver</span></span>

<span data-ttu-id="7d98d-687">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-687">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="7d98d-688">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="7d98d-688">Parameters - dragOver</span></span>

<span data-ttu-id="7d98d-689">dragSource</span><span class="sxs-lookup"><span data-stu-id="7d98d-689">dragSource</span></span>  
<span data-ttu-id="7d98d-690">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-690">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-691">dragMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-691">dragMode</span></span>  
<span data-ttu-id="7d98d-692">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-692">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-693">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-693">x</span></span>  
<span data-ttu-id="7d98d-694">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-694">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-695">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-695">y</span></span>  
<span data-ttu-id="7d98d-696">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-696">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="7d98d-697">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="7d98d-697">Return Value - dragOver</span></span>

<span data-ttu-id="7d98d-698">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-698">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="7d98d-699">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-699">Method dragOverEx</span></span>

<span data-ttu-id="7d98d-700">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-700">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="7d98d-701">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-701">Parameters - dragOverEx</span></span>

<span data-ttu-id="7d98d-702">dragSource</span><span class="sxs-lookup"><span data-stu-id="7d98d-702">dragSource</span></span>  
<span data-ttu-id="7d98d-703">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-703">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-704">dragMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-704">dragMode</span></span>  
<span data-ttu-id="7d98d-705">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-705">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-706">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-706">x</span></span>  
<span data-ttu-id="7d98d-707">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-707">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-708">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-708">y</span></span>  
<span data-ttu-id="7d98d-709">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-709">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="7d98d-710">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-710">Return Value - dragOverEx</span></span>

<span data-ttu-id="7d98d-711">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-711">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="7d98d-712">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="7d98d-712">Method dragText</span></span>

<span data-ttu-id="7d98d-713">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-713">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="7d98d-714">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="7d98d-714">Return Value - dragText</span></span>

<span data-ttu-id="7d98d-715">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7d98d-715">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="7d98d-716">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-716">Method enabled</span></span>

<span data-ttu-id="7d98d-717">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-717">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="7d98d-718">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-718">Parameters - enabled</span></span>

<span data-ttu-id="7d98d-719">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-719">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="7d98d-720">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-720">Return Value - enabled</span></span>

<span data-ttu-id="7d98d-721">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-721">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="7d98d-722">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-722">Remarks - enabled</span></span>

<span data-ttu-id="7d98d-723">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-723">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="7d98d-724">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-724">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="7d98d-725">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-725">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="7d98d-726">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="7d98d-726">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="7d98d-727">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="7d98d-727">Parameters - extendedDataType</span></span>

<span data-ttu-id="7d98d-728">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-728">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="7d98d-729">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="7d98d-729">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="7d98d-730">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="7d98d-730">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="7d98d-731">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="7d98d-731">Parameters - fastTabSummary</span></span>

<span data-ttu-id="7d98d-732">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-732">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="7d98d-733">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="7d98d-733">Return Value - fastTabSummary</span></span>

## <a name="method-find"></a><span data-ttu-id="7d98d-734">メソッド find</span><span class="sxs-lookup"><span data-stu-id="7d98d-734">Method find</span></span>

```xpp
public int find([str findStr], [int start], [int end], [int flags])
```

### <a name="parameters---find"></a><span data-ttu-id="7d98d-735">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="7d98d-735">Parameters - find</span></span>

<span data-ttu-id="7d98d-736">findStr</span><span class="sxs-lookup"><span data-stu-id="7d98d-736">findStr</span></span>  

<!-- -->

<span data-ttu-id="7d98d-737">開始</span><span class="sxs-lookup"><span data-stu-id="7d98d-737">start</span></span>  

<!-- -->

<span data-ttu-id="7d98d-738">終了</span><span class="sxs-lookup"><span data-stu-id="7d98d-738">end</span></span>  

<!-- -->

<span data-ttu-id="7d98d-739">flags</span><span class="sxs-lookup"><span data-stu-id="7d98d-739">flags</span></span>  

### <a name="return-value---find"></a><span data-ttu-id="7d98d-740">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="7d98d-740">Return Value - find</span></span>

## <a name="method-font"></a><span data-ttu-id="7d98d-741">メソッド font</span><span class="sxs-lookup"><span data-stu-id="7d98d-741">Method font</span></span>

<span data-ttu-id="7d98d-742">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-742">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="7d98d-743">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="7d98d-743">Parameters - font</span></span>

<span data-ttu-id="7d98d-744">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-744">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="7d98d-745">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="7d98d-745">Return Value - font</span></span>

<span data-ttu-id="7d98d-746">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="7d98d-746">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="7d98d-747">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-747">Method fontSize</span></span>

<span data-ttu-id="7d98d-748">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-748">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="7d98d-749">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-749">Parameters - fontSize</span></span>

<span data-ttu-id="7d98d-750">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-750">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="7d98d-751">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-751">Return Value - fontSize</span></span>

<span data-ttu-id="7d98d-752">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="7d98d-752">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="7d98d-753">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-753">Method foregroundColor</span></span>

<span data-ttu-id="7d98d-754">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-754">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="7d98d-755">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-755">Parameters - foregroundColor</span></span>

<span data-ttu-id="7d98d-756">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-756">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="7d98d-757">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-757">Return Value - foregroundColor</span></span>

<span data-ttu-id="7d98d-758">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="7d98d-758">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="7d98d-759">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-759">Remarks - foregroundColor</span></span>

<span data-ttu-id="7d98d-760">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-760">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="7d98d-761">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-761">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="7d98d-762">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-762">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="7d98d-763">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7d98d-763">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="7d98d-764">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-764">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="7d98d-765">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-765">The maximum value for a single byte is 255.</span></span>

## <a name="method-getcursorpos"></a><span data-ttu-id="7d98d-766">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="7d98d-766">Method getCursorPos</span></span>

```xpp
public container getCursorPos()
```

### <a name="return-value---getcursorpos"></a><span data-ttu-id="7d98d-767">戻り値 - getCursorPos</span><span class="sxs-lookup"><span data-stu-id="7d98d-767">Return Value - getCursorPos</span></span>

## <a name="method-getfirstvisibleline"></a><span data-ttu-id="7d98d-768">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-768">Method getFirstVisibleLine</span></span>

```xpp
public int getFirstVisibleLine()
```

### <a name="return-value---getfirstvisibleline"></a><span data-ttu-id="7d98d-769">戻り値 - getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-769">Return Value - getFirstVisibleLine</span></span>

## <a name="method-getline"></a><span data-ttu-id="7d98d-770">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-770">Method getLine</span></span>

```xpp
public str getLine(int lineNo)
```

### <a name="parameters---getline"></a><span data-ttu-id="7d98d-771">パラメーター - getLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-771">Parameters - getLine</span></span>

<span data-ttu-id="7d98d-772">lineNo</span><span class="sxs-lookup"><span data-stu-id="7d98d-772">lineNo</span></span>  

### <a name="return-value---getline"></a><span data-ttu-id="7d98d-773">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-773">Return Value - getLine</span></span>

## <a name="method-getlinecount"></a><span data-ttu-id="7d98d-774">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="7d98d-774">Method getLineCount</span></span>

```xpp
public int getLineCount()
```

### <a name="return-value---getlinecount"></a><span data-ttu-id="7d98d-775">戻り値 - getLineCount</span><span class="sxs-lookup"><span data-stu-id="7d98d-775">Return Value - getLineCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="7d98d-776">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="7d98d-776">Method getSelection</span></span>

```xpp
public container getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="7d98d-777">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="7d98d-777">Return Value - getSelection</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="7d98d-778">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="7d98d-778">Method hasChanged</span></span>

<span data-ttu-id="7d98d-779">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-779">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="7d98d-780">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="7d98d-780">Parameters - hasChanged</span></span>

<span data-ttu-id="7d98d-781">val</span><span class="sxs-lookup"><span data-stu-id="7d98d-781">val</span></span>  
<span data-ttu-id="7d98d-782">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-782">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="7d98d-783">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="7d98d-783">Return Value - hasChanged</span></span>

<span data-ttu-id="7d98d-784">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-784">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="7d98d-785">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="7d98d-785">Method hasUserSetting</span></span>

<span data-ttu-id="7d98d-786">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-786">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="7d98d-787">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="7d98d-787">Return Value - hasUserSetting</span></span>

<span data-ttu-id="7d98d-788">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-788">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="7d98d-789">メソッド height</span><span class="sxs-lookup"><span data-stu-id="7d98d-789">Method height</span></span>

<span data-ttu-id="7d98d-790">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-790">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="7d98d-791">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="7d98d-791">Parameters - height</span></span>

<span data-ttu-id="7d98d-792">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-792">value</span></span>  

<!-- -->

<span data-ttu-id="7d98d-793">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-793">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="7d98d-794">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="7d98d-794">Return Value - height</span></span>

<span data-ttu-id="7d98d-795">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="7d98d-795">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="7d98d-796">備考 - height</span><span class="sxs-lookup"><span data-stu-id="7d98d-796">Remarks - height</span></span>

<span data-ttu-id="7d98d-797">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-797">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7d98d-798">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-798">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="7d98d-799">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-799">Mode</span></span>            | <span data-ttu-id="7d98d-800">高さの計算</span><span class="sxs-lookup"><span data-stu-id="7d98d-800">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d98d-801">-1 正確</span><span class="sxs-lookup"><span data-stu-id="7d98d-801">-1 Exact</span></span>        | <span data-ttu-id="7d98d-802">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-802">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7d98d-803">0 自動</span><span class="sxs-lookup"><span data-stu-id="7d98d-803">0 Auto</span></span>          | <span data-ttu-id="7d98d-804">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-804">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7d98d-805">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="7d98d-805">1 Column height</span></span> | <span data-ttu-id="7d98d-806">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-806">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7d98d-807">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-807">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="7d98d-808">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-808">Method heightMode</span></span>

<span data-ttu-id="7d98d-809">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-809">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="7d98d-810">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-810">Parameters - heightMode</span></span>

<span data-ttu-id="7d98d-811">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-811">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="7d98d-812">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-812">Return Value - heightMode</span></span>

<span data-ttu-id="7d98d-813">計算モード。</span><span class="sxs-lookup"><span data-stu-id="7d98d-813">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="7d98d-814">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-814">Remarks - heightMode</span></span>

<span data-ttu-id="7d98d-815">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="7d98d-815">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="7d98d-816">モード。</span><span class="sxs-lookup"><span data-stu-id="7d98d-816">Mode.</span></span>         | <span data-ttu-id="7d98d-817">高さの計算</span><span class="sxs-lookup"><span data-stu-id="7d98d-817">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d98d-818">正確</span><span class="sxs-lookup"><span data-stu-id="7d98d-818">Exact</span></span>         | <span data-ttu-id="7d98d-819">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-819">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7d98d-820">自動</span><span class="sxs-lookup"><span data-stu-id="7d98d-820">Auto</span></span>          | <span data-ttu-id="7d98d-821">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-821">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7d98d-822">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="7d98d-822">Column height</span></span> | <span data-ttu-id="7d98d-823">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-823">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7d98d-824">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-824">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="7d98d-825">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-825">Method heightValue</span></span>

<span data-ttu-id="7d98d-826">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-826">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="7d98d-827">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-827">Parameters - heightValue</span></span>

<span data-ttu-id="7d98d-828">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-828">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="7d98d-829">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-829">Return Value - heightValue</span></span>

<span data-ttu-id="7d98d-830">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="7d98d-830">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="7d98d-831">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-831">Remarks - heightValue</span></span>

<span data-ttu-id="7d98d-832">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-832">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="7d98d-833">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="7d98d-833">Method helpField</span></span>

<span data-ttu-id="7d98d-834">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-834">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="7d98d-835">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="7d98d-835">Return Value - helpField</span></span>

<span data-ttu-id="7d98d-836">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7d98d-836">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="7d98d-837">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="7d98d-837">Remarks - helpField</span></span>

<span data-ttu-id="7d98d-838">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-838">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="7d98d-839">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-839">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="7d98d-840">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7d98d-840">Method helpText</span></span>

<span data-ttu-id="7d98d-841">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-841">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="7d98d-842">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="7d98d-842">Parameters - helpText</span></span>

<span data-ttu-id="7d98d-843">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-843">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="7d98d-844">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="7d98d-844">Return Value - helpText</span></span>

<span data-ttu-id="7d98d-845">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7d98d-845">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="7d98d-846">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="7d98d-846">Remarks - helpText</span></span>

<span data-ttu-id="7d98d-847">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-847">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="7d98d-848">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-848">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="7d98d-849">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7d98d-849">Method hierarchyParent</span></span>

<span data-ttu-id="7d98d-850">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-850">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="7d98d-851">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7d98d-851">Parameters - hierarchyParent</span></span>

<span data-ttu-id="7d98d-852">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-852">value</span></span>  
<span data-ttu-id="7d98d-853">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-853">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="7d98d-854">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7d98d-854">Return Value - hierarchyParent</span></span>

<span data-ttu-id="7d98d-855">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-855">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="7d98d-856">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="7d98d-856">Method hWnd</span></span>

<span data-ttu-id="7d98d-857">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-857">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="7d98d-858">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="7d98d-858">Return Value - hWnd</span></span>

<span data-ttu-id="7d98d-859">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="7d98d-859">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="7d98d-860">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="7d98d-860">Remarks - hWnd</span></span>

<span data-ttu-id="7d98d-861">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-861">The handle can be used with the Windows API.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="7d98d-862">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-862">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="7d98d-863">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-863">Parameters - iMEMode</span></span>

<span data-ttu-id="7d98d-864">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-864">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="7d98d-865">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-865">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="7d98d-866">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="7d98d-866">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="7d98d-867">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="7d98d-867">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="7d98d-868">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7d98d-868">Method isDisplayed</span></span>

<span data-ttu-id="7d98d-869">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-869">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="7d98d-870">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7d98d-870">Return Value - isDisplayed</span></span>

<span data-ttu-id="7d98d-871">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-871">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="7d98d-872">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7d98d-872">Remarks - isDisplayed</span></span>

<span data-ttu-id="7d98d-873">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-873">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="7d98d-874">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="7d98d-874">Method isRestricted</span></span>

<span data-ttu-id="7d98d-875">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-875">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="7d98d-876">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="7d98d-876">Return Value - isRestricted</span></span>

<span data-ttu-id="7d98d-877">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-877">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="7d98d-878">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-878">Method isUserSetupEnabled</span></span>

<span data-ttu-id="7d98d-879">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-879">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="7d98d-880">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-880">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="7d98d-881">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="7d98d-881">neededSetupRights</span></span>  
<span data-ttu-id="7d98d-882">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-882">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="7d98d-883">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-883">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="7d98d-884">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-884">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="7d98d-885">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7d98d-885">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="7d98d-886">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-886">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d98d-887">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="7d98d-887">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="7d98d-888">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-888">No changes can be made to the control.</span></span> <span data-ttu-id="7d98d-889">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-889">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="7d98d-890">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="7d98d-890">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="7d98d-891">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-891">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="7d98d-892">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-892">The user cannot move the control.</span></span>   |
| <span data-ttu-id="7d98d-893">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="7d98d-893">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="7d98d-894">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-894">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="7d98d-895">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-895">The user can also move the control.</span></span> |

<span data-ttu-id="7d98d-896">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-896">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="7d98d-897">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="7d98d-897">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="7d98d-898">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="7d98d-898">Parameters - italic</span></span>

<span data-ttu-id="7d98d-899">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-899">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="7d98d-900">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="7d98d-900">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="7d98d-901">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7d98d-901">Method label</span></span>

<span data-ttu-id="7d98d-902">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-902">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="7d98d-903">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="7d98d-903">Parameters - label</span></span>

<span data-ttu-id="7d98d-904">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-904">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="7d98d-905">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="7d98d-905">Return Value - label</span></span>

<span data-ttu-id="7d98d-906">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-906">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="7d98d-907">備考 - label</span><span class="sxs-lookup"><span data-stu-id="7d98d-907">Remarks - label</span></span>

<span data-ttu-id="7d98d-908">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-908">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7d98d-909">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-909">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="7d98d-910">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="7d98d-910">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="7d98d-911">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="7d98d-911">Parameters - labelAlignment</span></span>

<span data-ttu-id="7d98d-912">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-912">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="7d98d-913">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="7d98d-913">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="7d98d-914">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="7d98d-914">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="7d98d-915">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="7d98d-915">Parameters - labelBold</span></span>

<span data-ttu-id="7d98d-916">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-916">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="7d98d-917">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="7d98d-917">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="7d98d-918">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="7d98d-918">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="7d98d-919">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="7d98d-919">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="7d98d-920">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-920">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="7d98d-921">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="7d98d-921">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="7d98d-922">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="7d98d-922">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="7d98d-923">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="7d98d-923">Parameters - labelFont</span></span>

<span data-ttu-id="7d98d-924">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-924">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="7d98d-925">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="7d98d-925">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="7d98d-926">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-926">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="7d98d-927">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-927">Parameters - labelFontSize</span></span>

<span data-ttu-id="7d98d-928">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-928">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="7d98d-929">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-929">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="7d98d-930">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-930">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="7d98d-931">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-931">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="7d98d-932">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-932">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="7d98d-933">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="7d98d-933">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="7d98d-934">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="7d98d-934">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="7d98d-935">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="7d98d-935">Parameters - labelGuide</span></span>

<span data-ttu-id="7d98d-936">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-936">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="7d98d-937">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="7d98d-937">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="7d98d-938">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-938">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="7d98d-939">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-939">Parameters - labelHeight</span></span>

<span data-ttu-id="7d98d-940">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-940">value</span></span>  

<!-- -->

<span data-ttu-id="7d98d-941">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-941">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="7d98d-942">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-942">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="7d98d-943">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-943">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="7d98d-944">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-944">Parameters - labelHeightMode</span></span>

<span data-ttu-id="7d98d-945">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-945">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="7d98d-946">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-946">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="7d98d-947">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-947">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="7d98d-948">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-948">Parameters - labelHeightValue</span></span>

<span data-ttu-id="7d98d-949">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-949">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="7d98d-950">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-950">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="7d98d-951">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="7d98d-951">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="7d98d-952">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="7d98d-952">Parameters - labelItalic</span></span>

<span data-ttu-id="7d98d-953">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-953">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="7d98d-954">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="7d98d-954">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="7d98d-955">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7d98d-955">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="7d98d-956">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7d98d-956">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="7d98d-957">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-957">x</span></span>  

<!-- -->

<span data-ttu-id="7d98d-958">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-958">y</span></span>  

<!-- -->

<span data-ttu-id="7d98d-959">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-959">button</span></span>  

<!-- -->

<span data-ttu-id="7d98d-960">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-960">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="7d98d-961">Shift</span><span class="sxs-lookup"><span data-stu-id="7d98d-961">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="7d98d-962">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7d98d-962">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="7d98d-963">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="7d98d-963">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="7d98d-964">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="7d98d-964">Parameters - labelMouseDown</span></span>

<span data-ttu-id="7d98d-965">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-965">x</span></span>  

<!-- -->

<span data-ttu-id="7d98d-966">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-966">y</span></span>  

<!-- -->

<span data-ttu-id="7d98d-967">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-967">button</span></span>  

<!-- -->

<span data-ttu-id="7d98d-968">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-968">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="7d98d-969">Shift</span><span class="sxs-lookup"><span data-stu-id="7d98d-969">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="7d98d-970">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="7d98d-970">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="7d98d-971">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="7d98d-971">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="7d98d-972">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="7d98d-972">Parameters - labelMouseUp</span></span>

<span data-ttu-id="7d98d-973">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-973">x</span></span>  

<!-- -->

<span data-ttu-id="7d98d-974">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-974">y</span></span>  

<!-- -->

<span data-ttu-id="7d98d-975">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-975">button</span></span>  

<!-- -->

<span data-ttu-id="7d98d-976">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-976">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="7d98d-977">Shift</span><span class="sxs-lookup"><span data-stu-id="7d98d-977">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="7d98d-978">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="7d98d-978">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="7d98d-979">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="7d98d-979">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="7d98d-980">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="7d98d-980">Parameters - labelPosition</span></span>

<span data-ttu-id="7d98d-981">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-981">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="7d98d-982">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="7d98d-982">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="7d98d-983">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="7d98d-983">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="7d98d-984">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="7d98d-984">Parameters - labelUnderline</span></span>

<span data-ttu-id="7d98d-985">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-985">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="7d98d-986">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="7d98d-986">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="7d98d-987">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="7d98d-987">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="7d98d-988">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="7d98d-988">Parameters - labelWidth</span></span>

<span data-ttu-id="7d98d-989">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-989">value</span></span>  

<!-- -->

<span data-ttu-id="7d98d-990">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-990">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="7d98d-991">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="7d98d-991">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="7d98d-992">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-992">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="7d98d-993">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-993">Parameters - labelWidthMode</span></span>

<span data-ttu-id="7d98d-994">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-994">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="7d98d-995">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-995">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="7d98d-996">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-996">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="7d98d-997">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-997">Parameters - labelWidthValue</span></span>

<span data-ttu-id="7d98d-998">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-998">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="7d98d-999">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-999">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="7d98d-1000">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="7d98d-1000">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="7d98d-1001">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="7d98d-1001">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="7d98d-1002">メソッド left</span><span class="sxs-lookup"><span data-stu-id="7d98d-1002">Method left</span></span>

<span data-ttu-id="7d98d-1003">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1003">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="7d98d-1004">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="7d98d-1004">Parameters - left</span></span>

<span data-ttu-id="7d98d-1005">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1005">value</span></span>  
<span data-ttu-id="7d98d-1006">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1006">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1007">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1007">mode</span></span>  
<span data-ttu-id="7d98d-1008">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1008">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="7d98d-1009">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="7d98d-1009">Return Value - left</span></span>

<span data-ttu-id="7d98d-1010">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1010">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="7d98d-1011">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1011">Method leftMode</span></span>

<span data-ttu-id="7d98d-1012">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1012">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="7d98d-1013">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1013">Parameters - leftMode</span></span>

<span data-ttu-id="7d98d-1014">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1014">value</span></span>  
<span data-ttu-id="7d98d-1015">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1015">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="7d98d-1016">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1016">Return Value - leftMode</span></span>

<span data-ttu-id="7d98d-1017">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1017">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="7d98d-1018">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1018">Method leftValue</span></span>

<span data-ttu-id="7d98d-1019">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1019">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="7d98d-1020">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1020">Parameters - leftValue</span></span>

<span data-ttu-id="7d98d-1021">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1021">value</span></span>  
<span data-ttu-id="7d98d-1022">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1022">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="7d98d-1023">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1023">Return Value - leftValue</span></span>

<span data-ttu-id="7d98d-1024">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1024">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="7d98d-1025">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1025">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="7d98d-1026">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1026">Parameters - limitText</span></span>

<span data-ttu-id="7d98d-1027">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1027">value</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1028">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1028">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="7d98d-1029">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1029">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="7d98d-1030">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1030">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="7d98d-1031">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1031">Parameters - limitTextMode</span></span>

<span data-ttu-id="7d98d-1032">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1032">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="7d98d-1033">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1033">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="7d98d-1034">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1034">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="7d98d-1035">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1035">Parameters - limitTextValue</span></span>

<span data-ttu-id="7d98d-1036">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1036">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="7d98d-1037">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1037">Return Value - limitTextValue</span></span>

## <a name="method-linefromchar"></a><span data-ttu-id="7d98d-1038">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="7d98d-1038">Method lineFromChar</span></span>

```xpp
public int lineFromChar(int charIndex)
```

### <a name="parameters---linefromchar"></a><span data-ttu-id="7d98d-1039">パラメーター - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="7d98d-1039">Parameters - lineFromChar</span></span>

<span data-ttu-id="7d98d-1040">charIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-1040">charIndex</span></span>  

### <a name="return-value---linefromchar"></a><span data-ttu-id="7d98d-1041">戻り値 - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="7d98d-1041">Return Value - lineFromChar</span></span>

## <a name="method-lineindex"></a><span data-ttu-id="7d98d-1042">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-1042">Method lineIndex</span></span>

```xpp
public int lineIndex(int lineNo)
```

### <a name="parameters---lineindex"></a><span data-ttu-id="7d98d-1043">パラメーター - lineIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-1043">Parameters - lineIndex</span></span>

<span data-ttu-id="7d98d-1044">lineNo</span><span class="sxs-lookup"><span data-stu-id="7d98d-1044">lineNo</span></span>  

### <a name="return-value---lineindex"></a><span data-ttu-id="7d98d-1045">戻り値 - lineIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-1045">Return Value - lineIndex</span></span>

## <a name="method-linelength"></a><span data-ttu-id="7d98d-1046">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="7d98d-1046">Method lineLength</span></span>

```xpp
public int lineLength(int lineNo)
```

### <a name="parameters---linelength"></a><span data-ttu-id="7d98d-1047">パラメーター - lineLength</span><span class="sxs-lookup"><span data-stu-id="7d98d-1047">Parameters - lineLength</span></span>

<span data-ttu-id="7d98d-1048">lineNo</span><span class="sxs-lookup"><span data-stu-id="7d98d-1048">lineNo</span></span>  

### <a name="return-value---linelength"></a><span data-ttu-id="7d98d-1049">戻り値 - lineLength</span><span class="sxs-lookup"><span data-stu-id="7d98d-1049">Return Value - lineLength</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="7d98d-1050">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="7d98d-1050">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="7d98d-1051">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="7d98d-1051">Parameters - lookupButton</span></span>

<span data-ttu-id="7d98d-1052">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1052">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="7d98d-1053">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="7d98d-1053">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="7d98d-1054">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="7d98d-1054">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="7d98d-1055">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="7d98d-1055">Parameters - mandatory</span></span>

<span data-ttu-id="7d98d-1056">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1056">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="7d98d-1057">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="7d98d-1057">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="7d98d-1058">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7d98d-1058">Method markAsUserAdd</span></span>

<span data-ttu-id="7d98d-1059">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1059">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="7d98d-1060">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7d98d-1060">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="7d98d-1061">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1061">value</span></span>  
<span data-ttu-id="7d98d-1062">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1062">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="7d98d-1063">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7d98d-1063">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="7d98d-1064">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1064">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="7d98d-1065">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="7d98d-1065">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="7d98d-1066">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="7d98d-1066">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="7d98d-1067">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7d98d-1067">Method mouseDblClick</span></span>

<span data-ttu-id="7d98d-1068">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1068">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="7d98d-1069">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7d98d-1069">Parameters - mouseDblClick</span></span>

<span data-ttu-id="7d98d-1070">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1070">x</span></span>  
<span data-ttu-id="7d98d-1071">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1071">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1072">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1072">y</span></span>  
<span data-ttu-id="7d98d-1073">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1073">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1074">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-1074">button</span></span>  
<span data-ttu-id="7d98d-1075">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1075">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1076">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1076">Ctrl</span></span>  
<span data-ttu-id="7d98d-1077">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1077">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1078">シフト</span><span class="sxs-lookup"><span data-stu-id="7d98d-1078">Shift</span></span>  
<span data-ttu-id="7d98d-1079">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1079">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="7d98d-1080">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7d98d-1080">Return Value - mouseDblClick</span></span>

<span data-ttu-id="7d98d-1081">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1081">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="7d98d-1082">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7d98d-1082">Remarks - mouseDblClick</span></span>

<span data-ttu-id="7d98d-1083">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1083">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="7d98d-1084">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="7d98d-1084">Method mouseDown</span></span>

<span data-ttu-id="7d98d-1085">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1085">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="7d98d-1086">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7d98d-1086">Parameters - mouseDown</span></span>

<span data-ttu-id="7d98d-1087">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1087">x</span></span>  
<span data-ttu-id="7d98d-1088">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1088">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1089">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1089">y</span></span>  
<span data-ttu-id="7d98d-1090">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1090">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1091">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-1091">button</span></span>  
<span data-ttu-id="7d98d-1092">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1092">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1093">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1093">Ctrl</span></span>  
<span data-ttu-id="7d98d-1094">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1094">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1095">シフト</span><span class="sxs-lookup"><span data-stu-id="7d98d-1095">Shift</span></span>  
<span data-ttu-id="7d98d-1096">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1096">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="7d98d-1097">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7d98d-1097">Return Value - mouseDown</span></span>

<span data-ttu-id="7d98d-1098">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1098">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="7d98d-1099">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7d98d-1099">Remarks - mouseDown</span></span>

<span data-ttu-id="7d98d-1100">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1100">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="7d98d-1101">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1101">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="7d98d-1102">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="7d98d-1102">Method mouseMove</span></span>

<span data-ttu-id="7d98d-1103">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1103">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="7d98d-1104">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7d98d-1104">Parameters - mouseMove</span></span>

<span data-ttu-id="7d98d-1105">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1105">x</span></span>  
<span data-ttu-id="7d98d-1106">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1106">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1107">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1107">y</span></span>  
<span data-ttu-id="7d98d-1108">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1108">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1109">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-1109">button</span></span>  
<span data-ttu-id="7d98d-1110">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1110">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1111">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1111">Ctrl</span></span>  
<span data-ttu-id="7d98d-1112">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1112">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1113">シフト</span><span class="sxs-lookup"><span data-stu-id="7d98d-1113">Shift</span></span>  
<span data-ttu-id="7d98d-1114">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1114">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="7d98d-1115">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7d98d-1115">Return Value - mouseMove</span></span>

<span data-ttu-id="7d98d-1116">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1116">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="7d98d-1117">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7d98d-1117">Remarks - mouseMove</span></span>

<span data-ttu-id="7d98d-1118">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1118">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="7d98d-1119">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="7d98d-1119">Method mouseUp</span></span>

<span data-ttu-id="7d98d-1120">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1120">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="7d98d-1121">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7d98d-1121">Parameters - mouseUp</span></span>

<span data-ttu-id="7d98d-1122">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1122">x</span></span>  
<span data-ttu-id="7d98d-1123">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1123">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1124">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1124">y</span></span>  
<span data-ttu-id="7d98d-1125">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1125">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1126">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-1126">button</span></span>  
<span data-ttu-id="7d98d-1127">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1127">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1128">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1128">Ctrl</span></span>  
<span data-ttu-id="7d98d-1129">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1129">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1130">シフト</span><span class="sxs-lookup"><span data-stu-id="7d98d-1130">Shift</span></span>  
<span data-ttu-id="7d98d-1131">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1131">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="7d98d-1132">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7d98d-1132">Return Value - mouseUp</span></span>

<span data-ttu-id="7d98d-1133">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1133">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="7d98d-1134">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7d98d-1134">Remarks - mouseUp</span></span>

<span data-ttu-id="7d98d-1135">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1135">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="7d98d-1136">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1136">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-multiline"></a><span data-ttu-id="7d98d-1137">メソッド multiLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-1137">Method multiLine</span></span>

```xpp
public boolean multiLine([boolean value])
```

### <a name="parameters---multiline"></a><span data-ttu-id="7d98d-1138">パラメーター - multiLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-1138">Parameters - multiLine</span></span>

<span data-ttu-id="7d98d-1139">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1139">value</span></span>  

### <a name="return-value---multiline"></a><span data-ttu-id="7d98d-1140">戻り値 - multiLine</span><span class="sxs-lookup"><span data-stu-id="7d98d-1140">Return Value - multiLine</span></span>

## <a name="method-name"></a><span data-ttu-id="7d98d-1141">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7d98d-1141">Method name</span></span>

<span data-ttu-id="7d98d-1142">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1142">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="7d98d-1143">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="7d98d-1143">Parameters - name</span></span>

<span data-ttu-id="7d98d-1144">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1144">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="7d98d-1145">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="7d98d-1145">Return Value - name</span></span>

<span data-ttu-id="7d98d-1146">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1146">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="7d98d-1147">備考 - name</span><span class="sxs-lookup"><span data-stu-id="7d98d-1147">Remarks - name</span></span>

<span data-ttu-id="7d98d-1148">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1148">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7d98d-1149">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1149">It must start with a letter.</span></span>
-   <span data-ttu-id="7d98d-1150">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1150">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="7d98d-1151">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1151">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="7d98d-1152">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1152">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7d98d-1153">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1153">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="7d98d-1154">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="7d98d-1154">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="7d98d-1155">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="7d98d-1155">Parameters - neededPermission</span></span>

<span data-ttu-id="7d98d-1156">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1156">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="7d98d-1157">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="7d98d-1157">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="7d98d-1158">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7d98d-1158">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="7d98d-1159">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7d98d-1159">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="7d98d-1160">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1160">Method parentControl</span></span>

<span data-ttu-id="7d98d-1161">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1161">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="7d98d-1162">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1162">Return Value - parentControl</span></span>

<span data-ttu-id="7d98d-1163">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1163">The parent control for the control.</span></span>

## <a name="method-posfromchar"></a><span data-ttu-id="7d98d-1164">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="7d98d-1164">Method posFromChar</span></span>

```xpp
public container posFromChar(int charIndex)
```

### <a name="parameters---posfromchar"></a><span data-ttu-id="7d98d-1165">パラメーター - posFromChar</span><span class="sxs-lookup"><span data-stu-id="7d98d-1165">Parameters - posFromChar</span></span>

<span data-ttu-id="7d98d-1166">charIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-1166">charIndex</span></span>  

### <a name="return-value---posfromchar"></a><span data-ttu-id="7d98d-1167">戻り値 - posFromChar</span><span class="sxs-lookup"><span data-stu-id="7d98d-1167">Return Value - posFromChar</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="7d98d-1168">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="7d98d-1168">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="7d98d-1169">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="7d98d-1169">Parameters - promptrect</span></span>

<span data-ttu-id="7d98d-1170">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1170">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="7d98d-1171">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="7d98d-1171">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="7d98d-1172">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1172">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="7d98d-1173">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1173">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="7d98d-1174">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1174">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="7d98d-1175">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1175">Return Value - replaceOnLookup</span></span>

## <a name="method-replacetext"></a><span data-ttu-id="7d98d-1176">メソッド replaceText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1176">Method replaceText</span></span>

```xpp
public int replaceText([str findStr], [str replaceStr], [int start], [int end], [int flags])
```

### <a name="parameters---replacetext"></a><span data-ttu-id="7d98d-1177">パラメーター - replaceText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1177">Parameters - replaceText</span></span>

<span data-ttu-id="7d98d-1178">findStr</span><span class="sxs-lookup"><span data-stu-id="7d98d-1178">findStr</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1179">replaceStr</span><span class="sxs-lookup"><span data-stu-id="7d98d-1179">replaceStr</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1180">開始</span><span class="sxs-lookup"><span data-stu-id="7d98d-1180">start</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1181">終了</span><span class="sxs-lookup"><span data-stu-id="7d98d-1181">end</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1182">flags</span><span class="sxs-lookup"><span data-stu-id="7d98d-1182">flags</span></span>  

### <a name="return-value---replacetext"></a><span data-ttu-id="7d98d-1183">戻り値 - replaceText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1183">Return Value - replaceText</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="7d98d-1184">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="7d98d-1184">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="7d98d-1185">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="7d98d-1185">Parameters - searchAfterInput</span></span>

<span data-ttu-id="7d98d-1186">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1186">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="7d98d-1187">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="7d98d-1187">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="7d98d-1188">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1188">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="7d98d-1189">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1189">Parameters - searchMode</span></span>

<span data-ttu-id="7d98d-1190">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1190">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="7d98d-1191">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1191">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="7d98d-1192">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="7d98d-1192">Method securityKey</span></span>

<span data-ttu-id="7d98d-1193">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1193">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="7d98d-1194">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="7d98d-1194">Parameters - securityKey</span></span>

<span data-ttu-id="7d98d-1195">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1195">value</span></span>  
<span data-ttu-id="7d98d-1196">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1196">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="7d98d-1197">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="7d98d-1197">Return Value - securityKey</span></span>

<span data-ttu-id="7d98d-1198">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1198">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="7d98d-1199">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7d98d-1199">Method showContextMenu</span></span>

<span data-ttu-id="7d98d-1200">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1200">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="7d98d-1201">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7d98d-1201">Parameters - showContextMenu</span></span>

<span data-ttu-id="7d98d-1202">menuHandle</span><span class="sxs-lookup"><span data-stu-id="7d98d-1202">menuHandle</span></span>  
<span data-ttu-id="7d98d-1203">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1203">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="7d98d-1204">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7d98d-1204">Return Value - showContextMenu</span></span>

<span data-ttu-id="7d98d-1205">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1205">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="7d98d-1206">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="7d98d-1206">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="7d98d-1207">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="7d98d-1207">Parameters - showLabel</span></span>

<span data-ttu-id="7d98d-1208">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1208">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="7d98d-1209">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="7d98d-1209">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="7d98d-1210">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1210">Method skip</span></span>

<span data-ttu-id="7d98d-1211">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1211">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="7d98d-1212">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1212">Parameters - skip</span></span>

<span data-ttu-id="7d98d-1213">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1213">value</span></span>  
<span data-ttu-id="7d98d-1214">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1214">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="7d98d-1215">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1215">Return Value - skip</span></span>

<span data-ttu-id="7d98d-1216">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1216">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="7d98d-1217">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1217">Remarks - skip</span></span>

<span data-ttu-id="7d98d-1218">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1218">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="7d98d-1219">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="7d98d-1219">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="7d98d-1220">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="7d98d-1220">Parameters - sort</span></span>

<span data-ttu-id="7d98d-1221">sortDirection</span><span class="sxs-lookup"><span data-stu-id="7d98d-1221">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="7d98d-1222">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="7d98d-1222">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="7d98d-1223">メソッド style</span><span class="sxs-lookup"><span data-stu-id="7d98d-1223">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="7d98d-1224">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="7d98d-1224">Parameters - style</span></span>

<span data-ttu-id="7d98d-1225">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1225">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="7d98d-1226">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="7d98d-1226">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="7d98d-1227">メソッド text</span><span class="sxs-lookup"><span data-stu-id="7d98d-1227">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="7d98d-1228">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="7d98d-1228">Parameters - text</span></span>

<span data-ttu-id="7d98d-1229">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1229">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="7d98d-1230">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="7d98d-1230">Return Value - text</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="7d98d-1231">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1231">Method toolTip</span></span>

<span data-ttu-id="7d98d-1232">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1232">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="7d98d-1233">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1233">Return Value - toolTip</span></span>

<span data-ttu-id="7d98d-1234">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1234">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="7d98d-1235">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1235">Remarks - toolTip</span></span>

<span data-ttu-id="7d98d-1236">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1236">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="7d98d-1237">メソッド top</span><span class="sxs-lookup"><span data-stu-id="7d98d-1237">Method top</span></span>

<span data-ttu-id="7d98d-1238">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1238">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="7d98d-1239">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="7d98d-1239">Parameters - top</span></span>

<span data-ttu-id="7d98d-1240">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1240">value</span></span>  
<span data-ttu-id="7d98d-1241">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1241">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1242">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1242">mode</span></span>  
<span data-ttu-id="7d98d-1243">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1243">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="7d98d-1244">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="7d98d-1244">Return Value - top</span></span>

<span data-ttu-id="7d98d-1245">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1245">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="7d98d-1246">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1246">Method topMode</span></span>

<span data-ttu-id="7d98d-1247">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1247">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="7d98d-1248">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1248">Parameters - topMode</span></span>

<span data-ttu-id="7d98d-1249">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1249">value</span></span>  
<span data-ttu-id="7d98d-1250">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1250">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="7d98d-1251">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1251">Return Value - topMode</span></span>

<span data-ttu-id="7d98d-1252">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1252">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="7d98d-1253">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1253">Method topValue</span></span>

<span data-ttu-id="7d98d-1254">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1254">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="7d98d-1255">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1255">Parameters - topValue</span></span>

<span data-ttu-id="7d98d-1256">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1256">value</span></span>  
<span data-ttu-id="7d98d-1257">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1257">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="7d98d-1258">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1258">Return Value - topValue</span></span>

<span data-ttu-id="7d98d-1259">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1259">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="7d98d-1260">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="7d98d-1260">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="7d98d-1261">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="7d98d-1261">Parameters - type</span></span>

<span data-ttu-id="7d98d-1262">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1262">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="7d98d-1263">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="7d98d-1263">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="7d98d-1264">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="7d98d-1264">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="7d98d-1265">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="7d98d-1265">Parameters - underline</span></span>

<span data-ttu-id="7d98d-1266">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1266">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="7d98d-1267">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="7d98d-1267">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="7d98d-1268">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7d98d-1268">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="7d98d-1269">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7d98d-1269">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="7d98d-1270">データ</span><span class="sxs-lookup"><span data-stu-id="7d98d-1270">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="7d98d-1271">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7d98d-1271">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="7d98d-1272">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="7d98d-1272">Method userData</span></span>

<span data-ttu-id="7d98d-1273">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1273">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="7d98d-1274">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="7d98d-1274">Parameters - userData</span></span>

<span data-ttu-id="7d98d-1275">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1275">value</span></span>  
<span data-ttu-id="7d98d-1276">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1276">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="7d98d-1277">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="7d98d-1277">Return Value - userData</span></span>

<span data-ttu-id="7d98d-1278">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1278">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="7d98d-1279">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="7d98d-1279">Method userDataItem</span></span>

<span data-ttu-id="7d98d-1280">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1280">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="7d98d-1281">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="7d98d-1281">Parameters - userDataItem</span></span>

<span data-ttu-id="7d98d-1282">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1282">value</span></span>  
<span data-ttu-id="7d98d-1283">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1283">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="7d98d-1284">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="7d98d-1284">Return Value - userDataItem</span></span>

<span data-ttu-id="7d98d-1285">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1285">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="7d98d-1286">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="7d98d-1286">Method userDataItems</span></span>

<span data-ttu-id="7d98d-1287">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1287">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="7d98d-1288">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="7d98d-1288">Parameters - userDataItems</span></span>

<span data-ttu-id="7d98d-1289">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1289">value</span></span>  
<span data-ttu-id="7d98d-1290">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1290">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="7d98d-1291">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="7d98d-1291">Return Value - userDataItems</span></span>

<span data-ttu-id="7d98d-1292">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1292">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="7d98d-1293">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="7d98d-1293">Method userDisable</span></span>

<span data-ttu-id="7d98d-1294">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1294">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="7d98d-1295">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="7d98d-1295">Parameters - userDisable</span></span>

<span data-ttu-id="7d98d-1296">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1296">value</span></span>  
<span data-ttu-id="7d98d-1297">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1297">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="7d98d-1298">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="7d98d-1298">Return Value - userDisable</span></span>

<span data-ttu-id="7d98d-1299">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1299">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="7d98d-1300">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="7d98d-1300">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="7d98d-1301">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="7d98d-1301">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="7d98d-1302">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1302">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="7d98d-1303">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="7d98d-1303">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="7d98d-1304">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-1304">Method userHeight</span></span>

<span data-ttu-id="7d98d-1305">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1305">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="7d98d-1306">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-1306">Parameters - userHeight</span></span>

<span data-ttu-id="7d98d-1307">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1307">value</span></span>  
<span data-ttu-id="7d98d-1308">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1308">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="7d98d-1309">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="7d98d-1309">Return Value - userHeight</span></span>

<span data-ttu-id="7d98d-1310">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1310">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="7d98d-1311">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="7d98d-1311">Method userHide</span></span>

<span data-ttu-id="7d98d-1312">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1312">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="7d98d-1313">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="7d98d-1313">Parameters - userHide</span></span>

<span data-ttu-id="7d98d-1314">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1314">value</span></span>  
<span data-ttu-id="7d98d-1315">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1315">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="7d98d-1316">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="7d98d-1316">Return Value - userHide</span></span>

<span data-ttu-id="7d98d-1317">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1317">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="7d98d-1318">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="7d98d-1318">Remarks - userHide</span></span>

<span data-ttu-id="7d98d-1319">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1319">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="7d98d-1320">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1320">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="7d98d-1321">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1321">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="7d98d-1322">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7d98d-1322">Method userOrgContainer</span></span>

<span data-ttu-id="7d98d-1323">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1323">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="7d98d-1324">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7d98d-1324">Parameters - userOrgContainer</span></span>

<span data-ttu-id="7d98d-1325">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1325">value</span></span>  
<span data-ttu-id="7d98d-1326">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1326">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="7d98d-1327">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7d98d-1327">Return Value - userOrgContainer</span></span>

<span data-ttu-id="7d98d-1328">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1328">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="7d98d-1329">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7d98d-1329">Method userOrgSibling</span></span>

<span data-ttu-id="7d98d-1330">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1330">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="7d98d-1331">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7d98d-1331">Parameters - userOrgSibling</span></span>

<span data-ttu-id="7d98d-1332">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1332">value</span></span>  
<span data-ttu-id="7d98d-1333">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1333">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="7d98d-1334">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7d98d-1334">Return Value - userOrgSibling</span></span>

<span data-ttu-id="7d98d-1335">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1335">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="7d98d-1336">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1336">Method userPromptText</span></span>

<span data-ttu-id="7d98d-1337">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1337">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="7d98d-1338">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1338">Parameters - userPromptText</span></span>

<span data-ttu-id="7d98d-1339">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1339">value</span></span>  
<span data-ttu-id="7d98d-1340">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1340">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="7d98d-1341">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1341">Return Value - userPromptText</span></span>

<span data-ttu-id="7d98d-1342">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1342">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="7d98d-1343">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7d98d-1343">Method userSecurityLevel</span></span>

<span data-ttu-id="7d98d-1344">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1344">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="7d98d-1345">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7d98d-1345">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="7d98d-1346">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1346">value</span></span>  
<span data-ttu-id="7d98d-1347">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1347">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="7d98d-1348">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7d98d-1348">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="7d98d-1349">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1349">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="7d98d-1350">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1350">Method userSkip</span></span>

<span data-ttu-id="7d98d-1351">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1351">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="7d98d-1352">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1352">Parameters - userSkip</span></span>

<span data-ttu-id="7d98d-1353">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1353">value</span></span>  
<span data-ttu-id="7d98d-1354">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1354">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="7d98d-1355">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1355">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="7d98d-1356">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="7d98d-1356">Return Value - userSkip</span></span>

<span data-ttu-id="7d98d-1357">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1357">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="7d98d-1358">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="7d98d-1358">Method userWidth</span></span>

<span data-ttu-id="7d98d-1359">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1359">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="7d98d-1360">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="7d98d-1360">Parameters - userWidth</span></span>

<span data-ttu-id="7d98d-1361">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1361">value</span></span>  
<span data-ttu-id="7d98d-1362">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1362">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="7d98d-1363">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="7d98d-1363">Return Value - userWidth</span></span>

<span data-ttu-id="7d98d-1364">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1364">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="7d98d-1365">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="7d98d-1365">Remarks - userWidth</span></span>

<span data-ttu-id="7d98d-1366">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1366">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="7d98d-1367">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1367">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="7d98d-1368">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1368">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="7d98d-1369">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="7d98d-1369">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="7d98d-1370">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="7d98d-1370">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="7d98d-1371">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7d98d-1371">Method verticalSpacing</span></span>

<span data-ttu-id="7d98d-1372">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1372">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="7d98d-1373">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7d98d-1373">Parameters - verticalSpacing</span></span>

<span data-ttu-id="7d98d-1374">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1374">value</span></span>  
<span data-ttu-id="7d98d-1375">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1375">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1376">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1376">mode</span></span>  
<span data-ttu-id="7d98d-1377">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1377">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="7d98d-1378">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7d98d-1378">Return Value - verticalSpacing</span></span>

<span data-ttu-id="7d98d-1379">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1379">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="7d98d-1380">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1380">Method verticalSpacingMode</span></span>

<span data-ttu-id="7d98d-1381">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1381">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="7d98d-1382">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1382">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="7d98d-1383">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1383">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="7d98d-1384">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1384">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="7d98d-1385">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1385">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="7d98d-1386">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1386">Method verticalSpacingValue</span></span>

<span data-ttu-id="7d98d-1387">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1387">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="7d98d-1388">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1388">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="7d98d-1389">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1389">value</span></span>  
<span data-ttu-id="7d98d-1390">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1390">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="7d98d-1391">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1391">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="7d98d-1392">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1392">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="7d98d-1393">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1393">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="7d98d-1394">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1394">Parameters - viewEditMode</span></span>

<span data-ttu-id="7d98d-1395">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1395">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="7d98d-1396">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1396">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="7d98d-1397">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="7d98d-1397">Method visible</span></span>

<span data-ttu-id="7d98d-1398">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1398">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="7d98d-1399">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="7d98d-1399">Parameters - visible</span></span>

<span data-ttu-id="7d98d-1400">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1400">value</span></span>  
<span data-ttu-id="7d98d-1401">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1401">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="7d98d-1402">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="7d98d-1402">Return Value - visible</span></span>

<span data-ttu-id="7d98d-1403">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1403">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="7d98d-1404">メソッド width</span><span class="sxs-lookup"><span data-stu-id="7d98d-1404">Method width</span></span>

<span data-ttu-id="7d98d-1405">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1405">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="7d98d-1406">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="7d98d-1406">Parameters - width</span></span>

<span data-ttu-id="7d98d-1407">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1407">value</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1408">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1408">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="7d98d-1409">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="7d98d-1409">Return Value - width</span></span>

<span data-ttu-id="7d98d-1410">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1410">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="7d98d-1411">備考 - width</span><span class="sxs-lookup"><span data-stu-id="7d98d-1411">Remarks - width</span></span>

<span data-ttu-id="7d98d-1412">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1412">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7d98d-1413">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1413">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="7d98d-1414">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1414">Mode</span></span>           | <span data-ttu-id="7d98d-1415">幅計算</span><span class="sxs-lookup"><span data-stu-id="7d98d-1415">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d98d-1416">-1 正確</span><span class="sxs-lookup"><span data-stu-id="7d98d-1416">-1 Exact</span></span>       | <span data-ttu-id="7d98d-1417">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1417">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7d98d-1418">0 自動</span><span class="sxs-lookup"><span data-stu-id="7d98d-1418">0 Auto</span></span>         | <span data-ttu-id="7d98d-1419">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1419">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7d98d-1420">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="7d98d-1420">1 Column width</span></span> | <span data-ttu-id="7d98d-1421">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1421">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7d98d-1422">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1422">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="7d98d-1423">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1423">Method widthMode</span></span>

<span data-ttu-id="7d98d-1424">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1424">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="7d98d-1425">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1425">Parameters - widthMode</span></span>

<span data-ttu-id="7d98d-1426">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1426">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="7d98d-1427">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1427">Return Value - widthMode</span></span>

<span data-ttu-id="7d98d-1428">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1428">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="7d98d-1429">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1429">Remarks - widthMode</span></span>

<span data-ttu-id="7d98d-1430">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1430">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="7d98d-1431">モード</span><span class="sxs-lookup"><span data-stu-id="7d98d-1431">Mode</span></span>         | <span data-ttu-id="7d98d-1432">幅計算</span><span class="sxs-lookup"><span data-stu-id="7d98d-1432">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d98d-1433">正確</span><span class="sxs-lookup"><span data-stu-id="7d98d-1433">Exact</span></span>        | <span data-ttu-id="7d98d-1434">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1434">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7d98d-1435">自動</span><span class="sxs-lookup"><span data-stu-id="7d98d-1435">Auto</span></span>         | <span data-ttu-id="7d98d-1436">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1436">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7d98d-1437">列の幅</span><span class="sxs-lookup"><span data-stu-id="7d98d-1437">Column width</span></span> | <span data-ttu-id="7d98d-1438">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1438">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7d98d-1439">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1439">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="7d98d-1440">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1440">Method widthValue</span></span>

<span data-ttu-id="7d98d-1441">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1441">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="7d98d-1442">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1442">Parameters - widthValue</span></span>

<span data-ttu-id="7d98d-1443">値</span><span class="sxs-lookup"><span data-stu-id="7d98d-1443">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="7d98d-1444">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1444">Return Value - widthValue</span></span>

<span data-ttu-id="7d98d-1445">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1445">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="7d98d-1446">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7d98d-1446">Remarks - widthValue</span></span>

<span data-ttu-id="7d98d-1447">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1447">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-lookup"></a><span data-ttu-id="7d98d-1448">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1448">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="7d98d-1449">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-1449">Method prefColumnSize</span></span>

<span data-ttu-id="7d98d-1450">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1450">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="7d98d-1451">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="7d98d-1451">Parameters - prefColumnSize</span></span>

<span data-ttu-id="7d98d-1452">width</span><span class="sxs-lookup"><span data-stu-id="7d98d-1452">width</span></span>  
<span data-ttu-id="7d98d-1453">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1453">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1454">height</span><span class="sxs-lookup"><span data-stu-id="7d98d-1454">height</span></span>  
<span data-ttu-id="7d98d-1455">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1455">The preferred height of the control.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="7d98d-1456">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="7d98d-1456">Method endDrag</span></span>

<span data-ttu-id="7d98d-1457">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1457">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="7d98d-1458">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="7d98d-1458">Remarks - endDrag</span></span>

<span data-ttu-id="7d98d-1459">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1459">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="7d98d-1460">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1460">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-performformlookup"></a><span data-ttu-id="7d98d-1461">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1461">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="7d98d-1462">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1462">Parameters - performFormLookup</span></span>

<span data-ttu-id="7d98d-1463">フォーム</span><span class="sxs-lookup"><span data-stu-id="7d98d-1463">form</span></span>  

## <a name="method-drop"></a><span data-ttu-id="7d98d-1464">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="7d98d-1464">Method drop</span></span>

<span data-ttu-id="7d98d-1465">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1465">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="7d98d-1466">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="7d98d-1466">Parameters - drop</span></span>

<span data-ttu-id="7d98d-1467">dragSource</span><span class="sxs-lookup"><span data-stu-id="7d98d-1467">dragSource</span></span>  
<span data-ttu-id="7d98d-1468">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1468">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1469">dragMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1469">dragMode</span></span>  
<span data-ttu-id="7d98d-1470">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1470">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1471">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1471">x</span></span>  
<span data-ttu-id="7d98d-1472">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1472">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1473">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1473">y</span></span>  
<span data-ttu-id="7d98d-1474">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1474">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onlookup"></a><span data-ttu-id="7d98d-1475">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1475">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="7d98d-1476">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1476">Parameters - OnLookup</span></span>

<span data-ttu-id="7d98d-1477">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1477">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1478">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1478">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="7d98d-1479">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="7d98d-1479">Method paste</span></span>

<span data-ttu-id="7d98d-1480">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1480">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-scrollcursor"></a><span data-ttu-id="7d98d-1481">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="7d98d-1481">Method scrollCursor</span></span>

```xpp
public void scrollCursor()
```

## <a name="method-undo"></a><span data-ttu-id="7d98d-1482">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="7d98d-1482">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-mouseleave"></a><span data-ttu-id="7d98d-1483">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="7d98d-1483">Method mouseLeave</span></span>

<span data-ttu-id="7d98d-1484">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1484">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-onmodified"></a><span data-ttu-id="7d98d-1485">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="7d98d-1485">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="7d98d-1486">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="7d98d-1486">Parameters - OnModified</span></span>

<span data-ttu-id="7d98d-1487">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1487">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1488">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1488">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="7d98d-1489">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-1489">Method dropEx</span></span>

<span data-ttu-id="7d98d-1490">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1490">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="7d98d-1491">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="7d98d-1491">Parameters - dropEx</span></span>

<span data-ttu-id="7d98d-1492">dragSource</span><span class="sxs-lookup"><span data-stu-id="7d98d-1492">dragSource</span></span>  
<span data-ttu-id="7d98d-1493">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1493">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1494">dragMode</span><span class="sxs-lookup"><span data-stu-id="7d98d-1494">dragMode</span></span>  
<span data-ttu-id="7d98d-1495">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1495">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1496">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1496">x</span></span>  
<span data-ttu-id="7d98d-1497">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1497">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1498">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1498">y</span></span>  
<span data-ttu-id="7d98d-1499">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1499">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-setselection"></a><span data-ttu-id="7d98d-1500">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="7d98d-1500">Method setSelection</span></span>

```xpp
public void setSelection(int charIndexFrom, int charIndexTo)
```

### <a name="parameters---setselection"></a><span data-ttu-id="7d98d-1501">パラメーター - setSelection</span><span class="sxs-lookup"><span data-stu-id="7d98d-1501">Parameters - setSelection</span></span>

<span data-ttu-id="7d98d-1502">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="7d98d-1502">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1503">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="7d98d-1503">charIndexTo</span></span>  

## <a name="method-pastetext"></a><span data-ttu-id="7d98d-1504">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1504">Method pasteText</span></span>

```xpp
public void pasteText(str pasteStr, [boolean InsertSel])
```

### <a name="parameters---pastetext"></a><span data-ttu-id="7d98d-1505">パラメーター - pasteText</span><span class="sxs-lookup"><span data-stu-id="7d98d-1505">Parameters - pasteText</span></span>

<span data-ttu-id="7d98d-1506">pasteStr</span><span class="sxs-lookup"><span data-stu-id="7d98d-1506">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1507">InsertSel</span><span class="sxs-lookup"><span data-stu-id="7d98d-1507">InsertSel</span></span>  

## <a name="method-context"></a><span data-ttu-id="7d98d-1508">メソッド context</span><span class="sxs-lookup"><span data-stu-id="7d98d-1508">Method context</span></span>

<span data-ttu-id="7d98d-1509">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1509">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-onenter"></a><span data-ttu-id="7d98d-1510">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="7d98d-1510">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="7d98d-1511">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="7d98d-1511">Parameters - OnEnter</span></span>

<span data-ttu-id="7d98d-1512">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1512">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1513">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1513">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="7d98d-1514">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="7d98d-1514">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="7d98d-1515">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="7d98d-1515">Parameters - filter</span></span>

<span data-ttu-id="7d98d-1516">filterStr</span><span class="sxs-lookup"><span data-stu-id="7d98d-1516">filterStr</span></span>  

## <a name="method-enter"></a><span data-ttu-id="7d98d-1517">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="7d98d-1517">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="7d98d-1518">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1518">Method displayControl</span></span>

<span data-ttu-id="7d98d-1519">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1519">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-performtypelookup"></a><span data-ttu-id="7d98d-1520">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1520">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="7d98d-1521">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1521">Parameters - performTypeLookup</span></span>

<span data-ttu-id="7d98d-1522">userType</span><span class="sxs-lookup"><span data-stu-id="7d98d-1522">userType</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1523">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7d98d-1523">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1524">会社</span><span class="sxs-lookup"><span data-stu-id="7d98d-1524">company</span></span>  

## <a name="method-onvalidating"></a><span data-ttu-id="7d98d-1525">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="7d98d-1525">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="7d98d-1526">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="7d98d-1526">Parameters - OnValidating</span></span>

<span data-ttu-id="7d98d-1527">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1527">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1528">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1528">e</span></span>  

## <a name="method-setcursorpos"></a><span data-ttu-id="7d98d-1529">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="7d98d-1529">Method setCursorPos</span></span>

```xpp
public void setCursorPos(int x, int y)
```

### <a name="parameters---setcursorpos"></a><span data-ttu-id="7d98d-1530">パラメーター - setCursorPos</span><span class="sxs-lookup"><span data-stu-id="7d98d-1530">Parameters - setCursorPos</span></span>

<span data-ttu-id="7d98d-1531">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1531">x</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1532">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1532">y</span></span>  

## <a name="method-copy"></a><span data-ttu-id="7d98d-1533">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="7d98d-1533">Method copy</span></span>

<span data-ttu-id="7d98d-1534">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1534">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-onleaving"></a><span data-ttu-id="7d98d-1535">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="7d98d-1535">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="7d98d-1536">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="7d98d-1536">Parameters - OnLeaving</span></span>

<span data-ttu-id="7d98d-1537">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1537">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1538">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1538">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="7d98d-1539">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="7d98d-1539">Method dragLeave</span></span>

<span data-ttu-id="7d98d-1540">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1540">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-linescroll"></a><span data-ttu-id="7d98d-1541">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="7d98d-1541">Method lineScroll</span></span>

```xpp
public void lineScroll(int dx, int dy)
```

### <a name="parameters---linescroll"></a><span data-ttu-id="7d98d-1542">パラメーター - lineScroll</span><span class="sxs-lookup"><span data-stu-id="7d98d-1542">Parameters - lineScroll</span></span>

<span data-ttu-id="7d98d-1543">dx</span><span class="sxs-lookup"><span data-stu-id="7d98d-1543">dx</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1544">dy</span><span class="sxs-lookup"><span data-stu-id="7d98d-1544">dy</span></span>  

## <a name="method-ongotfocus"></a><span data-ttu-id="7d98d-1545">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="7d98d-1545">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="7d98d-1546">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="7d98d-1546">Parameters - OnGotFocus</span></span>

<span data-ttu-id="7d98d-1547">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1547">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1548">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1548">e</span></span>  

## <a name="method-performdblookup"></a><span data-ttu-id="7d98d-1549">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1549">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="7d98d-1550">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="7d98d-1550">Parameters - performDBLookup</span></span>

<span data-ttu-id="7d98d-1551">fieldId</span><span class="sxs-lookup"><span data-stu-id="7d98d-1551">fieldId</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1552">tableId</span><span class="sxs-lookup"><span data-stu-id="7d98d-1552">tableId</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1553">会社</span><span class="sxs-lookup"><span data-stu-id="7d98d-1553">company</span></span>  

## <a name="method-cut"></a><span data-ttu-id="7d98d-1554">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="7d98d-1554">Method cut</span></span>

<span data-ttu-id="7d98d-1555">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1555">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-lostfocus"></a><span data-ttu-id="7d98d-1556">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="7d98d-1556">Method lostFocus</span></span>

<span data-ttu-id="7d98d-1557">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1557">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="7d98d-1558">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-1558">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="7d98d-1559">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="7d98d-1559">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="7d98d-1560">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="7d98d-1560">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1561">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="7d98d-1561">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1562">overrideObject</span><span class="sxs-lookup"><span data-stu-id="7d98d-1562">overrideObject</span></span>  

## <a name="method-textchange"></a><span data-ttu-id="7d98d-1563">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="7d98d-1563">Method textChange</span></span>

```xpp
public void textChange()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="7d98d-1564">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="7d98d-1564">Method resetUserSetting</span></span>

<span data-ttu-id="7d98d-1565">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1565">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-inputsearch"></a><span data-ttu-id="7d98d-1566">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="7d98d-1566">Method inputSearch</span></span>

<span data-ttu-id="7d98d-1567">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1567">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="7d98d-1568">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="7d98d-1568">Parameters - inputSearch</span></span>

<span data-ttu-id="7d98d-1569">searchStr</span><span class="sxs-lookup"><span data-stu-id="7d98d-1569">searchStr</span></span>  
<span data-ttu-id="7d98d-1570">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1570">The string value to use to filter data; optional.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="7d98d-1571">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="7d98d-1571">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="7d98d-1572">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="7d98d-1572">Parameters - OnLostFocus</span></span>

<span data-ttu-id="7d98d-1573">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1573">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1574">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1574">e</span></span>  

## <a name="method-mouseenter"></a><span data-ttu-id="7d98d-1575">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="7d98d-1575">Method mouseEnter</span></span>

<span data-ttu-id="7d98d-1576">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1576">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="7d98d-1577">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="7d98d-1577">Parameters - mouseEnter</span></span>

<span data-ttu-id="7d98d-1578">x</span><span class="sxs-lookup"><span data-stu-id="7d98d-1578">x</span></span>  
<span data-ttu-id="7d98d-1579">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1579">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1580">y</span><span class="sxs-lookup"><span data-stu-id="7d98d-1580">y</span></span>  
<span data-ttu-id="7d98d-1581">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1581">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1582">ボタン</span><span class="sxs-lookup"><span data-stu-id="7d98d-1582">button</span></span>  
<span data-ttu-id="7d98d-1583">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1583">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1584">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7d98d-1584">Ctrl</span></span>  
<span data-ttu-id="7d98d-1585">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1585">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7d98d-1586">シフト</span><span class="sxs-lookup"><span data-stu-id="7d98d-1586">Shift</span></span>  
<span data-ttu-id="7d98d-1587">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1587">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="7d98d-1588">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="7d98d-1588">Method gotFocus</span></span>

<span data-ttu-id="7d98d-1589">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1589">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-onvalidated"></a><span data-ttu-id="7d98d-1590">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="7d98d-1590">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="7d98d-1591">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="7d98d-1591">Parameters - OnValidated</span></span>

<span data-ttu-id="7d98d-1592">sender</span><span class="sxs-lookup"><span data-stu-id="7d98d-1592">sender</span></span>  

<!-- -->

<span data-ttu-id="7d98d-1593">e</span><span class="sxs-lookup"><span data-stu-id="7d98d-1593">e</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="7d98d-1594">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="7d98d-1594">Method setFocus</span></span>

<span data-ttu-id="7d98d-1595">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="7d98d-1595">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-jumpref"></a><span data-ttu-id="7d98d-1596">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="7d98d-1596">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

