---
title: FormRealControl クラス
description: このトピックでは、FormRealControl クラスについて説明します。
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
ms.openlocfilehash: 05baba0ca2084b11feb9cbf3d5f401e389922f0b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502919"
---
# <a name="class-formrealcontrol"></a><span data-ttu-id="6bf00-103">クラス FormRealControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-103">Class FormRealControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormRealControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="6bf00-104">備考</span><span class="sxs-lookup"><span data-stu-id="6bf00-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="6bf00-105">例</span><span class="sxs-lookup"><span data-stu-id="6bf00-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6bf00-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="6bf00-106">Methods</span></span>

| <span data-ttu-id="6bf00-107">方法</span><span class="sxs-lookup"><span data-stu-id="6bf00-107">Method</span></span>                                                                                                      | <span data-ttu-id="6bf00-108">説明</span><span class="sxs-lookup"><span data-stu-id="6bf00-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf00-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="6bf00-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="6bf00-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="6bf00-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="6bf00-114">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-114">public int allowNegative(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-115">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="6bf00-115">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="6bf00-116">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-116">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="6bf00-117">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-117">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="6bf00-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="6bf00-120">public int autoInsSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-120">public int autoInsSeparator(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-121">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-121">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="6bf00-122">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-122">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="6bf00-123">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-123">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="6bf00-124">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-124">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="6bf00-125">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6bf00-125">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="6bf00-126">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-126">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="6bf00-127">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-127">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="6bf00-128">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-128">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                                             |
| <span data-ttu-id="6bf00-129">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-129">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="6bf00-130">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-130">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="6bf00-131">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-131">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-132">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="6bf00-132">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="6bf00-133">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-133">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="6bf00-134">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-134">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="6bf00-135">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-135">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="6bf00-136">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6bf00-136">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-137">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-137">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="6bf00-138">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-138">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="6bf00-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="6bf00-140">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-140">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="6bf00-141">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="6bf00-141">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="6bf00-142">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-142">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="6bf00-143">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-143">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="6bf00-144">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-144">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="6bf00-145">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-145">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-146">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-146">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-147">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="6bf00-147">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-148">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="6bf00-148">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-149">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-149">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-150">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-150">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="6bf00-151">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-151">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="6bf00-152">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-152">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="6bf00-153">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-153">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="6bf00-154">public int decimalSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-154">public int decimalSeparator(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-155">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-155">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-156">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-156">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>                                               |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-157">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-157">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-158">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-158">public int displaceNegativeValue(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-159">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-159">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-160">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-160">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-161">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-161">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-162">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-162">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-163">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-163">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-164">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-164">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-165">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-165">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="6bf00-166">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-166">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="6bf00-167">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-167">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bf00-168">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-168">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                        |
| <span data-ttu-id="6bf00-169">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6bf00-169">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="6bf00-170">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-170">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="6bf00-171">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6bf00-171">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="6bf00-172">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-172">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="6bf00-173">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="6bf00-173">public str dragText()</span></span>                                                                                       | <span data-ttu-id="6bf00-174">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-174">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="6bf00-175">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-175">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="6bf00-176">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-176">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="6bf00-177">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-177">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-178">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-178">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-179">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-179">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="6bf00-180">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-180">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="6bf00-181">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-181">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bf00-182">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-182">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="6bf00-183">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-183">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="6bf00-184">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-184">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="6bf00-185">public int formatMST(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-185">public int formatMST(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-186">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="6bf00-186">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-187">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="6bf00-187">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-188">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="6bf00-188">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-189">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="6bf00-189">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-190">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="6bf00-190">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-191">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-191">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="6bf00-192">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-192">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="6bf00-193">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="6bf00-193">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="6bf00-194">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-194">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="6bf00-195">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-195">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="6bf00-196">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-196">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="6bf00-197">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-197">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="6bf00-198">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-198">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="6bf00-199">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-199">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="6bf00-200">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-200">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="6bf00-201">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="6bf00-201">public str helpField()</span></span>                                                                                      | <span data-ttu-id="6bf00-202">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-202">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="6bf00-203">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-203">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="6bf00-204">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-204">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="6bf00-205">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-205">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="6bf00-206">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-206">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="6bf00-207">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="6bf00-207">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="6bf00-208">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-208">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="6bf00-209">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-209">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-210">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="6bf00-210">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-211">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="6bf00-211">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="6bf00-212">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-212">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="6bf00-213">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="6bf00-213">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="6bf00-214">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-214">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="6bf00-215">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="6bf00-215">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="6bf00-216">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-216">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="6bf00-217">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="6bf00-217">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-218">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-218">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-219">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-219">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="6bf00-220">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-220">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="6bf00-221">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-221">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-222">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-222">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-223">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-223">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-224">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-224">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-225">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-225">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-226">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-226">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-227">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-227">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-228">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-228">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-229">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-229">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-230">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-230">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-231">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-231">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-232">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-232">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-233">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-233">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-234">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-234">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-235">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-235">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-236">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-236">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-237">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-237">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-238">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-238">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-239">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-239">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-240">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="6bf00-240">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-241">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-241">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="6bf00-242">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-242">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="6bf00-243">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-243">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bf00-244">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-244">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="6bf00-245">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-245">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="6bf00-246">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-246">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="6bf00-247">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-247">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-248">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-248">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-249">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-249">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-250">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="6bf00-250">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-251">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="6bf00-251">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-252">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="6bf00-252">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-253">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-253">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-254">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-254">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-255">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-255">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="6bf00-256">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-256">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="6bf00-257">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-257">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-258">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-258">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-259">public int minNoOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-259">public int minNoOfDecimalsValue(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-260">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="6bf00-260">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-261">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-261">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="6bf00-262">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-262">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="6bf00-263">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-263">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="6bf00-264">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-264">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="6bf00-265">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-265">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="6bf00-266">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-266">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="6bf00-267">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-267">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="6bf00-268">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-268">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="6bf00-269">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-269">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="6bf00-270">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-270">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="6bf00-271">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-271">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-272">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-272">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-273">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-273">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-274">public int noOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-274">public int noOfDecimalsValue(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-275">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="6bf00-275">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-276">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="6bf00-276">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="6bf00-277">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-277">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="6bf00-278">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="6bf00-278">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-279">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-279">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-280">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-280">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-281">public Real realValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-281">public Real realValue(\[Real value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-282">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-282">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-283">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-283">public int rotateSign(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-284">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-284">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-285">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-285">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-286">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-286">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="6bf00-287">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-287">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="6bf00-288">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="6bf00-288">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="6bf00-289">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-289">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="6bf00-290">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-290">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-291">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-291">public int showZero(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-292">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-292">public int signDisplay(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-293">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-293">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="6bf00-294">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-294">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="6bf00-295">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-295">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-296">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-296">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-297">public int thousandSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-297">public int thousandSeparator(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-298">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="6bf00-298">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="6bf00-299">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-299">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="6bf00-300">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-300">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="6bf00-301">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-301">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="6bf00-302">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-302">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="6bf00-303">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-303">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="6bf00-304">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-304">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bf00-305">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-305">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="6bf00-306">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-306">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-307">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-307">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-308">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="6bf00-308">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-309">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-309">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bf00-310">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-310">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="6bf00-311">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-311">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="6bf00-312">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-312">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="6bf00-313">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-313">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="6bf00-314">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-314">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="6bf00-315">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-315">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="6bf00-316">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-316">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="6bf00-317">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-317">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-318">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-318">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="6bf00-319">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-319">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="6bf00-320">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-320">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bf00-321">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-321">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="6bf00-322">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-322">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="6bf00-323">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-323">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="6bf00-324">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-324">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="6bf00-325">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-325">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="6bf00-326">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-326">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="6bf00-327">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-327">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="6bf00-328">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-328">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="6bf00-329">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-329">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="6bf00-330">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-330">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="6bf00-331">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-331">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="6bf00-332">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-332">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="6bf00-333">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-333">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="6bf00-334">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="6bf00-334">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-335">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-335">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="6bf00-336">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-336">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="6bf00-337">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-337">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="6bf00-338">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-338">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="6bf00-339">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-339">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="6bf00-340">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-340">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="6bf00-341">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-341">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-342">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-342">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="6bf00-343">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-343">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="6bf00-344">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-344">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="6bf00-345">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-345">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="6bf00-346">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-346">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="6bf00-347">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-347">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="6bf00-348">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-348">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="6bf00-349">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-349">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="6bf00-350">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="6bf00-350">public void displayControl()</span></span>                                                                                | <span data-ttu-id="6bf00-351">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-351">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="6bf00-352">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-352">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-353">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-353">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-354">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-354">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-355">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="6bf00-355">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-356">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-356">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-357">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-357">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-358">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-358">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-359">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="6bf00-359">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="6bf00-360">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-360">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="6bf00-361">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="6bf00-361">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="6bf00-362">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-362">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="6bf00-363">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-363">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-364">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-364">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-365">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="6bf00-365">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="6bf00-366">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-366">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="6bf00-367">public void undo()</span><span class="sxs-lookup"><span data-stu-id="6bf00-367">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-368">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-368">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-369">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="6bf00-369">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="6bf00-370">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-370">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="6bf00-371">public void context()</span><span class="sxs-lookup"><span data-stu-id="6bf00-371">public void context()</span></span>                                                                                       | <span data-ttu-id="6bf00-372">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-372">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="6bf00-373">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="6bf00-373">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-374">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-374">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-375">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6bf00-375">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="6bf00-376">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-376">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="6bf00-377">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="6bf00-377">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="6bf00-378">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-378">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="6bf00-379">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="6bf00-379">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-380">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="6bf00-380">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-381">public void paste()</span><span class="sxs-lookup"><span data-stu-id="6bf00-381">public void paste()</span></span>                                                                                         | <span data-ttu-id="6bf00-382">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-382">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="6bf00-383">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-383">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-384">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-384">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-385">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="6bf00-385">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-386">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="6bf00-386">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="6bf00-387">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-387">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="6bf00-388">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="6bf00-388">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="6bf00-389">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-389">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="6bf00-390">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="6bf00-390">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-391">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="6bf00-391">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-392">public void copy()</span><span class="sxs-lookup"><span data-stu-id="6bf00-392">public void copy()</span></span>                                                                                          | <span data-ttu-id="6bf00-393">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-393">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="6bf00-394">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="6bf00-394">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-395">public void cut()</span><span class="sxs-lookup"><span data-stu-id="6bf00-395">public void cut()</span></span>                                                                                           | <span data-ttu-id="6bf00-396">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-396">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="6bf00-397">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="6bf00-397">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="6bf00-398">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-398">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="6bf00-399">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="6bf00-399">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="6bf00-400">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-400">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="6bf00-401">public void enter()</span><span class="sxs-lookup"><span data-stu-id="6bf00-401">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="6bf00-402">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="6bf00-402">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="6bf00-403">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-403">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="6bf00-404">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6bf00-404">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="6bf00-405">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-405">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="6bf00-406">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="6bf00-406">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="6bf00-407">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-407">Method alignControl</span></span>

<span data-ttu-id="6bf00-408">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-408">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="6bf00-409">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-409">Parameters - alignControl</span></span>

<span data-ttu-id="6bf00-410">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-410">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="6bf00-411">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-411">Return Value - alignControl</span></span>

<span data-ttu-id="6bf00-412">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-412">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="6bf00-413">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-413">Remarks - alignControl</span></span>

<span data-ttu-id="6bf00-414">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-414">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="6bf00-415">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="6bf00-415">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="6bf00-416">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="6bf00-416">Parameters - alignment</span></span>

<span data-ttu-id="6bf00-417">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-417">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="6bf00-418">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="6bf00-418">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="6bf00-419">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bf00-419">Method allowEdit</span></span>

<span data-ttu-id="6bf00-420">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-420">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="6bf00-421">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bf00-421">Parameters - allowEdit</span></span>

<span data-ttu-id="6bf00-422">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-422">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="6bf00-423">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bf00-423">Return Value - allowEdit</span></span>

<span data-ttu-id="6bf00-424">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-424">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="6bf00-425">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6bf00-425">Remarks - allowEdit</span></span>

<span data-ttu-id="6bf00-426">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-426">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allownegative"></a><span data-ttu-id="6bf00-427">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="6bf00-427">Method allowNegative</span></span>

```xpp
public int allowNegative([int value])
```

### <a name="parameters---allownegative"></a><span data-ttu-id="6bf00-428">パラメーター - allowNegative</span><span class="sxs-lookup"><span data-stu-id="6bf00-428">Parameters - allowNegative</span></span>

<span data-ttu-id="6bf00-429">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-429">value</span></span>  

### <a name="return-value---allownegative"></a><span data-ttu-id="6bf00-430">戻り値 - allowNegative</span><span class="sxs-lookup"><span data-stu-id="6bf00-430">Return Value - allowNegative</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="6bf00-431">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="6bf00-431">Method allowSysSetup</span></span>

<span data-ttu-id="6bf00-432">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-432">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="6bf00-433">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="6bf00-433">Return Value - allowSysSetup</span></span>

<span data-ttu-id="6bf00-434">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-434">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="6bf00-435">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-435">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="6bf00-436">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-436">Parameters - arrayIndex</span></span>

<span data-ttu-id="6bf00-437">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-437">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="6bf00-438">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-438">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="6bf00-439">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bf00-439">Method autoDeclaration</span></span>

<span data-ttu-id="6bf00-440">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-440">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="6bf00-441">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bf00-441">Parameters - autoDeclaration</span></span>

<span data-ttu-id="6bf00-442">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-442">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="6bf00-443">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bf00-443">Return Value - autoDeclaration</span></span>

<span data-ttu-id="6bf00-444">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-444">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="6bf00-445">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6bf00-445">Remarks - autoDeclaration</span></span>

<span data-ttu-id="6bf00-446">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-446">Controls cannot have identical names.</span></span>

## <a name="method-autoinsseparator"></a><span data-ttu-id="6bf00-447">メソッド autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-447">Method autoInsSeparator</span></span>

```xpp
public int autoInsSeparator([int value])
```

### <a name="parameters---autoinsseparator"></a><span data-ttu-id="6bf00-448">パラメーター - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-448">Parameters - autoInsSeparator</span></span>

<span data-ttu-id="6bf00-449">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-449">value</span></span>  

### <a name="return-value---autoinsseparator"></a><span data-ttu-id="6bf00-450">戻り値 - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-450">Return Value - autoInsSeparator</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="6bf00-451">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-451">Method backgroundColor</span></span>

<span data-ttu-id="6bf00-452">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-452">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="6bf00-453">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-453">Parameters - backgroundColor</span></span>

<span data-ttu-id="6bf00-454">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-454">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="6bf00-455">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-455">Return Value - backgroundColor</span></span>

<span data-ttu-id="6bf00-456">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="6bf00-456">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="6bf00-457">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-457">Remarks - backgroundColor</span></span>

<span data-ttu-id="6bf00-458">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-458">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="6bf00-459">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-459">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="6bf00-460">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-460">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="6bf00-461">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-461">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="6bf00-462">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-462">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="6bf00-463">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-463">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="6bf00-464">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="6bf00-464">Method backStyle</span></span>

<span data-ttu-id="6bf00-465">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-465">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="6bf00-466">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="6bf00-466">Parameters - backStyle</span></span>

<span data-ttu-id="6bf00-467">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-467">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="6bf00-468">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="6bf00-468">Return Value - backStyle</span></span>

<span data-ttu-id="6bf00-469">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-469">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="6bf00-470">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="6bf00-470">Method beginDrag</span></span>

<span data-ttu-id="6bf00-471">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-471">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="6bf00-472">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="6bf00-472">Parameters - beginDrag</span></span>

<span data-ttu-id="6bf00-473">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-473">x</span></span>  
<span data-ttu-id="6bf00-474">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-474">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="6bf00-475">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-475">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="6bf00-476">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-476">y</span></span>  
<span data-ttu-id="6bf00-477">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-477">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="6bf00-478">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-478">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="6bf00-479">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="6bf00-479">Return Value - beginDrag</span></span>

<span data-ttu-id="6bf00-480">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-480">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="6bf00-481">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="6bf00-481">Remarks - beginDrag</span></span>

<span data-ttu-id="6bf00-482">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-482">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="6bf00-483">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-483">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="6bf00-484">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="6bf00-484">Method bold</span></span>

<span data-ttu-id="6bf00-485">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-485">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="6bf00-486">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="6bf00-486">Parameters - bold</span></span>

<span data-ttu-id="6bf00-487">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-487">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="6bf00-488">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="6bf00-488">Return Value - bold</span></span>

<span data-ttu-id="6bf00-489">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-489">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="6bf00-490">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="6bf00-490">Remarks - bold</span></span>

<span data-ttu-id="6bf00-491">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-491">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="6bf00-492">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-492">0 Use the default font weight.</span></span>
-   <span data-ttu-id="6bf00-493">1 シン。</span><span class="sxs-lookup"><span data-stu-id="6bf00-493">1 Thin.</span></span>
-   <span data-ttu-id="6bf00-494">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="6bf00-494">2 Extra-light.</span></span>
-   <span data-ttu-id="6bf00-495">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="6bf00-495">3 Light.</span></span>
-   <span data-ttu-id="6bf00-496">4 標準。</span><span class="sxs-lookup"><span data-stu-id="6bf00-496">4 Normal.</span></span>
-   <span data-ttu-id="6bf00-497">5 中。</span><span class="sxs-lookup"><span data-stu-id="6bf00-497">5 Medium.</span></span>
-   <span data-ttu-id="6bf00-498">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="6bf00-498">6 Semibold.</span></span>
-   <span data-ttu-id="6bf00-499">7 太字。</span><span class="sxs-lookup"><span data-stu-id="6bf00-499">7 Bold.</span></span>
-   <span data-ttu-id="6bf00-500">8 極太。</span><span class="sxs-lookup"><span data-stu-id="6bf00-500">8 Extra-bold.</span></span>
-   <span data-ttu-id="6bf00-501">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="6bf00-501">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="6bf00-502">メソッド border</span><span class="sxs-lookup"><span data-stu-id="6bf00-502">Method border</span></span>

<span data-ttu-id="6bf00-503">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-503">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="6bf00-504">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="6bf00-504">Parameters - border</span></span>

<span data-ttu-id="6bf00-505">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-505">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="6bf00-506">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="6bf00-506">Return Value - border</span></span>

<span data-ttu-id="6bf00-507">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="6bf00-507">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="6bf00-508">備考 - border</span><span class="sxs-lookup"><span data-stu-id="6bf00-508">Remarks - border</span></span>

<span data-ttu-id="6bf00-509">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-509">The integer that is returned contains the style of the borderline of the control as follows.</span></span>

| <span data-ttu-id="6bf00-510">先頭値</span><span class="sxs-lookup"><span data-stu-id="6bf00-510">Value</span></span> | <span data-ttu-id="6bf00-511">説明</span><span class="sxs-lookup"><span data-stu-id="6bf00-511">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="6bf00-512">0</span><span class="sxs-lookup"><span data-stu-id="6bf00-512">0</span></span>     | <span data-ttu-id="6bf00-513">自動</span><span class="sxs-lookup"><span data-stu-id="6bf00-513">Auto</span></span>        |
| <span data-ttu-id="6bf00-514">1</span><span class="sxs-lookup"><span data-stu-id="6bf00-514">1</span></span>     | <span data-ttu-id="6bf00-515">3D</span><span class="sxs-lookup"><span data-stu-id="6bf00-515">3D</span></span>          |
| <span data-ttu-id="6bf00-516">2</span><span class="sxs-lookup"><span data-stu-id="6bf00-516">2</span></span>     | <span data-ttu-id="6bf00-517">1 行</span><span class="sxs-lookup"><span data-stu-id="6bf00-517">Single line</span></span> |
| <span data-ttu-id="6bf00-518">3</span><span class="sxs-lookup"><span data-stu-id="6bf00-518">3</span></span>     | <span data-ttu-id="6bf00-519">集合住宅</span><span class="sxs-lookup"><span data-stu-id="6bf00-519">Flat</span></span>        |
| <span data-ttu-id="6bf00-520">4</span><span class="sxs-lookup"><span data-stu-id="6bf00-520">4</span></span>     | <span data-ttu-id="6bf00-521">None</span><span class="sxs-lookup"><span data-stu-id="6bf00-521">None</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="6bf00-522">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-522">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="6bf00-523">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-523">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="6bf00-524">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-524">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="6bf00-525">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-525">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="6bf00-526">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-526">Method calcControlSize</span></span>

<span data-ttu-id="6bf00-527">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-527">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="6bf00-528">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-528">Parameters - calcControlSize</span></span>

<span data-ttu-id="6bf00-529">chars</span><span class="sxs-lookup"><span data-stu-id="6bf00-529">chars</span></span>  
<span data-ttu-id="6bf00-530">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="6bf00-530">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="6bf00-531">明細行</span><span class="sxs-lookup"><span data-stu-id="6bf00-531">lines</span></span>  
<span data-ttu-id="6bf00-532">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="6bf00-532">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="6bf00-533">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-533">Return Value - calcControlSize</span></span>

<span data-ttu-id="6bf00-534">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="6bf00-534">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="6bf00-535">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="6bf00-535">Method characterSet</span></span>

<span data-ttu-id="6bf00-536">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-536">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="6bf00-537">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="6bf00-537">Parameters - characterSet</span></span>

<span data-ttu-id="6bf00-538">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-538">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="6bf00-539">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6bf00-539">Return Value - characterSet</span></span>

<span data-ttu-id="6bf00-540">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-540">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="6bf00-541">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6bf00-541">Remarks - characterSet</span></span>

<span data-ttu-id="6bf00-542">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-542">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="6bf00-543">先頭値</span><span class="sxs-lookup"><span data-stu-id="6bf00-543">Value</span></span> | <span data-ttu-id="6bf00-544">説明</span><span class="sxs-lookup"><span data-stu-id="6bf00-544">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="6bf00-545">0</span><span class="sxs-lookup"><span data-stu-id="6bf00-545">0</span></span>     | <span data-ttu-id="6bf00-546">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-546">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="6bf00-547">1</span><span class="sxs-lookup"><span data-stu-id="6bf00-547">1</span></span>     | <span data-ttu-id="6bf00-548">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-548">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="6bf00-549">2</span><span class="sxs-lookup"><span data-stu-id="6bf00-549">2</span></span>     | <span data-ttu-id="6bf00-550">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-550">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="6bf00-551">77</span><span class="sxs-lookup"><span data-stu-id="6bf00-551">77</span></span>    | <span data-ttu-id="6bf00-552">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-552">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="6bf00-553">128</span><span class="sxs-lookup"><span data-stu-id="6bf00-553">128</span></span>   | <span data-ttu-id="6bf00-554">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-554">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="6bf00-555">129</span><span class="sxs-lookup"><span data-stu-id="6bf00-555">129</span></span>   | <span data-ttu-id="6bf00-556">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-556">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="6bf00-557">134</span><span class="sxs-lookup"><span data-stu-id="6bf00-557">134</span></span>   | <span data-ttu-id="6bf00-558">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-558">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="6bf00-559">136</span><span class="sxs-lookup"><span data-stu-id="6bf00-559">136</span></span>   | <span data-ttu-id="6bf00-560">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-560">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="6bf00-561">161</span><span class="sxs-lookup"><span data-stu-id="6bf00-561">161</span></span>   | <span data-ttu-id="6bf00-562">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-562">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="6bf00-563">162</span><span class="sxs-lookup"><span data-stu-id="6bf00-563">162</span></span>   | <span data-ttu-id="6bf00-564">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-564">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="6bf00-565">163</span><span class="sxs-lookup"><span data-stu-id="6bf00-565">163</span></span>   | <span data-ttu-id="6bf00-566">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-566">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="6bf00-567">186</span><span class="sxs-lookup"><span data-stu-id="6bf00-567">186</span></span>   | <span data-ttu-id="6bf00-568">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-568">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="6bf00-569">204</span><span class="sxs-lookup"><span data-stu-id="6bf00-569">204</span></span>   | <span data-ttu-id="6bf00-570">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-570">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="6bf00-571">238</span><span class="sxs-lookup"><span data-stu-id="6bf00-571">238</span></span>   | <span data-ttu-id="6bf00-572">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-572">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="6bf00-573">255</span><span class="sxs-lookup"><span data-stu-id="6bf00-573">255</span></span>   | <span data-ttu-id="6bf00-574">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-574">OEM\_CHARSET</span></span>         |

<span data-ttu-id="6bf00-575">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-575">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6bf00-576">金額</span><span class="sxs-lookup"><span data-stu-id="6bf00-576">Value</span></span> | <span data-ttu-id="6bf00-577">説明</span><span class="sxs-lookup"><span data-stu-id="6bf00-577">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="6bf00-578">130</span><span class="sxs-lookup"><span data-stu-id="6bf00-578">130</span></span>   | <span data-ttu-id="6bf00-579">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-579">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="6bf00-580">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-580">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="6bf00-581">先頭値</span><span class="sxs-lookup"><span data-stu-id="6bf00-581">Value</span></span> | <span data-ttu-id="6bf00-582">説明</span><span class="sxs-lookup"><span data-stu-id="6bf00-582">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="6bf00-583">177</span><span class="sxs-lookup"><span data-stu-id="6bf00-583">177</span></span>   | <span data-ttu-id="6bf00-584">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-584">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="6bf00-585">178</span><span class="sxs-lookup"><span data-stu-id="6bf00-585">178</span></span>   | <span data-ttu-id="6bf00-586">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-586">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="6bf00-587">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-587">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="6bf00-588">先頭値</span><span class="sxs-lookup"><span data-stu-id="6bf00-588">Value</span></span> | <span data-ttu-id="6bf00-589">説明</span><span class="sxs-lookup"><span data-stu-id="6bf00-589">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="6bf00-590">222</span><span class="sxs-lookup"><span data-stu-id="6bf00-590">222</span></span>   | <span data-ttu-id="6bf00-591">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6bf00-591">THAI\_CHARSET</span></span> |

<span data-ttu-id="6bf00-592">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-592">The default character set is set to values that are based on the current system locale.</span></span> <span data-ttu-id="6bf00-593">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-593">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="6bf00-594">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6bf00-594">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-charfrompos"></a><span data-ttu-id="6bf00-595">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="6bf00-595">Method charFromPos</span></span>

```xpp
public int charFromPos(int x, int y)
```

### <a name="parameters---charfrompos"></a><span data-ttu-id="6bf00-596">パラメーター - charFromPos</span><span class="sxs-lookup"><span data-stu-id="6bf00-596">Parameters - charFromPos</span></span>

<span data-ttu-id="6bf00-597">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-597">x</span></span>  

<!-- -->

<span data-ttu-id="6bf00-598">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-598">y</span></span>  

### <a name="return-value---charfrompos"></a><span data-ttu-id="6bf00-599">戻り値 - charFromPos</span><span class="sxs-lookup"><span data-stu-id="6bf00-599">Return Value - charFromPos</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="6bf00-600">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bf00-600">Method colorScheme</span></span>

<span data-ttu-id="6bf00-601">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-601">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="6bf00-602">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bf00-602">Parameters - colorScheme</span></span>

<span data-ttu-id="6bf00-603">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-603">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="6bf00-604">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bf00-604">Return Value - colorScheme</span></span>

<span data-ttu-id="6bf00-605">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="6bf00-605">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="6bf00-606">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6bf00-606">Remarks - colorScheme</span></span>

<span data-ttu-id="6bf00-607">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-607">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="6bf00-608">先頭値</span><span class="sxs-lookup"><span data-stu-id="6bf00-608">Value</span></span> | <span data-ttu-id="6bf00-609">スタイル</span><span class="sxs-lookup"><span data-stu-id="6bf00-609">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="6bf00-610">0</span><span class="sxs-lookup"><span data-stu-id="6bf00-610">0</span></span>     | <span data-ttu-id="6bf00-611">既定</span><span class="sxs-lookup"><span data-stu-id="6bf00-611">Default</span></span>               |
| <span data-ttu-id="6bf00-612">1</span><span class="sxs-lookup"><span data-stu-id="6bf00-612">1</span></span>     | <span data-ttu-id="6bf00-613">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="6bf00-613">The Windows palette</span></span>   |
| <span data-ttu-id="6bf00-614">2</span><span class="sxs-lookup"><span data-stu-id="6bf00-614">2</span></span>     | <span data-ttu-id="6bf00-615">真の配色</span><span class="sxs-lookup"><span data-stu-id="6bf00-615">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="6bf00-616">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bf00-616">Method configurationKey</span></span>

<span data-ttu-id="6bf00-617">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-617">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="6bf00-618">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bf00-618">Parameters - configurationKey</span></span>

<span data-ttu-id="6bf00-619">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-619">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="6bf00-620">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bf00-620">Return Value - configurationKey</span></span>

<span data-ttu-id="6bf00-621">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="6bf00-621">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="6bf00-622">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6bf00-622">Remarks - configurationKey</span></span>

<span data-ttu-id="6bf00-623">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-623">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="6bf00-624">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-624">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="6bf00-625">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-625">Method configurationKeyEx</span></span>

<span data-ttu-id="6bf00-626">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-626">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="6bf00-627">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-627">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="6bf00-628">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="6bf00-628">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="6bf00-629">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-629">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="6bf00-630">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-630">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="6bf00-631">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-631">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="6bf00-632">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-632">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="6bf00-633">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6bf00-633">Method countryRegionCodes</span></span>

<span data-ttu-id="6bf00-634">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-634">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="6bf00-635">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6bf00-635">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="6bf00-636">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-636">value</span></span>  
<span data-ttu-id="6bf00-637">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-637">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="6bf00-638">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6bf00-638">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="6bf00-639">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="6bf00-639">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="6bf00-640">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6bf00-640">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="6bf00-641">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6bf00-641">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="6bf00-642">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-642">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="6bf00-643">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6bf00-643">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="6bf00-644">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="6bf00-644">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="6bf00-645">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="6bf00-645">Parameters - dataField</span></span>

<span data-ttu-id="6bf00-646">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-646">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="6bf00-647">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="6bf00-647">Return Value - dataField</span></span>

## <a name="method-datafieldarrayindex"></a><span data-ttu-id="6bf00-648">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-648">Method dataFieldArrayIndex</span></span>

```xpp
public int dataFieldArrayIndex()
```

### <a name="return-value---datafieldarrayindex"></a><span data-ttu-id="6bf00-649">戻り値 - dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-649">Return Value - dataFieldArrayIndex</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="6bf00-650">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="6bf00-650">Method dataFieldName</span></span>

```xpp
public FieldName dataFieldName()
```

### <a name="return-value---datafieldname"></a><span data-ttu-id="6bf00-651">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="6bf00-651">Return Value - dataFieldName</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="6bf00-652">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-652">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="6bf00-653">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-653">Parameters - dataMethod</span></span>

<span data-ttu-id="6bf00-654">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-654">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="6bf00-655">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-655">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="6bf00-656">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6bf00-656">Method dataRelationPath</span></span>

<span data-ttu-id="6bf00-657">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-657">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="6bf00-658">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6bf00-658">Parameters - dataRelationPath</span></span>

<span data-ttu-id="6bf00-659">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-659">value</span></span>  
<span data-ttu-id="6bf00-660">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-660">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="6bf00-661">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6bf00-661">Return Value - dataRelationPath</span></span>

<span data-ttu-id="6bf00-662">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="6bf00-662">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="6bf00-663">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6bf00-663">Remarks - dataRelationPath</span></span>

<span data-ttu-id="6bf00-664">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-664">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="6bf00-665">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="6bf00-665">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="6bf00-666">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="6bf00-666">Method dataSource</span></span>

<span data-ttu-id="6bf00-667">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-667">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="6bf00-668">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="6bf00-668">Parameters - dataSource</span></span>

<span data-ttu-id="6bf00-669">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-669">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="6bf00-670">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="6bf00-670">Return Value - dataSource</span></span>

<span data-ttu-id="6bf00-671">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="6bf00-671">The identifier of the data source that will be used.</span></span>

## <a name="method-decimalseparator"></a><span data-ttu-id="6bf00-672">メソッド decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-672">Method decimalSeparator</span></span>

```xpp
public int decimalSeparator([int value])
```

### <a name="parameters---decimalseparator"></a><span data-ttu-id="6bf00-673">パラメーター - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-673">Parameters - decimalSeparator</span></span>

<span data-ttu-id="6bf00-674">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-674">value</span></span>  

### <a name="return-value---decimalseparator"></a><span data-ttu-id="6bf00-675">戻り値 - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-675">Return Value - decimalSeparator</span></span>

## <a name="method-direction"></a><span data-ttu-id="6bf00-676">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="6bf00-676">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="6bf00-677">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="6bf00-677">Parameters - direction</span></span>

<span data-ttu-id="6bf00-678">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-678">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="6bf00-679">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="6bf00-679">Return Value - direction</span></span>

## <a name="method-displacenegative"></a><span data-ttu-id="6bf00-680">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="6bf00-680">Method displaceNegative</span></span>

```xpp
public int displaceNegative([int value], [AutoMode mode])
```

### <a name="parameters---displacenegative"></a><span data-ttu-id="6bf00-681">パラメーター - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="6bf00-681">Parameters - displaceNegative</span></span>

<span data-ttu-id="6bf00-682">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-682">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-683">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-683">mode</span></span>  

### <a name="return-value---displacenegative"></a><span data-ttu-id="6bf00-684">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="6bf00-684">Return Value - displaceNegative</span></span>

## <a name="method-displacenegativemode"></a><span data-ttu-id="6bf00-685">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-685">Method displaceNegativeMode</span></span>

```xpp
public AutoMode displaceNegativeMode([AutoMode mode])
```

### <a name="parameters---displacenegativemode"></a><span data-ttu-id="6bf00-686">パラメーター - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-686">Parameters - displaceNegativeMode</span></span>

<span data-ttu-id="6bf00-687">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-687">mode</span></span>  

### <a name="return-value---displacenegativemode"></a><span data-ttu-id="6bf00-688">戻り値 - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-688">Return Value - displaceNegativeMode</span></span>

## <a name="method-displacenegativevalue"></a><span data-ttu-id="6bf00-689">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-689">Method displaceNegativeValue</span></span>

```xpp
public int displaceNegativeValue([int value])
```

### <a name="parameters---displacenegativevalue"></a><span data-ttu-id="6bf00-690">パラメーター - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-690">Parameters - displaceNegativeValue</span></span>

<span data-ttu-id="6bf00-691">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-691">value</span></span>  

### <a name="return-value---displacenegativevalue"></a><span data-ttu-id="6bf00-692">戻り値 - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-692">Return Value - displaceNegativeValue</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="6bf00-693">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-693">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="6bf00-694">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-694">Parameters - displayHeight</span></span>

<span data-ttu-id="6bf00-695">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-695">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-696">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-696">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="6bf00-697">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-697">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="6bf00-698">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-698">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="6bf00-699">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-699">Parameters - displayHeightMode</span></span>

<span data-ttu-id="6bf00-700">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-700">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="6bf00-701">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-701">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="6bf00-702">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-702">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="6bf00-703">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-703">Parameters - displayHeightValue</span></span>

<span data-ttu-id="6bf00-704">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-704">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="6bf00-705">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-705">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="6bf00-706">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="6bf00-706">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="6bf00-707">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="6bf00-707">Parameters - displayLength</span></span>

<span data-ttu-id="6bf00-708">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-708">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-709">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-709">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="6bf00-710">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="6bf00-710">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="6bf00-711">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-711">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="6bf00-712">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-712">Parameters - displayLengthMode</span></span>

<span data-ttu-id="6bf00-713">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-713">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="6bf00-714">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-714">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="6bf00-715">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-715">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="6bf00-716">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-716">Parameters - displayLengthValue</span></span>

<span data-ttu-id="6bf00-717">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-717">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="6bf00-718">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-718">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="6bf00-719">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="6bf00-719">Method displayTarget</span></span>

<span data-ttu-id="6bf00-720">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-720">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="6bf00-721">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6bf00-721">Parameters - displayTarget</span></span>

<span data-ttu-id="6bf00-722">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-722">value</span></span>  
<span data-ttu-id="6bf00-723">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-723">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="6bf00-724">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6bf00-724">Return Value - displayTarget</span></span>

<span data-ttu-id="6bf00-725">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-725">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="6bf00-726">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="6bf00-726">Method dragDrop</span></span>

<span data-ttu-id="6bf00-727">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-727">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="6bf00-728">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6bf00-728">Parameters - dragDrop</span></span>

<span data-ttu-id="6bf00-729">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-729">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="6bf00-730">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6bf00-730">Return Value - dragDrop</span></span>

<span data-ttu-id="6bf00-731">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-731">1 if drag-and-drop operations are enabled; otherwise, 0.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="6bf00-732">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="6bf00-732">Method dragOver</span></span>

<span data-ttu-id="6bf00-733">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-733">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="6bf00-734">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="6bf00-734">Parameters - dragOver</span></span>

<span data-ttu-id="6bf00-735">dragSource</span><span class="sxs-lookup"><span data-stu-id="6bf00-735">dragSource</span></span>  
<span data-ttu-id="6bf00-736">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-736">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-737">dragMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-737">dragMode</span></span>  
<span data-ttu-id="6bf00-738">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-738">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-739">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-739">x</span></span>  
<span data-ttu-id="6bf00-740">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-740">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-741">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-741">y</span></span>  
<span data-ttu-id="6bf00-742">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-742">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="6bf00-743">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="6bf00-743">Return Value - dragOver</span></span>

<span data-ttu-id="6bf00-744">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-744">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="6bf00-745">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-745">Method dragOverEx</span></span>

<span data-ttu-id="6bf00-746">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-746">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="6bf00-747">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-747">Parameters - dragOverEx</span></span>

<span data-ttu-id="6bf00-748">dragSource</span><span class="sxs-lookup"><span data-stu-id="6bf00-748">dragSource</span></span>  
<span data-ttu-id="6bf00-749">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-749">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-750">dragMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-750">dragMode</span></span>  
<span data-ttu-id="6bf00-751">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-751">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-752">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-752">x</span></span>  
<span data-ttu-id="6bf00-753">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-753">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-754">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-754">y</span></span>  
<span data-ttu-id="6bf00-755">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-755">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="6bf00-756">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-756">Return Value - dragOverEx</span></span>

<span data-ttu-id="6bf00-757">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-757">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="6bf00-758">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="6bf00-758">Method dragText</span></span>

<span data-ttu-id="6bf00-759">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-759">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="6bf00-760">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="6bf00-760">Return Value - dragText</span></span>

<span data-ttu-id="6bf00-761">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="6bf00-761">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="6bf00-762">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-762">Method enabled</span></span>

<span data-ttu-id="6bf00-763">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-763">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="6bf00-764">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-764">Parameters - enabled</span></span>

<span data-ttu-id="6bf00-765">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-765">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="6bf00-766">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-766">Return Value - enabled</span></span>

<span data-ttu-id="6bf00-767">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-767">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="6bf00-768">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-768">Remarks - enabled</span></span>

<span data-ttu-id="6bf00-769">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-769">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="6bf00-770">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-770">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="6bf00-771">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-771">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="6bf00-772">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6bf00-772">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="6bf00-773">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6bf00-773">Parameters - extendedDataType</span></span>

<span data-ttu-id="6bf00-774">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-774">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="6bf00-775">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6bf00-775">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="6bf00-776">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bf00-776">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="6bf00-777">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bf00-777">Parameters - fastTabSummary</span></span>

<span data-ttu-id="6bf00-778">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-778">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="6bf00-779">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bf00-779">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="6bf00-780">メソッド font</span><span class="sxs-lookup"><span data-stu-id="6bf00-780">Method font</span></span>

<span data-ttu-id="6bf00-781">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-781">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="6bf00-782">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="6bf00-782">Parameters - font</span></span>

<span data-ttu-id="6bf00-783">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-783">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="6bf00-784">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="6bf00-784">Return Value - font</span></span>

<span data-ttu-id="6bf00-785">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="6bf00-785">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="6bf00-786">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-786">Method fontSize</span></span>

<span data-ttu-id="6bf00-787">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-787">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="6bf00-788">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-788">Parameters - fontSize</span></span>

<span data-ttu-id="6bf00-789">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-789">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="6bf00-790">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-790">Return Value - fontSize</span></span>

<span data-ttu-id="6bf00-791">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="6bf00-791">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="6bf00-792">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-792">Method foregroundColor</span></span>

<span data-ttu-id="6bf00-793">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-793">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="6bf00-794">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-794">Parameters - foregroundColor</span></span>

<span data-ttu-id="6bf00-795">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-795">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="6bf00-796">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-796">Return Value - foregroundColor</span></span>

<span data-ttu-id="6bf00-797">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="6bf00-797">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="6bf00-798">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-798">Remarks - foregroundColor</span></span>

<span data-ttu-id="6bf00-799">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-799">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="6bf00-800">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-800">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="6bf00-801">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-801">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="6bf00-802">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6bf00-802">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="6bf00-803">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-803">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="6bf00-804">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-804">The maximum value for a single byte is 255.</span></span>

## <a name="method-formatmst"></a><span data-ttu-id="6bf00-805">メソッド formatMST</span><span class="sxs-lookup"><span data-stu-id="6bf00-805">Method formatMST</span></span>

```xpp
public int formatMST([int value])
```

### <a name="parameters---formatmst"></a><span data-ttu-id="6bf00-806">パラメーター - formatMST</span><span class="sxs-lookup"><span data-stu-id="6bf00-806">Parameters - formatMST</span></span>

<span data-ttu-id="6bf00-807">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-807">value</span></span>  

### <a name="return-value---formatmst"></a><span data-ttu-id="6bf00-808">戻り値 - formatMST</span><span class="sxs-lookup"><span data-stu-id="6bf00-808">Return Value - formatMST</span></span>

## <a name="method-getcursorpos"></a><span data-ttu-id="6bf00-809">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="6bf00-809">Method getCursorPos</span></span>

```xpp
public container getCursorPos()
```

### <a name="return-value---getcursorpos"></a><span data-ttu-id="6bf00-810">戻り値 - getCursorPos</span><span class="sxs-lookup"><span data-stu-id="6bf00-810">Return Value - getCursorPos</span></span>

## <a name="method-getfirstvisibleline"></a><span data-ttu-id="6bf00-811">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="6bf00-811">Method getFirstVisibleLine</span></span>

```xpp
public int getFirstVisibleLine()
```

### <a name="return-value---getfirstvisibleline"></a><span data-ttu-id="6bf00-812">戻り値 - getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="6bf00-812">Return Value - getFirstVisibleLine</span></span>

## <a name="method-getline"></a><span data-ttu-id="6bf00-813">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="6bf00-813">Method getLine</span></span>

```xpp
public str getLine(int lineNo)
```

### <a name="parameters---getline"></a><span data-ttu-id="6bf00-814">パラメーター - getLine</span><span class="sxs-lookup"><span data-stu-id="6bf00-814">Parameters - getLine</span></span>

<span data-ttu-id="6bf00-815">lineNo</span><span class="sxs-lookup"><span data-stu-id="6bf00-815">lineNo</span></span>  

### <a name="return-value---getline"></a><span data-ttu-id="6bf00-816">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="6bf00-816">Return Value - getLine</span></span>

## <a name="method-getlinecount"></a><span data-ttu-id="6bf00-817">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="6bf00-817">Method getLineCount</span></span>

```xpp
public int getLineCount()
```

### <a name="return-value---getlinecount"></a><span data-ttu-id="6bf00-818">戻り値 - getLineCount</span><span class="sxs-lookup"><span data-stu-id="6bf00-818">Return Value - getLineCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="6bf00-819">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="6bf00-819">Method getSelection</span></span>

```xpp
public container getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="6bf00-820">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="6bf00-820">Return Value - getSelection</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="6bf00-821">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="6bf00-821">Method hasChanged</span></span>

<span data-ttu-id="6bf00-822">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-822">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="6bf00-823">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="6bf00-823">Parameters - hasChanged</span></span>

<span data-ttu-id="6bf00-824">val</span><span class="sxs-lookup"><span data-stu-id="6bf00-824">val</span></span>  
<span data-ttu-id="6bf00-825">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-825">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="6bf00-826">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="6bf00-826">Return Value - hasChanged</span></span>

<span data-ttu-id="6bf00-827">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-827">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="6bf00-828">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="6bf00-828">Method hasUserSetting</span></span>

<span data-ttu-id="6bf00-829">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-829">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="6bf00-830">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="6bf00-830">Return Value - hasUserSetting</span></span>

<span data-ttu-id="6bf00-831">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-831">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="6bf00-832">メソッド height</span><span class="sxs-lookup"><span data-stu-id="6bf00-832">Method height</span></span>

<span data-ttu-id="6bf00-833">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-833">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="6bf00-834">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="6bf00-834">Parameters - height</span></span>

<span data-ttu-id="6bf00-835">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-835">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-836">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-836">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="6bf00-837">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="6bf00-837">Return Value - height</span></span>

<span data-ttu-id="6bf00-838">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="6bf00-838">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="6bf00-839">備考 - height</span><span class="sxs-lookup"><span data-stu-id="6bf00-839">Remarks - height</span></span>

<span data-ttu-id="6bf00-840">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-840">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6bf00-841">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6bf00-841">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6bf00-842">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-842">Mode</span></span>            | <span data-ttu-id="6bf00-843">高さの計算</span><span class="sxs-lookup"><span data-stu-id="6bf00-843">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf00-844">-1 正確</span><span class="sxs-lookup"><span data-stu-id="6bf00-844">-1 Exact</span></span>        | <span data-ttu-id="6bf00-845">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-845">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bf00-846">0 自動</span><span class="sxs-lookup"><span data-stu-id="6bf00-846">0 Auto</span></span>          | <span data-ttu-id="6bf00-847">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-847">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bf00-848">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="6bf00-848">1 Column height</span></span> | <span data-ttu-id="6bf00-849">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-849">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6bf00-850">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-850">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="6bf00-851">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-851">Method heightMode</span></span>

<span data-ttu-id="6bf00-852">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-852">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="6bf00-853">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-853">Parameters - heightMode</span></span>

<span data-ttu-id="6bf00-854">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-854">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="6bf00-855">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-855">Return Value - heightMode</span></span>

<span data-ttu-id="6bf00-856">計算モード。</span><span class="sxs-lookup"><span data-stu-id="6bf00-856">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="6bf00-857">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-857">Remarks - heightMode</span></span>

<span data-ttu-id="6bf00-858">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6bf00-858">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6bf00-859">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-859">Mode</span></span>          | <span data-ttu-id="6bf00-860">高さの計算</span><span class="sxs-lookup"><span data-stu-id="6bf00-860">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf00-861">正確</span><span class="sxs-lookup"><span data-stu-id="6bf00-861">Exact</span></span>         | <span data-ttu-id="6bf00-862">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-862">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bf00-863">自動</span><span class="sxs-lookup"><span data-stu-id="6bf00-863">Auto</span></span>          | <span data-ttu-id="6bf00-864">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-864">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bf00-865">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="6bf00-865">Column height</span></span> | <span data-ttu-id="6bf00-866">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-866">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6bf00-867">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-867">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="6bf00-868">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-868">Method heightValue</span></span>

<span data-ttu-id="6bf00-869">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-869">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="6bf00-870">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-870">Parameters - heightValue</span></span>

<span data-ttu-id="6bf00-871">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-871">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="6bf00-872">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-872">Return Value - heightValue</span></span>

<span data-ttu-id="6bf00-873">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="6bf00-873">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="6bf00-874">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-874">Remarks - heightValue</span></span>

<span data-ttu-id="6bf00-875">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-875">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="6bf00-876">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="6bf00-876">Method helpField</span></span>

<span data-ttu-id="6bf00-877">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-877">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="6bf00-878">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="6bf00-878">Return Value - helpField</span></span>

<span data-ttu-id="6bf00-879">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="6bf00-879">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="6bf00-880">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="6bf00-880">Remarks - helpField</span></span>

<span data-ttu-id="6bf00-881">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-881">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="6bf00-882">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-882">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="6bf00-883">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="6bf00-883">Method helpText</span></span>

<span data-ttu-id="6bf00-884">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-884">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="6bf00-885">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="6bf00-885">Parameters - helpText</span></span>

<span data-ttu-id="6bf00-886">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-886">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="6bf00-887">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="6bf00-887">Return Value - helpText</span></span>

<span data-ttu-id="6bf00-888">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="6bf00-888">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="6bf00-889">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="6bf00-889">Remarks - helpText</span></span>

<span data-ttu-id="6bf00-890">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-890">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="6bf00-891">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-891">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="6bf00-892">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6bf00-892">Method hierarchyParent</span></span>

<span data-ttu-id="6bf00-893">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-893">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="6bf00-894">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6bf00-894">Parameters - hierarchyParent</span></span>

<span data-ttu-id="6bf00-895">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-895">value</span></span>  
<span data-ttu-id="6bf00-896">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-896">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="6bf00-897">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6bf00-897">Return Value - hierarchyParent</span></span>

<span data-ttu-id="6bf00-898">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-898">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="6bf00-899">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="6bf00-899">Method hWnd</span></span>

<span data-ttu-id="6bf00-900">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-900">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="6bf00-901">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="6bf00-901">Return Value - hWnd</span></span>

<span data-ttu-id="6bf00-902">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="6bf00-902">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="6bf00-903">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="6bf00-903">Remarks - hWnd</span></span>

<span data-ttu-id="6bf00-904">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-904">The handle can be used with the Windows API.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="6bf00-905">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-905">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="6bf00-906">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-906">Parameters - iMEMode</span></span>

<span data-ttu-id="6bf00-907">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-907">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="6bf00-908">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-908">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="6bf00-909">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="6bf00-909">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="6bf00-910">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="6bf00-910">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="6bf00-911">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="6bf00-911">Method isDisplayed</span></span>

<span data-ttu-id="6bf00-912">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-912">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="6bf00-913">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="6bf00-913">Return Value - isDisplayed</span></span>

<span data-ttu-id="6bf00-914">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-914">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="6bf00-915">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="6bf00-915">Remarks - isDisplayed</span></span>

<span data-ttu-id="6bf00-916">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-916">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="6bf00-917">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="6bf00-917">Method isRestricted</span></span>

<span data-ttu-id="6bf00-918">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-918">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="6bf00-919">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="6bf00-919">Return Value - isRestricted</span></span>

<span data-ttu-id="6bf00-920">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-920">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="6bf00-921">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-921">Method isUserSetupEnabled</span></span>

<span data-ttu-id="6bf00-922">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-922">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="6bf00-923">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-923">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="6bf00-924">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="6bf00-924">neededSetupRights</span></span>  
<span data-ttu-id="6bf00-925">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-925">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="6bf00-926">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-926">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="6bf00-927">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-927">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="6bf00-928">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="6bf00-928">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="6bf00-929">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-929">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf00-930">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="6bf00-930">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="6bf00-931">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-931">No changes can be made to the control.</span></span> <span data-ttu-id="6bf00-932">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-932">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="6bf00-933">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="6bf00-933">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="6bf00-934">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-934">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="6bf00-935">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-935">The user cannot move the control.</span></span>   |
| <span data-ttu-id="6bf00-936">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="6bf00-936">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="6bf00-937">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-937">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="6bf00-938">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-938">The user can also move the control.</span></span> |

<span data-ttu-id="6bf00-939">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-939">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="6bf00-940">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="6bf00-940">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="6bf00-941">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="6bf00-941">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="6bf00-942">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="6bf00-942">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="6bf00-943">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="6bf00-943">Parameters - italic</span></span>

<span data-ttu-id="6bf00-944">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-944">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="6bf00-945">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="6bf00-945">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="6bf00-946">メソッド label</span><span class="sxs-lookup"><span data-stu-id="6bf00-946">Method label</span></span>

<span data-ttu-id="6bf00-947">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-947">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="6bf00-948">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="6bf00-948">Parameters - label</span></span>

<span data-ttu-id="6bf00-949">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-949">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="6bf00-950">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="6bf00-950">Return Value - label</span></span>

<span data-ttu-id="6bf00-951">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-951">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="6bf00-952">備考 - label</span><span class="sxs-lookup"><span data-stu-id="6bf00-952">Remarks - label</span></span>

<span data-ttu-id="6bf00-953">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-953">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="6bf00-954">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-954">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="6bf00-955">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6bf00-955">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="6bf00-956">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6bf00-956">Parameters - labelAlignment</span></span>

<span data-ttu-id="6bf00-957">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-957">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="6bf00-958">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6bf00-958">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="6bf00-959">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="6bf00-959">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="6bf00-960">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="6bf00-960">Parameters - labelBold</span></span>

<span data-ttu-id="6bf00-961">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-961">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="6bf00-962">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="6bf00-962">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="6bf00-963">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6bf00-963">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="6bf00-964">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6bf00-964">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="6bf00-965">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-965">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="6bf00-966">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6bf00-966">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="6bf00-967">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="6bf00-967">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="6bf00-968">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="6bf00-968">Parameters - labelFont</span></span>

<span data-ttu-id="6bf00-969">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-969">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="6bf00-970">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="6bf00-970">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="6bf00-971">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-971">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="6bf00-972">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-972">Parameters - labelFontSize</span></span>

<span data-ttu-id="6bf00-973">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-973">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="6bf00-974">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-974">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="6bf00-975">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-975">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="6bf00-976">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-976">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="6bf00-977">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-977">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="6bf00-978">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6bf00-978">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="6bf00-979">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="6bf00-979">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="6bf00-980">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="6bf00-980">Parameters - labelGuide</span></span>

<span data-ttu-id="6bf00-981">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-981">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="6bf00-982">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="6bf00-982">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="6bf00-983">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-983">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="6bf00-984">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-984">Parameters - labelHeight</span></span>

<span data-ttu-id="6bf00-985">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-985">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-986">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-986">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="6bf00-987">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-987">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="6bf00-988">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-988">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="6bf00-989">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-989">Parameters - labelHeightMode</span></span>

<span data-ttu-id="6bf00-990">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-990">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="6bf00-991">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-991">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="6bf00-992">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-992">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="6bf00-993">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-993">Parameters - labelHeightValue</span></span>

<span data-ttu-id="6bf00-994">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-994">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="6bf00-995">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-995">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="6bf00-996">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="6bf00-996">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="6bf00-997">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6bf00-997">Parameters - labelItalic</span></span>

<span data-ttu-id="6bf00-998">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-998">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="6bf00-999">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6bf00-999">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="6bf00-1000">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6bf00-1000">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="6bf00-1001">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6bf00-1001">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="6bf00-1002">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1002">x</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1003">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1003">y</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1004">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1004">button</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1005">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1005">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1006">Shift</span><span class="sxs-lookup"><span data-stu-id="6bf00-1006">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="6bf00-1007">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6bf00-1007">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="6bf00-1008">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="6bf00-1008">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="6bf00-1009">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="6bf00-1009">Parameters - labelMouseDown</span></span>

<span data-ttu-id="6bf00-1010">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1010">x</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1011">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1011">y</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1012">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1012">button</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1013">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1013">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1014">Shift</span><span class="sxs-lookup"><span data-stu-id="6bf00-1014">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="6bf00-1015">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="6bf00-1015">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="6bf00-1016">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="6bf00-1016">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="6bf00-1017">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="6bf00-1017">Parameters - labelMouseUp</span></span>

<span data-ttu-id="6bf00-1018">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1018">x</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1019">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1019">y</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1020">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1020">button</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1021">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1021">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1022">Shift</span><span class="sxs-lookup"><span data-stu-id="6bf00-1022">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="6bf00-1023">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="6bf00-1023">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="6bf00-1024">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="6bf00-1024">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="6bf00-1025">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6bf00-1025">Parameters - labelPosition</span></span>

<span data-ttu-id="6bf00-1026">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1026">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="6bf00-1027">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6bf00-1027">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="6bf00-1028">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6bf00-1028">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="6bf00-1029">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6bf00-1029">Parameters - labelUnderline</span></span>

<span data-ttu-id="6bf00-1030">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1030">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="6bf00-1031">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6bf00-1031">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="6bf00-1032">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="6bf00-1032">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="6bf00-1033">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="6bf00-1033">Parameters - labelWidth</span></span>

<span data-ttu-id="6bf00-1034">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1034">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1035">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1035">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="6bf00-1036">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="6bf00-1036">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="6bf00-1037">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1037">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="6bf00-1038">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1038">Parameters - labelWidthMode</span></span>

<span data-ttu-id="6bf00-1039">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1039">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="6bf00-1040">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1040">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="6bf00-1041">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1041">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="6bf00-1042">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1042">Parameters - labelWidthValue</span></span>

<span data-ttu-id="6bf00-1043">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1043">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="6bf00-1044">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1044">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="6bf00-1045">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="6bf00-1045">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="6bf00-1046">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="6bf00-1046">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="6bf00-1047">メソッド left</span><span class="sxs-lookup"><span data-stu-id="6bf00-1047">Method left</span></span>

<span data-ttu-id="6bf00-1048">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1048">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="6bf00-1049">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="6bf00-1049">Parameters - left</span></span>

<span data-ttu-id="6bf00-1050">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1050">value</span></span>  
<span data-ttu-id="6bf00-1051">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1051">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1052">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1052">mode</span></span>  
<span data-ttu-id="6bf00-1053">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1053">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="6bf00-1054">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="6bf00-1054">Return Value - left</span></span>

<span data-ttu-id="6bf00-1055">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1055">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="6bf00-1056">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1056">Method leftMode</span></span>

<span data-ttu-id="6bf00-1057">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1057">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="6bf00-1058">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1058">Parameters - leftMode</span></span>

<span data-ttu-id="6bf00-1059">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1059">value</span></span>  
<span data-ttu-id="6bf00-1060">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1060">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="6bf00-1061">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1061">Return Value - leftMode</span></span>

<span data-ttu-id="6bf00-1062">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1062">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="6bf00-1063">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1063">Method leftValue</span></span>

<span data-ttu-id="6bf00-1064">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1064">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="6bf00-1065">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1065">Parameters - leftValue</span></span>

<span data-ttu-id="6bf00-1066">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1066">value</span></span>  
<span data-ttu-id="6bf00-1067">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1067">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="6bf00-1068">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1068">Return Value - leftValue</span></span>

<span data-ttu-id="6bf00-1069">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1069">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="6bf00-1070">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1070">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="6bf00-1071">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1071">Parameters - limitText</span></span>

<span data-ttu-id="6bf00-1072">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1072">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1073">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1073">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="6bf00-1074">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1074">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="6bf00-1075">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1075">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="6bf00-1076">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1076">Parameters - limitTextMode</span></span>

<span data-ttu-id="6bf00-1077">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1077">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="6bf00-1078">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1078">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="6bf00-1079">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1079">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="6bf00-1080">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1080">Parameters - limitTextValue</span></span>

<span data-ttu-id="6bf00-1081">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1081">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="6bf00-1082">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1082">Return Value - limitTextValue</span></span>

## <a name="method-linefromchar"></a><span data-ttu-id="6bf00-1083">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="6bf00-1083">Method lineFromChar</span></span>

```xpp
public int lineFromChar(int charIndex)
```

### <a name="parameters---linefromchar"></a><span data-ttu-id="6bf00-1084">パラメーター - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="6bf00-1084">Parameters - lineFromChar</span></span>

<span data-ttu-id="6bf00-1085">charIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-1085">charIndex</span></span>  

### <a name="return-value---linefromchar"></a><span data-ttu-id="6bf00-1086">戻り値 - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="6bf00-1086">Return Value - lineFromChar</span></span>

## <a name="method-lineindex"></a><span data-ttu-id="6bf00-1087">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-1087">Method lineIndex</span></span>

```xpp
public int lineIndex(int lineNo)
```

### <a name="parameters---lineindex"></a><span data-ttu-id="6bf00-1088">パラメーター - lineIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-1088">Parameters - lineIndex</span></span>

<span data-ttu-id="6bf00-1089">lineNo</span><span class="sxs-lookup"><span data-stu-id="6bf00-1089">lineNo</span></span>  

### <a name="return-value---lineindex"></a><span data-ttu-id="6bf00-1090">戻り値 - lineIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-1090">Return Value - lineIndex</span></span>

## <a name="method-linelength"></a><span data-ttu-id="6bf00-1091">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="6bf00-1091">Method lineLength</span></span>

```xpp
public int lineLength(int lineNo)
```

### <a name="parameters---linelength"></a><span data-ttu-id="6bf00-1092">パラメーター - lineLength</span><span class="sxs-lookup"><span data-stu-id="6bf00-1092">Parameters - lineLength</span></span>

<span data-ttu-id="6bf00-1093">lineNo</span><span class="sxs-lookup"><span data-stu-id="6bf00-1093">lineNo</span></span>  

### <a name="return-value---linelength"></a><span data-ttu-id="6bf00-1094">戻り値 - lineLength</span><span class="sxs-lookup"><span data-stu-id="6bf00-1094">Return Value - lineLength</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="6bf00-1095">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="6bf00-1095">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="6bf00-1096">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="6bf00-1096">Parameters - lookupButton</span></span>

<span data-ttu-id="6bf00-1097">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1097">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="6bf00-1098">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="6bf00-1098">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="6bf00-1099">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="6bf00-1099">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="6bf00-1100">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="6bf00-1100">Parameters - mandatory</span></span>

<span data-ttu-id="6bf00-1101">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1101">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="6bf00-1102">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="6bf00-1102">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="6bf00-1103">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="6bf00-1103">Method markAsUserAdd</span></span>

<span data-ttu-id="6bf00-1104">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1104">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="6bf00-1105">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="6bf00-1105">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="6bf00-1106">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1106">value</span></span>  
<span data-ttu-id="6bf00-1107">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1107">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="6bf00-1108">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="6bf00-1108">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="6bf00-1109">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1109">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-minnoofdecimals"></a><span data-ttu-id="6bf00-1110">メソッド minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="6bf00-1110">Method minNoOfDecimals</span></span>

```xpp
public int minNoOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---minnoofdecimals"></a><span data-ttu-id="6bf00-1111">パラメーター - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="6bf00-1111">Parameters - minNoOfDecimals</span></span>

<span data-ttu-id="6bf00-1112">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1112">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1113">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1113">mode</span></span>  

### <a name="return-value---minnoofdecimals"></a><span data-ttu-id="6bf00-1114">戻り値 - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="6bf00-1114">Return Value - minNoOfDecimals</span></span>

## <a name="method-minnoofdecimalsmode"></a><span data-ttu-id="6bf00-1115">メソッド minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1115">Method minNoOfDecimalsMode</span></span>

```xpp
public AutoMode minNoOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---minnoofdecimalsmode"></a><span data-ttu-id="6bf00-1116">パラメーター - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1116">Parameters - minNoOfDecimalsMode</span></span>

<span data-ttu-id="6bf00-1117">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1117">mode</span></span>  

### <a name="return-value---minnoofdecimalsmode"></a><span data-ttu-id="6bf00-1118">戻り値 - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1118">Return Value - minNoOfDecimalsMode</span></span>

## <a name="method-minnoofdecimalsvalue"></a><span data-ttu-id="6bf00-1119">メソッド minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1119">Method minNoOfDecimalsValue</span></span>

```xpp
public int minNoOfDecimalsValue([int value])
```

### <a name="parameters---minnoofdecimalsvalue"></a><span data-ttu-id="6bf00-1120">パラメーター - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1120">Parameters - minNoOfDecimalsValue</span></span>

<span data-ttu-id="6bf00-1121">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1121">value</span></span>  

### <a name="return-value---minnoofdecimalsvalue"></a><span data-ttu-id="6bf00-1122">戻り値 - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1122">Return Value - minNoOfDecimalsValue</span></span>

## <a name="method-modified"></a><span data-ttu-id="6bf00-1123">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="6bf00-1123">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="6bf00-1124">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="6bf00-1124">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="6bf00-1125">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6bf00-1125">Method mouseDblClick</span></span>

<span data-ttu-id="6bf00-1126">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1126">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="6bf00-1127">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6bf00-1127">Parameters - mouseDblClick</span></span>

<span data-ttu-id="6bf00-1128">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1128">x</span></span>  
<span data-ttu-id="6bf00-1129">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1129">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1130">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1130">y</span></span>  
<span data-ttu-id="6bf00-1131">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1131">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1132">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1132">button</span></span>  
<span data-ttu-id="6bf00-1133">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1133">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1134">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1134">Ctrl</span></span>  
<span data-ttu-id="6bf00-1135">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1135">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1136">シフト</span><span class="sxs-lookup"><span data-stu-id="6bf00-1136">Shift</span></span>  
<span data-ttu-id="6bf00-1137">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1137">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="6bf00-1138">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6bf00-1138">Return Value - mouseDblClick</span></span>

<span data-ttu-id="6bf00-1139">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1139">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="6bf00-1140">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="6bf00-1140">Remarks - mouseDblClick</span></span>

<span data-ttu-id="6bf00-1141">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1141">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="6bf00-1142">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="6bf00-1142">Method mouseDown</span></span>

<span data-ttu-id="6bf00-1143">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1143">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="6bf00-1144">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="6bf00-1144">Parameters - mouseDown</span></span>

<span data-ttu-id="6bf00-1145">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1145">x</span></span>  
<span data-ttu-id="6bf00-1146">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1146">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1147">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1147">y</span></span>  
<span data-ttu-id="6bf00-1148">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1148">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1149">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1149">button</span></span>  
<span data-ttu-id="6bf00-1150">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1150">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1151">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1151">Ctrl</span></span>  
<span data-ttu-id="6bf00-1152">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1152">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1153">シフト</span><span class="sxs-lookup"><span data-stu-id="6bf00-1153">Shift</span></span>  
<span data-ttu-id="6bf00-1154">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1154">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="6bf00-1155">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="6bf00-1155">Return Value - mouseDown</span></span>

<span data-ttu-id="6bf00-1156">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1156">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="6bf00-1157">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="6bf00-1157">Remarks - mouseDown</span></span>

<span data-ttu-id="6bf00-1158">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1158">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="6bf00-1159">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1159">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="6bf00-1160">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="6bf00-1160">Method mouseMove</span></span>

<span data-ttu-id="6bf00-1161">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1161">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="6bf00-1162">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="6bf00-1162">Parameters - mouseMove</span></span>

<span data-ttu-id="6bf00-1163">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1163">x</span></span>  
<span data-ttu-id="6bf00-1164">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1164">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1165">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1165">y</span></span>  
<span data-ttu-id="6bf00-1166">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1166">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1167">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1167">button</span></span>  
<span data-ttu-id="6bf00-1168">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1168">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1169">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1169">Ctrl</span></span>  
<span data-ttu-id="6bf00-1170">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1170">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1171">シフト</span><span class="sxs-lookup"><span data-stu-id="6bf00-1171">Shift</span></span>  
<span data-ttu-id="6bf00-1172">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1172">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="6bf00-1173">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="6bf00-1173">Return Value - mouseMove</span></span>

<span data-ttu-id="6bf00-1174">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1174">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="6bf00-1175">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="6bf00-1175">Remarks - mouseMove</span></span>

<span data-ttu-id="6bf00-1176">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1176">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="6bf00-1177">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="6bf00-1177">Method mouseUp</span></span>

<span data-ttu-id="6bf00-1178">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1178">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="6bf00-1179">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="6bf00-1179">Parameters - mouseUp</span></span>

<span data-ttu-id="6bf00-1180">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1180">x</span></span>  
<span data-ttu-id="6bf00-1181">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1181">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1182">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1182">y</span></span>  
<span data-ttu-id="6bf00-1183">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1183">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1184">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1184">button</span></span>  
<span data-ttu-id="6bf00-1185">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1185">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1186">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1186">Ctrl</span></span>  
<span data-ttu-id="6bf00-1187">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1187">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1188">シフト</span><span class="sxs-lookup"><span data-stu-id="6bf00-1188">Shift</span></span>  
<span data-ttu-id="6bf00-1189">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1189">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="6bf00-1190">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="6bf00-1190">Return Value - mouseUp</span></span>

<span data-ttu-id="6bf00-1191">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1191">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="6bf00-1192">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="6bf00-1192">Remarks - mouseUp</span></span>

<span data-ttu-id="6bf00-1193">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1193">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="6bf00-1194">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1194">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="6bf00-1195">メソッド名</span><span class="sxs-lookup"><span data-stu-id="6bf00-1195">Method name</span></span>

<span data-ttu-id="6bf00-1196">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1196">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="6bf00-1197">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="6bf00-1197">Parameters - name</span></span>

<span data-ttu-id="6bf00-1198">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1198">value</span></span>  
<span data-ttu-id="6bf00-1199">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1199">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="6bf00-1200">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="6bf00-1200">Return Value - name</span></span>

<span data-ttu-id="6bf00-1201">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1201">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="6bf00-1202">備考 - name</span><span class="sxs-lookup"><span data-stu-id="6bf00-1202">Remarks - name</span></span>

<span data-ttu-id="6bf00-1203">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1203">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="6bf00-1204">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1204">It must start with a letter.</span></span>
-   <span data-ttu-id="6bf00-1205">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1205">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="6bf00-1206">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1206">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="6bf00-1207">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1207">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="6bf00-1208">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1208">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="6bf00-1209">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="6bf00-1209">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="6bf00-1210">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6bf00-1210">Parameters - neededPermission</span></span>

<span data-ttu-id="6bf00-1211">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1211">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="6bf00-1212">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6bf00-1212">Return Value - neededPermission</span></span>

## <a name="method-noofdecimals"></a><span data-ttu-id="6bf00-1213">メソッド noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="6bf00-1213">Method noOfDecimals</span></span>

```xpp
public int noOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---noofdecimals"></a><span data-ttu-id="6bf00-1214">パラメーター - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="6bf00-1214">Parameters - noOfDecimals</span></span>

<span data-ttu-id="6bf00-1215">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1215">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1216">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1216">mode</span></span>  

### <a name="return-value---noofdecimals"></a><span data-ttu-id="6bf00-1217">戻り値 - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="6bf00-1217">Return Value - noOfDecimals</span></span>

## <a name="method-noofdecimalsmode"></a><span data-ttu-id="6bf00-1218">メソッド noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1218">Method noOfDecimalsMode</span></span>

```xpp
public AutoMode noOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---noofdecimalsmode"></a><span data-ttu-id="6bf00-1219">パラメーター - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1219">Parameters - noOfDecimalsMode</span></span>

<span data-ttu-id="6bf00-1220">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1220">mode</span></span>  

### <a name="return-value---noofdecimalsmode"></a><span data-ttu-id="6bf00-1221">戻り値 - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1221">Return Value - noOfDecimalsMode</span></span>

## <a name="method-noofdecimalsvalue"></a><span data-ttu-id="6bf00-1222">メソッド noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1222">Method noOfDecimalsValue</span></span>

```xpp
public int noOfDecimalsValue([int value])
```

### <a name="parameters---noofdecimalsvalue"></a><span data-ttu-id="6bf00-1223">パラメーター - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1223">Parameters - noOfDecimalsValue</span></span>

<span data-ttu-id="6bf00-1224">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1224">value</span></span>  

### <a name="return-value---noofdecimalsvalue"></a><span data-ttu-id="6bf00-1225">戻り値 - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1225">Return Value - noOfDecimalsValue</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="6bf00-1226">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6bf00-1226">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="6bf00-1227">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6bf00-1227">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="6bf00-1228">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1228">Method parentControl</span></span>

<span data-ttu-id="6bf00-1229">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1229">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="6bf00-1230">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1230">Return Value - parentControl</span></span>

<span data-ttu-id="6bf00-1231">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1231">The parent control for the control.</span></span>

## <a name="method-posfromchar"></a><span data-ttu-id="6bf00-1232">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="6bf00-1232">Method posFromChar</span></span>

```xpp
public container posFromChar(int charIndex)
```

### <a name="parameters---posfromchar"></a><span data-ttu-id="6bf00-1233">パラメーター - posFromChar</span><span class="sxs-lookup"><span data-stu-id="6bf00-1233">Parameters - posFromChar</span></span>

<span data-ttu-id="6bf00-1234">charIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-1234">charIndex</span></span>  

### <a name="return-value---posfromchar"></a><span data-ttu-id="6bf00-1235">戻り値 - posFromChar</span><span class="sxs-lookup"><span data-stu-id="6bf00-1235">Return Value - posFromChar</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="6bf00-1236">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="6bf00-1236">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="6bf00-1237">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="6bf00-1237">Parameters - previewPartRef</span></span>

<span data-ttu-id="6bf00-1238">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1238">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="6bf00-1239">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="6bf00-1239">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="6bf00-1240">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="6bf00-1240">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="6bf00-1241">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="6bf00-1241">Parameters - promptrect</span></span>

<span data-ttu-id="6bf00-1242">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1242">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="6bf00-1243">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="6bf00-1243">Return Value - promptrect</span></span>

## <a name="method-realvalue"></a><span data-ttu-id="6bf00-1244">メソッド realValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1244">Method realValue</span></span>

```xpp
public Real realValue([Real value])
```

### <a name="parameters---realvalue"></a><span data-ttu-id="6bf00-1245">パラメーター - realValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1245">Parameters - realValue</span></span>

<span data-ttu-id="6bf00-1246">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1246">value</span></span>  

### <a name="return-value---realvalue"></a><span data-ttu-id="6bf00-1247">戻り値 - realValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1247">Return Value - realValue</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="6bf00-1248">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1248">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="6bf00-1249">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1249">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="6bf00-1250">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1250">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="6bf00-1251">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1251">Return Value - replaceOnLookup</span></span>

## <a name="method-rotatesign"></a><span data-ttu-id="6bf00-1252">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="6bf00-1252">Method rotateSign</span></span>

```xpp
public int rotateSign([int value])
```

### <a name="parameters---rotatesign"></a><span data-ttu-id="6bf00-1253">パラメーター - rotateSign</span><span class="sxs-lookup"><span data-stu-id="6bf00-1253">Parameters - rotateSign</span></span>

<span data-ttu-id="6bf00-1254">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1254">value</span></span>  

### <a name="return-value---rotatesign"></a><span data-ttu-id="6bf00-1255">戻り値 - rotateSign</span><span class="sxs-lookup"><span data-stu-id="6bf00-1255">Return Value - rotateSign</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="6bf00-1256">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="6bf00-1256">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="6bf00-1257">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="6bf00-1257">Parameters - searchAfterInput</span></span>

<span data-ttu-id="6bf00-1258">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1258">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="6bf00-1259">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="6bf00-1259">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="6bf00-1260">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1260">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="6bf00-1261">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1261">Parameters - searchMode</span></span>

<span data-ttu-id="6bf00-1262">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1262">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="6bf00-1263">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1263">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="6bf00-1264">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="6bf00-1264">Method securityKey</span></span>

<span data-ttu-id="6bf00-1265">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1265">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="6bf00-1266">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="6bf00-1266">Parameters - securityKey</span></span>

<span data-ttu-id="6bf00-1267">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1267">value</span></span>  
<span data-ttu-id="6bf00-1268">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1268">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="6bf00-1269">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="6bf00-1269">Return Value - securityKey</span></span>

<span data-ttu-id="6bf00-1270">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1270">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="6bf00-1271">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="6bf00-1271">Method showContextMenu</span></span>

<span data-ttu-id="6bf00-1272">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1272">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="6bf00-1273">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="6bf00-1273">Parameters - showContextMenu</span></span>

<span data-ttu-id="6bf00-1274">menuHandle</span><span class="sxs-lookup"><span data-stu-id="6bf00-1274">menuHandle</span></span>  
<span data-ttu-id="6bf00-1275">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1275">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="6bf00-1276">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="6bf00-1276">Return Value - showContextMenu</span></span>

<span data-ttu-id="6bf00-1277">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1277">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="6bf00-1278">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="6bf00-1278">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="6bf00-1279">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="6bf00-1279">Parameters - showLabel</span></span>

<span data-ttu-id="6bf00-1280">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1280">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="6bf00-1281">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="6bf00-1281">Return Value - showLabel</span></span>

## <a name="method-showzero"></a><span data-ttu-id="6bf00-1282">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="6bf00-1282">Method showZero</span></span>

```xpp
public int showZero([int value])
```

### <a name="parameters---showzero"></a><span data-ttu-id="6bf00-1283">パラメーター - showZero</span><span class="sxs-lookup"><span data-stu-id="6bf00-1283">Parameters - showZero</span></span>

<span data-ttu-id="6bf00-1284">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1284">value</span></span>  

### <a name="return-value---showzero"></a><span data-ttu-id="6bf00-1285">戻り値 - showZero</span><span class="sxs-lookup"><span data-stu-id="6bf00-1285">Return Value - showZero</span></span>

## <a name="method-signdisplay"></a><span data-ttu-id="6bf00-1286">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="6bf00-1286">Method signDisplay</span></span>

```xpp
public int signDisplay([int value])
```

### <a name="parameters---signdisplay"></a><span data-ttu-id="6bf00-1287">パラメーター - signDisplay</span><span class="sxs-lookup"><span data-stu-id="6bf00-1287">Parameters - signDisplay</span></span>

<span data-ttu-id="6bf00-1288">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1288">value</span></span>  

### <a name="return-value---signdisplay"></a><span data-ttu-id="6bf00-1289">戻り値 - signDisplay</span><span class="sxs-lookup"><span data-stu-id="6bf00-1289">Return Value - signDisplay</span></span>

## <a name="method-skip"></a><span data-ttu-id="6bf00-1290">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1290">Method skip</span></span>

<span data-ttu-id="6bf00-1291">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1291">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="6bf00-1292">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1292">Parameters - skip</span></span>

<span data-ttu-id="6bf00-1293">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1293">value</span></span>  
<span data-ttu-id="6bf00-1294">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1294">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="6bf00-1295">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1295">Return Value - skip</span></span>

<span data-ttu-id="6bf00-1296">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1296">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="6bf00-1297">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1297">Remarks - skip</span></span>

<span data-ttu-id="6bf00-1298">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1298">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="6bf00-1299">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="6bf00-1299">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="6bf00-1300">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="6bf00-1300">Parameters - sort</span></span>

<span data-ttu-id="6bf00-1301">sortDirection</span><span class="sxs-lookup"><span data-stu-id="6bf00-1301">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="6bf00-1302">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="6bf00-1302">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="6bf00-1303">メソッド style</span><span class="sxs-lookup"><span data-stu-id="6bf00-1303">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="6bf00-1304">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="6bf00-1304">Parameters - style</span></span>

<span data-ttu-id="6bf00-1305">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1305">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="6bf00-1306">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="6bf00-1306">Return Value - style</span></span>

## <a name="method-thousandseparator"></a><span data-ttu-id="6bf00-1307">メソッド thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-1307">Method thousandSeparator</span></span>

```xpp
public int thousandSeparator([int value])
```

### <a name="parameters---thousandseparator"></a><span data-ttu-id="6bf00-1308">パラメーター - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-1308">Parameters - thousandSeparator</span></span>

<span data-ttu-id="6bf00-1309">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1309">value</span></span>  

### <a name="return-value---thousandseparator"></a><span data-ttu-id="6bf00-1310">戻り値 - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="6bf00-1310">Return Value - thousandSeparator</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="6bf00-1311">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1311">Method toolTip</span></span>

<span data-ttu-id="6bf00-1312">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1312">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="6bf00-1313">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1313">Return Value - toolTip</span></span>

<span data-ttu-id="6bf00-1314">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1314">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="6bf00-1315">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1315">Remarks - toolTip</span></span>

<span data-ttu-id="6bf00-1316">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1316">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="6bf00-1317">メソッド top</span><span class="sxs-lookup"><span data-stu-id="6bf00-1317">Method top</span></span>

<span data-ttu-id="6bf00-1318">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1318">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="6bf00-1319">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="6bf00-1319">Parameters - top</span></span>

<span data-ttu-id="6bf00-1320">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1320">value</span></span>  
<span data-ttu-id="6bf00-1321">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1321">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1322">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1322">mode</span></span>  
<span data-ttu-id="6bf00-1323">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1323">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="6bf00-1324">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="6bf00-1324">Return Value - top</span></span>

<span data-ttu-id="6bf00-1325">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1325">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="6bf00-1326">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1326">Method topMode</span></span>

<span data-ttu-id="6bf00-1327">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1327">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="6bf00-1328">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1328">Parameters - topMode</span></span>

<span data-ttu-id="6bf00-1329">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1329">value</span></span>  
<span data-ttu-id="6bf00-1330">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1330">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="6bf00-1331">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1331">Return Value - topMode</span></span>

<span data-ttu-id="6bf00-1332">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1332">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="6bf00-1333">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1333">Method topValue</span></span>

<span data-ttu-id="6bf00-1334">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1334">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="6bf00-1335">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1335">Parameters - topValue</span></span>

<span data-ttu-id="6bf00-1336">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1336">value</span></span>  
<span data-ttu-id="6bf00-1337">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1337">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="6bf00-1338">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1338">Return Value - topValue</span></span>

<span data-ttu-id="6bf00-1339">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1339">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="6bf00-1340">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="6bf00-1340">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="6bf00-1341">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="6bf00-1341">Parameters - type</span></span>

<span data-ttu-id="6bf00-1342">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1342">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="6bf00-1343">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="6bf00-1343">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="6bf00-1344">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="6bf00-1344">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="6bf00-1345">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="6bf00-1345">Parameters - underline</span></span>

<span data-ttu-id="6bf00-1346">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1346">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="6bf00-1347">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="6bf00-1347">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="6bf00-1348">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6bf00-1348">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="6bf00-1349">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6bf00-1349">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="6bf00-1350">データ</span><span class="sxs-lookup"><span data-stu-id="6bf00-1350">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="6bf00-1351">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="6bf00-1351">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="6bf00-1352">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="6bf00-1352">Method userData</span></span>

<span data-ttu-id="6bf00-1353">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1353">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="6bf00-1354">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="6bf00-1354">Parameters - userData</span></span>

<span data-ttu-id="6bf00-1355">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1355">value</span></span>  
<span data-ttu-id="6bf00-1356">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1356">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="6bf00-1357">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="6bf00-1357">Return Value - userData</span></span>

<span data-ttu-id="6bf00-1358">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1358">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="6bf00-1359">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="6bf00-1359">Method userDataItem</span></span>

<span data-ttu-id="6bf00-1360">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1360">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="6bf00-1361">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6bf00-1361">Parameters - userDataItem</span></span>

<span data-ttu-id="6bf00-1362">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1362">value</span></span>  
<span data-ttu-id="6bf00-1363">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1363">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="6bf00-1364">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6bf00-1364">Return Value - userDataItem</span></span>

<span data-ttu-id="6bf00-1365">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1365">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="6bf00-1366">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="6bf00-1366">Method userDataItems</span></span>

<span data-ttu-id="6bf00-1367">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1367">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="6bf00-1368">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6bf00-1368">Parameters - userDataItems</span></span>

<span data-ttu-id="6bf00-1369">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1369">value</span></span>  
<span data-ttu-id="6bf00-1370">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1370">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="6bf00-1371">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6bf00-1371">Return Value - userDataItems</span></span>

<span data-ttu-id="6bf00-1372">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1372">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="6bf00-1373">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="6bf00-1373">Method userDisable</span></span>

<span data-ttu-id="6bf00-1374">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1374">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="6bf00-1375">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="6bf00-1375">Parameters - userDisable</span></span>

<span data-ttu-id="6bf00-1376">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1376">value</span></span>  
<span data-ttu-id="6bf00-1377">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1377">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="6bf00-1378">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="6bf00-1378">Return Value - userDisable</span></span>

<span data-ttu-id="6bf00-1379">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1379">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="6bf00-1380">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bf00-1380">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="6bf00-1381">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bf00-1381">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="6bf00-1382">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1382">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="6bf00-1383">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6bf00-1383">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="6bf00-1384">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-1384">Method userHeight</span></span>

<span data-ttu-id="6bf00-1385">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1385">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="6bf00-1386">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-1386">Parameters - userHeight</span></span>

<span data-ttu-id="6bf00-1387">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1387">value</span></span>  
<span data-ttu-id="6bf00-1388">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1388">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="6bf00-1389">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="6bf00-1389">Return Value - userHeight</span></span>

<span data-ttu-id="6bf00-1390">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1390">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="6bf00-1391">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="6bf00-1391">Method userHide</span></span>

<span data-ttu-id="6bf00-1392">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1392">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="6bf00-1393">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="6bf00-1393">Parameters - userHide</span></span>

<span data-ttu-id="6bf00-1394">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1394">value</span></span>  
<span data-ttu-id="6bf00-1395">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1395">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="6bf00-1396">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="6bf00-1396">Return Value - userHide</span></span>

<span data-ttu-id="6bf00-1397">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1397">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="6bf00-1398">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="6bf00-1398">Remarks - userHide</span></span>

<span data-ttu-id="6bf00-1399">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1399">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="6bf00-1400">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1400">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="6bf00-1401">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1401">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="6bf00-1402">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="6bf00-1402">Method userOrgContainer</span></span>

<span data-ttu-id="6bf00-1403">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1403">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="6bf00-1404">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="6bf00-1404">Parameters - userOrgContainer</span></span>

<span data-ttu-id="6bf00-1405">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1405">value</span></span>  
<span data-ttu-id="6bf00-1406">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1406">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="6bf00-1407">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="6bf00-1407">Return Value - userOrgContainer</span></span>

<span data-ttu-id="6bf00-1408">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1408">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="6bf00-1409">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="6bf00-1409">Method userOrgSibling</span></span>

<span data-ttu-id="6bf00-1410">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1410">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="6bf00-1411">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="6bf00-1411">Parameters - userOrgSibling</span></span>

<span data-ttu-id="6bf00-1412">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1412">value</span></span>  
<span data-ttu-id="6bf00-1413">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1413">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="6bf00-1414">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="6bf00-1414">Return Value - userOrgSibling</span></span>

<span data-ttu-id="6bf00-1415">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1415">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="6bf00-1416">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1416">Method userPromptText</span></span>

<span data-ttu-id="6bf00-1417">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1417">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="6bf00-1418">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1418">Parameters - userPromptText</span></span>

<span data-ttu-id="6bf00-1419">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1419">value</span></span>  
<span data-ttu-id="6bf00-1420">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1420">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="6bf00-1421">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1421">Return Value - userPromptText</span></span>

<span data-ttu-id="6bf00-1422">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1422">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="6bf00-1423">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="6bf00-1423">Method userSecurityLevel</span></span>

<span data-ttu-id="6bf00-1424">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1424">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="6bf00-1425">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="6bf00-1425">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="6bf00-1426">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1426">value</span></span>  
<span data-ttu-id="6bf00-1427">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1427">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="6bf00-1428">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="6bf00-1428">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="6bf00-1429">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1429">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="6bf00-1430">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1430">Method userSkip</span></span>

<span data-ttu-id="6bf00-1431">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1431">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="6bf00-1432">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1432">Parameters - userSkip</span></span>

<span data-ttu-id="6bf00-1433">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1433">value</span></span>  
<span data-ttu-id="6bf00-1434">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1434">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="6bf00-1435">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1435">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="6bf00-1436">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="6bf00-1436">Return Value - userSkip</span></span>

<span data-ttu-id="6bf00-1437">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1437">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="6bf00-1438">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="6bf00-1438">Method userWidth</span></span>

<span data-ttu-id="6bf00-1439">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1439">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="6bf00-1440">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="6bf00-1440">Parameters - userWidth</span></span>

<span data-ttu-id="6bf00-1441">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1441">value</span></span>  
<span data-ttu-id="6bf00-1442">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1442">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="6bf00-1443">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="6bf00-1443">Return Value - userWidth</span></span>

<span data-ttu-id="6bf00-1444">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1444">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="6bf00-1445">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="6bf00-1445">Remarks - userWidth</span></span>

<span data-ttu-id="6bf00-1446">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1446">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="6bf00-1447">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1447">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="6bf00-1448">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1448">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="6bf00-1449">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="6bf00-1449">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="6bf00-1450">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="6bf00-1450">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="6bf00-1451">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6bf00-1451">Method verticalSpacing</span></span>

<span data-ttu-id="6bf00-1452">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1452">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="6bf00-1453">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6bf00-1453">Parameters - verticalSpacing</span></span>

<span data-ttu-id="6bf00-1454">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1454">value</span></span>  
<span data-ttu-id="6bf00-1455">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1455">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1456">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1456">mode</span></span>  
<span data-ttu-id="6bf00-1457">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1457">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="6bf00-1458">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6bf00-1458">Return Value - verticalSpacing</span></span>

<span data-ttu-id="6bf00-1459">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1459">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="6bf00-1460">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1460">Method verticalSpacingMode</span></span>

<span data-ttu-id="6bf00-1461">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1461">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="6bf00-1462">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1462">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="6bf00-1463">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1463">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="6bf00-1464">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1464">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="6bf00-1465">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1465">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="6bf00-1466">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1466">Method verticalSpacingValue</span></span>

<span data-ttu-id="6bf00-1467">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1467">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="6bf00-1468">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1468">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="6bf00-1469">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1469">value</span></span>  
<span data-ttu-id="6bf00-1470">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1470">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="6bf00-1471">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1471">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="6bf00-1472">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1472">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="6bf00-1473">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1473">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="6bf00-1474">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1474">Parameters - viewEditMode</span></span>

<span data-ttu-id="6bf00-1475">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1475">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="6bf00-1476">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1476">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="6bf00-1477">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="6bf00-1477">Method visible</span></span>

<span data-ttu-id="6bf00-1478">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1478">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="6bf00-1479">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="6bf00-1479">Parameters - visible</span></span>

<span data-ttu-id="6bf00-1480">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1480">value</span></span>  
<span data-ttu-id="6bf00-1481">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1481">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="6bf00-1482">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="6bf00-1482">Return Value - visible</span></span>

<span data-ttu-id="6bf00-1483">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1483">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="6bf00-1484">メソッド width</span><span class="sxs-lookup"><span data-stu-id="6bf00-1484">Method width</span></span>

<span data-ttu-id="6bf00-1485">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1485">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="6bf00-1486">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="6bf00-1486">Parameters - width</span></span>

<span data-ttu-id="6bf00-1487">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1487">value</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1488">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1488">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="6bf00-1489">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="6bf00-1489">Return Value - width</span></span>

<span data-ttu-id="6bf00-1490">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1490">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="6bf00-1491">備考 - width</span><span class="sxs-lookup"><span data-stu-id="6bf00-1491">Remarks - width</span></span>

<span data-ttu-id="6bf00-1492">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1492">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6bf00-1493">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1493">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="6bf00-1494">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1494">Mode</span></span>           | <span data-ttu-id="6bf00-1495">幅計算</span><span class="sxs-lookup"><span data-stu-id="6bf00-1495">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf00-1496">-1 正確</span><span class="sxs-lookup"><span data-stu-id="6bf00-1496">-1 Exact</span></span>       | <span data-ttu-id="6bf00-1497">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1497">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bf00-1498">0 自動</span><span class="sxs-lookup"><span data-stu-id="6bf00-1498">0 Auto</span></span>         | <span data-ttu-id="6bf00-1499">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1499">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bf00-1500">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="6bf00-1500">1 Column width</span></span> | <span data-ttu-id="6bf00-1501">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1501">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6bf00-1502">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1502">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="6bf00-1503">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1503">Method widthMode</span></span>

<span data-ttu-id="6bf00-1504">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1504">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="6bf00-1505">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1505">Parameters - widthMode</span></span>

<span data-ttu-id="6bf00-1506">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1506">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="6bf00-1507">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1507">Return Value - widthMode</span></span>

<span data-ttu-id="6bf00-1508">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1508">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="6bf00-1509">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1509">Remarks - widthMode</span></span>

<span data-ttu-id="6bf00-1510">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1510">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="6bf00-1511">モード</span><span class="sxs-lookup"><span data-stu-id="6bf00-1511">Mode</span></span>         | <span data-ttu-id="6bf00-1512">幅計算</span><span class="sxs-lookup"><span data-stu-id="6bf00-1512">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf00-1513">正確</span><span class="sxs-lookup"><span data-stu-id="6bf00-1513">Exact</span></span>        | <span data-ttu-id="6bf00-1514">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1514">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6bf00-1515">自動</span><span class="sxs-lookup"><span data-stu-id="6bf00-1515">Auto</span></span>         | <span data-ttu-id="6bf00-1516">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1516">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6bf00-1517">列の幅</span><span class="sxs-lookup"><span data-stu-id="6bf00-1517">Column width</span></span> | <span data-ttu-id="6bf00-1518">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1518">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6bf00-1519">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1519">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="6bf00-1520">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1520">Method widthValue</span></span>

<span data-ttu-id="6bf00-1521">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1521">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="6bf00-1522">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1522">Parameters - widthValue</span></span>

<span data-ttu-id="6bf00-1523">値</span><span class="sxs-lookup"><span data-stu-id="6bf00-1523">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="6bf00-1524">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1524">Return Value - widthValue</span></span>

<span data-ttu-id="6bf00-1525">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1525">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="6bf00-1526">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6bf00-1526">Remarks - widthValue</span></span>

<span data-ttu-id="6bf00-1527">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1527">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="6bf00-1528">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1528">Method displayControl</span></span>

<span data-ttu-id="6bf00-1529">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1529">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-performtypelookup"></a><span data-ttu-id="6bf00-1530">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1530">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="6bf00-1531">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1531">Parameters - performTypeLookup</span></span>

<span data-ttu-id="6bf00-1532">userType</span><span class="sxs-lookup"><span data-stu-id="6bf00-1532">userType</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1533">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6bf00-1533">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1534">会社</span><span class="sxs-lookup"><span data-stu-id="6bf00-1534">company</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="6bf00-1535">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="6bf00-1535">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="6bf00-1536">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="6bf00-1536">Parameters - OnLeaving</span></span>

<span data-ttu-id="6bf00-1537">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1537">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1538">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1538">e</span></span>  

## <a name="method-pastetext"></a><span data-ttu-id="6bf00-1539">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1539">Method pasteText</span></span>

```xpp
public void pasteText(str pasteStr, [boolean InsertSel])
```

### <a name="parameters---pastetext"></a><span data-ttu-id="6bf00-1540">パラメーター - pasteText</span><span class="sxs-lookup"><span data-stu-id="6bf00-1540">Parameters - pasteText</span></span>

<span data-ttu-id="6bf00-1541">pasteStr</span><span class="sxs-lookup"><span data-stu-id="6bf00-1541">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1542">InsertSel</span><span class="sxs-lookup"><span data-stu-id="6bf00-1542">InsertSel</span></span>  

## <a name="method-lookup"></a><span data-ttu-id="6bf00-1543">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1543">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-onvalidated"></a><span data-ttu-id="6bf00-1544">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="6bf00-1544">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="6bf00-1545">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="6bf00-1545">Parameters - OnValidated</span></span>

<span data-ttu-id="6bf00-1546">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1546">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1547">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1547">e</span></span>  

## <a name="method-onlookup"></a><span data-ttu-id="6bf00-1548">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1548">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="6bf00-1549">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1549">Parameters - OnLookup</span></span>

<span data-ttu-id="6bf00-1550">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1550">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1551">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1551">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="6bf00-1552">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="6bf00-1552">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="6bf00-1553">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="6bf00-1553">Parameters - filter</span></span>

<span data-ttu-id="6bf00-1554">filterStr</span><span class="sxs-lookup"><span data-stu-id="6bf00-1554">filterStr</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="6bf00-1555">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="6bf00-1555">Method mouseLeave</span></span>

<span data-ttu-id="6bf00-1556">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1556">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-dragleave"></a><span data-ttu-id="6bf00-1557">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="6bf00-1557">Method dragLeave</span></span>

<span data-ttu-id="6bf00-1558">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1558">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="6bf00-1559">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-1559">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="6bf00-1560">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6bf00-1560">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="6bf00-1561">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="6bf00-1561">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1562">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="6bf00-1562">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1563">overrideObject</span><span class="sxs-lookup"><span data-stu-id="6bf00-1563">overrideObject</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="6bf00-1564">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="6bf00-1564">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="6bf00-1565">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="6bf00-1565">Parameters - OnModified</span></span>

<span data-ttu-id="6bf00-1566">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1566">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1567">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1567">e</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="6bf00-1568">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="6bf00-1568">Method setFocus</span></span>

<span data-ttu-id="6bf00-1569">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1569">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-undo"></a><span data-ttu-id="6bf00-1570">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="6bf00-1570">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-performdblookup"></a><span data-ttu-id="6bf00-1571">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1571">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="6bf00-1572">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1572">Parameters - performDBLookup</span></span>

<span data-ttu-id="6bf00-1573">fieldId</span><span class="sxs-lookup"><span data-stu-id="6bf00-1573">fieldId</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1574">tableId</span><span class="sxs-lookup"><span data-stu-id="6bf00-1574">tableId</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1575">会社</span><span class="sxs-lookup"><span data-stu-id="6bf00-1575">company</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="6bf00-1576">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="6bf00-1576">Method inputSearch</span></span>

<span data-ttu-id="6bf00-1577">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1577">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="6bf00-1578">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="6bf00-1578">Parameters - inputSearch</span></span>

<span data-ttu-id="6bf00-1579">searchStr</span><span class="sxs-lookup"><span data-stu-id="6bf00-1579">searchStr</span></span>  
<span data-ttu-id="6bf00-1580">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1580">The string value to use to filter data; optional.</span></span>

## <a name="method-context"></a><span data-ttu-id="6bf00-1581">メソッド context</span><span class="sxs-lookup"><span data-stu-id="6bf00-1581">Method context</span></span>

<span data-ttu-id="6bf00-1582">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1582">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-textchange"></a><span data-ttu-id="6bf00-1583">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="6bf00-1583">Method textChange</span></span>

```xpp
public void textChange()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="6bf00-1584">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="6bf00-1584">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="6bf00-1585">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="6bf00-1585">Parameters - OnGotFocus</span></span>

<span data-ttu-id="6bf00-1586">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1586">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1587">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1587">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="6bf00-1588">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="6bf00-1588">Method drop</span></span>

<span data-ttu-id="6bf00-1589">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1589">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="6bf00-1590">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="6bf00-1590">Parameters - drop</span></span>

<span data-ttu-id="6bf00-1591">dragSource</span><span class="sxs-lookup"><span data-stu-id="6bf00-1591">dragSource</span></span>  
<span data-ttu-id="6bf00-1592">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1592">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1593">dragMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1593">dragMode</span></span>  
<span data-ttu-id="6bf00-1594">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1594">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1595">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1595">x</span></span>  
<span data-ttu-id="6bf00-1596">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1596">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1597">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1597">y</span></span>  
<span data-ttu-id="6bf00-1598">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1598">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="6bf00-1599">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="6bf00-1599">Method gotFocus</span></span>

<span data-ttu-id="6bf00-1600">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1600">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-scrollcursor"></a><span data-ttu-id="6bf00-1601">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="6bf00-1601">Method scrollCursor</span></span>

```xpp
public void scrollCursor()
```

## <a name="method-linescroll"></a><span data-ttu-id="6bf00-1602">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="6bf00-1602">Method lineScroll</span></span>

```xpp
public void lineScroll(int dx, int dy)
```

### <a name="parameters---linescroll"></a><span data-ttu-id="6bf00-1603">パラメーター - lineScroll</span><span class="sxs-lookup"><span data-stu-id="6bf00-1603">Parameters - lineScroll</span></span>

<span data-ttu-id="6bf00-1604">dx</span><span class="sxs-lookup"><span data-stu-id="6bf00-1604">dx</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1605">dy</span><span class="sxs-lookup"><span data-stu-id="6bf00-1605">dy</span></span>  

## <a name="method-paste"></a><span data-ttu-id="6bf00-1606">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="6bf00-1606">Method paste</span></span>

<span data-ttu-id="6bf00-1607">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1607">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-onvalidating"></a><span data-ttu-id="6bf00-1608">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="6bf00-1608">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="6bf00-1609">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="6bf00-1609">Parameters - OnValidating</span></span>

<span data-ttu-id="6bf00-1610">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1610">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1611">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1611">e</span></span>  

## <a name="method-onenter"></a><span data-ttu-id="6bf00-1612">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="6bf00-1612">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="6bf00-1613">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="6bf00-1613">Parameters - OnEnter</span></span>

<span data-ttu-id="6bf00-1614">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1614">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1615">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1615">e</span></span>  

## <a name="method-performformlookup"></a><span data-ttu-id="6bf00-1616">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1616">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="6bf00-1617">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="6bf00-1617">Parameters - performFormLookup</span></span>

<span data-ttu-id="6bf00-1618">フォーム</span><span class="sxs-lookup"><span data-stu-id="6bf00-1618">form</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="6bf00-1619">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="6bf00-1619">Method lostFocus</span></span>

<span data-ttu-id="6bf00-1620">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1620">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-enddrag"></a><span data-ttu-id="6bf00-1621">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="6bf00-1621">Method endDrag</span></span>

<span data-ttu-id="6bf00-1622">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1622">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="6bf00-1623">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="6bf00-1623">Remarks - endDrag</span></span>

<span data-ttu-id="6bf00-1624">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1624">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="6bf00-1625">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1625">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="6bf00-1626">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="6bf00-1626">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="6bf00-1627">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="6bf00-1627">Parameters - OnLostFocus</span></span>

<span data-ttu-id="6bf00-1628">sender</span><span class="sxs-lookup"><span data-stu-id="6bf00-1628">sender</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1629">e</span><span class="sxs-lookup"><span data-stu-id="6bf00-1629">e</span></span>  

## <a name="method-setselection"></a><span data-ttu-id="6bf00-1630">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="6bf00-1630">Method setSelection</span></span>

```xpp
public void setSelection(int charIndexFrom, int charIndexTo)
```

### <a name="parameters---setselection"></a><span data-ttu-id="6bf00-1631">パラメーター - setSelection</span><span class="sxs-lookup"><span data-stu-id="6bf00-1631">Parameters - setSelection</span></span>

<span data-ttu-id="6bf00-1632">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="6bf00-1632">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1633">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="6bf00-1633">charIndexTo</span></span>  

## <a name="method-copy"></a><span data-ttu-id="6bf00-1634">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="6bf00-1634">Method copy</span></span>

<span data-ttu-id="6bf00-1635">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1635">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-jumpref"></a><span data-ttu-id="6bf00-1636">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="6bf00-1636">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-cut"></a><span data-ttu-id="6bf00-1637">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="6bf00-1637">Method cut</span></span>

<span data-ttu-id="6bf00-1638">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1638">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-mouseenter"></a><span data-ttu-id="6bf00-1639">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="6bf00-1639">Method mouseEnter</span></span>

<span data-ttu-id="6bf00-1640">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1640">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="6bf00-1641">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="6bf00-1641">Parameters - mouseEnter</span></span>

<span data-ttu-id="6bf00-1642">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1642">x</span></span>  
<span data-ttu-id="6bf00-1643">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1643">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1644">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1644">y</span></span>  
<span data-ttu-id="6bf00-1645">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1645">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1646">ボタン</span><span class="sxs-lookup"><span data-stu-id="6bf00-1646">button</span></span>  
<span data-ttu-id="6bf00-1647">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1647">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1648">Ctrl</span><span class="sxs-lookup"><span data-stu-id="6bf00-1648">Ctrl</span></span>  
<span data-ttu-id="6bf00-1649">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1649">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1650">シフト</span><span class="sxs-lookup"><span data-stu-id="6bf00-1650">Shift</span></span>  
<span data-ttu-id="6bf00-1651">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1651">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-prefcolumnsize"></a><span data-ttu-id="6bf00-1652">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-1652">Method prefColumnSize</span></span>

<span data-ttu-id="6bf00-1653">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1653">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="6bf00-1654">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="6bf00-1654">Parameters - prefColumnSize</span></span>

<span data-ttu-id="6bf00-1655">width</span><span class="sxs-lookup"><span data-stu-id="6bf00-1655">width</span></span>  
<span data-ttu-id="6bf00-1656">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1656">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1657">height</span><span class="sxs-lookup"><span data-stu-id="6bf00-1657">height</span></span>  
<span data-ttu-id="6bf00-1658">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1658">The preferred height of the control.</span></span>

## <a name="method-enter"></a><span data-ttu-id="6bf00-1659">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="6bf00-1659">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="6bf00-1660">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="6bf00-1660">Method resetUserSetting</span></span>

<span data-ttu-id="6bf00-1661">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1661">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-dropex"></a><span data-ttu-id="6bf00-1662">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-1662">Method dropEx</span></span>

<span data-ttu-id="6bf00-1663">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1663">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="6bf00-1664">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="6bf00-1664">Parameters - dropEx</span></span>

<span data-ttu-id="6bf00-1665">dragSource</span><span class="sxs-lookup"><span data-stu-id="6bf00-1665">dragSource</span></span>  
<span data-ttu-id="6bf00-1666">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1666">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1667">dragMode</span><span class="sxs-lookup"><span data-stu-id="6bf00-1667">dragMode</span></span>  
<span data-ttu-id="6bf00-1668">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1668">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1669">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1669">x</span></span>  
<span data-ttu-id="6bf00-1670">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1670">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="6bf00-1671">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1671">y</span></span>  
<span data-ttu-id="6bf00-1672">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6bf00-1672">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-setcursorpos"></a><span data-ttu-id="6bf00-1673">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="6bf00-1673">Method setCursorPos</span></span>

```xpp
public void setCursorPos(int x, int y)
```

### <a name="parameters---setcursorpos"></a><span data-ttu-id="6bf00-1674">パラメーター - setCursorPos</span><span class="sxs-lookup"><span data-stu-id="6bf00-1674">Parameters - setCursorPos</span></span>

<span data-ttu-id="6bf00-1675">x</span><span class="sxs-lookup"><span data-stu-id="6bf00-1675">x</span></span>  

<!-- -->

<span data-ttu-id="6bf00-1676">y</span><span class="sxs-lookup"><span data-stu-id="6bf00-1676">y</span></span>  



