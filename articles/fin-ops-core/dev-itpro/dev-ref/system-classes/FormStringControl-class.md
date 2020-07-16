---
title: FormStringControl クラス
description: このトピックでは、FormStringControl クラスについて説明します。
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
ms.openlocfilehash: c2ce5c92a8b2b1aaf77affe39223c43a97cad705
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502620"
---
# <a name="class-formstringcontrol"></a><span data-ttu-id="241d3-103">クラス FormStringControl</span><span class="sxs-lookup"><span data-stu-id="241d3-103">Class FormStringControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormStringControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="241d3-104">備考</span><span class="sxs-lookup"><span data-stu-id="241d3-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="241d3-105">例</span><span class="sxs-lookup"><span data-stu-id="241d3-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="241d3-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="241d3-106">Methods</span></span>

| <span data-ttu-id="241d3-107">方法</span><span class="sxs-lookup"><span data-stu-id="241d3-107">Method</span></span>                                                                                                      | <span data-ttu-id="241d3-108">説明</span><span class="sxs-lookup"><span data-stu-id="241d3-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d3-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="241d3-110">コントロールを配置するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-110">Indicates whether to align the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="241d3-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="241d3-113">ユーザーがコントロールの内容を変更できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-113">Indicates whether the user can change the contents of the control.</span></span>                                                                                                      |
| <span data-ttu-id="241d3-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="241d3-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="241d3-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="241d3-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="241d3-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-118">Indicates whether the system can declare a member variable that has the same name as the control.</span></span>                                                                       |
| <span data-ttu-id="241d3-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="241d3-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="241d3-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="241d3-122">コントロールの背景色を透明にできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-122">Indicates whether the control background can be transparent.</span></span>                                                                                                            |
| <span data-ttu-id="241d3-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="241d3-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="241d3-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="241d3-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="241d3-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-126">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                                             |
| <span data-ttu-id="241d3-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="241d3-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="241d3-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="241d3-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="241d3-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="241d3-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="241d3-132">public int changeCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-132">public int changeCase(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-133">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-133">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="241d3-134">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-134">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="241d3-135">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="241d3-135">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-136">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-136">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="241d3-137">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-137">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="241d3-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="241d3-139">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-139">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="241d3-140">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="241d3-140">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="241d3-141">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-141">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="241d3-142">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-142">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="241d3-143">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-143">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="241d3-144">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-144">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-145">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-145">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-146">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="241d3-146">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-147">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="241d3-147">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-148">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-148">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-149">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-149">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="241d3-150">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-150">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="241d3-151">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-151">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="241d3-152">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-152">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="241d3-153">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-153">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-154">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-154">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-155">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-155">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-156">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-156">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-157">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-157">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-158">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-158">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-159">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-159">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-160">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-160">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="241d3-161">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-161">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="241d3-162">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-162">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="241d3-163">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-163">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                        |
| <span data-ttu-id="241d3-164">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="241d3-164">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="241d3-165">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-165">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="241d3-166">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="241d3-166">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="241d3-167">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-167">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="241d3-168">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="241d3-168">public str dragText()</span></span>                                                                                       | <span data-ttu-id="241d3-169">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-169">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="241d3-170">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-170">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="241d3-171">オブジェクトを有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-171">Indicates whether to enable or disable the object.</span></span>                                                                                                                      |
| <span data-ttu-id="241d3-172">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-172">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-173">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-173">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-174">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-174">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="241d3-175">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-175">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="241d3-176">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-176">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="241d3-177">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-177">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="241d3-178">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-178">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="241d3-179">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-179">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="241d3-180">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="241d3-180">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="241d3-181">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="241d3-181">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-182">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="241d3-182">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="241d3-183">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="241d3-183">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="241d3-184">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="241d3-184">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="241d3-185">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="241d3-185">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="241d3-186">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-186">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="241d3-187">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="241d3-187">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="241d3-188">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-188">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="241d3-189">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-189">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="241d3-190">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-190">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="241d3-191">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-191">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="241d3-192">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-192">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="241d3-193">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-193">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="241d3-194">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-194">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="241d3-195">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="241d3-195">public str helpField()</span></span>                                                                                      | <span data-ttu-id="241d3-196">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-196">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="241d3-197">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-197">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="241d3-198">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-198">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="241d3-199">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-199">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="241d3-200">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-200">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="241d3-201">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="241d3-201">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="241d3-202">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-202">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="241d3-203">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-203">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="241d3-204">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="241d3-204">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-205">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="241d3-205">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="241d3-206">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-206">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="241d3-207">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="241d3-207">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="241d3-208">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-208">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="241d3-209">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="241d3-209">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="241d3-210">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-210">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="241d3-211">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="241d3-211">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-212">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-212">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-213">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-213">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="241d3-214">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-214">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="241d3-215">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-215">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-216">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-216">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-217">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-217">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-218">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-218">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-219">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-219">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="241d3-220">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-220">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="241d3-221">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-221">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-222">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-222">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="241d3-223">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-223">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="241d3-224">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-224">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-225">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-225">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="241d3-226">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-226">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-227">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-227">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-228">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-228">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="241d3-229">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-229">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="241d3-230">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-230">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-231">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-231">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="241d3-232">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-232">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-233">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-233">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="241d3-234">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="241d3-234">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-235">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-235">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="241d3-236">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-236">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="241d3-237">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-237">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="241d3-238">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-238">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="241d3-239">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-239">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="241d3-240">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-240">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="241d3-241">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-241">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-242">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-242">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-243">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-243">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-244">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="241d3-244">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-245">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="241d3-245">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-246">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="241d3-246">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="241d3-247">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-247">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-248">public boolean lookupOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-248">public boolean lookupOnly(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-249">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-249">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-250">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-250">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="241d3-251">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="241d3-251">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="241d3-252">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="241d3-252">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="241d3-253">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-253">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="241d3-254">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-254">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="241d3-255">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-255">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="241d3-256">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-256">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="241d3-257">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-257">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="241d3-258">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-258">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="241d3-259">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-259">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="241d3-260">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-260">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="241d3-261">public boolean multiLine(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-261">public boolean multiLine(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-262">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-262">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="241d3-263">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-263">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="241d3-264">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-264">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-265">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="241d3-265">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="241d3-266">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="241d3-266">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="241d3-267">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-267">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="241d3-268">public boolean passwordStyle(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-268">public boolean passwordStyle(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="241d3-269">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="241d3-269">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-270">public FieldId presenceDataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-270">public FieldId presenceDataField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-271">public int presenceDataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-271">public int presenceDataSource(\[AnyType value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-272">public int presenceIndicatorAllowed(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-272">public int presenceIndicatorAllowed(\[int value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="241d3-273">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-273">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-274">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-274">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-275">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-275">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="241d3-276">public str resolveAmbiguousReference()</span><span class="sxs-lookup"><span data-stu-id="241d3-276">public str resolveAmbiguousReference()</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-277">public FieldBinding disambiguationLookupTarget()</span><span class="sxs-lookup"><span data-stu-id="241d3-277">public FieldBinding disambiguationLookupTarget()</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="241d3-278">public str lookupDisambiguateReference(FieldBinding fieldBinding)</span><span class="sxs-lookup"><span data-stu-id="241d3-278">public str lookupDisambiguateReference(FieldBinding fieldBinding)</span></span>                                           |                                                                                                                                                                         |
| <span data-ttu-id="241d3-279">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-279">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-280">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-280">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-281">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-281">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="241d3-282">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-282">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="241d3-283">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="241d3-283">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="241d3-284">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-284">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="241d3-285">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-285">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-286">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-286">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="241d3-287">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-287">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="241d3-288">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="241d3-288">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-289">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-289">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="241d3-290">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-290">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="241d3-291">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="241d3-291">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="241d3-292">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-292">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="241d3-293">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-293">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="241d3-294">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-294">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="241d3-295">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-295">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="241d3-296">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-296">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="241d3-297">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-297">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="241d3-298">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-298">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="241d3-299">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-299">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="241d3-300">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-300">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-301">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="241d3-301">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-302">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-302">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="241d3-303">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-303">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="241d3-304">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-304">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="241d3-305">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-305">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="241d3-306">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-306">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="241d3-307">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-307">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="241d3-308">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-308">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="241d3-309">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-309">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="241d3-310">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-310">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-311">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-311">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="241d3-312">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-312">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="241d3-313">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-313">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="241d3-314">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-314">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="241d3-315">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-315">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="241d3-316">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-316">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="241d3-317">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-317">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="241d3-318">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-318">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="241d3-319">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-319">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="241d3-320">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-320">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="241d3-321">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-321">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="241d3-322">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-322">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="241d3-323">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-323">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="241d3-324">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-324">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="241d3-325">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-325">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="241d3-326">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-326">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="241d3-327">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="241d3-327">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="241d3-328">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-328">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="241d3-329">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-329">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="241d3-330">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-330">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="241d3-331">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-331">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="241d3-332">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-332">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="241d3-333">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-333">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="241d3-334">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-334">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-335">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-335">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="241d3-336">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-336">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="241d3-337">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="241d3-337">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="241d3-338">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-338">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="241d3-339">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-339">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="241d3-340">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-340">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="241d3-341">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="241d3-341">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="241d3-342">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-342">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="241d3-343">public void presenceRefresh()</span><span class="sxs-lookup"><span data-stu-id="241d3-343">public void presenceRefresh()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="241d3-344">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-344">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="241d3-345">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="241d3-345">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="241d3-346">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-346">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="241d3-347">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="241d3-347">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="241d3-348">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-348">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="241d3-349">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="241d3-349">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-350">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-350">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-351">public void undo()</span><span class="sxs-lookup"><span data-stu-id="241d3-351">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="241d3-352">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="241d3-352">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="241d3-353">public void context()</span><span class="sxs-lookup"><span data-stu-id="241d3-353">public void context()</span></span>                                                                                       | <span data-ttu-id="241d3-354">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-354">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="241d3-355">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-355">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-356">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="241d3-356">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-357">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="241d3-357">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-358">public void enter()</span><span class="sxs-lookup"><span data-stu-id="241d3-358">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="241d3-359">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="241d3-359">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="241d3-360">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="241d3-360">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="241d3-361">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="241d3-361">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="241d3-362">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="241d3-362">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="241d3-363">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-363">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="241d3-364">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="241d3-364">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="241d3-365">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-365">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="241d3-366">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="241d3-366">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="241d3-367">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-367">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="241d3-368">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="241d3-368">public void displayControl()</span></span>                                                                                | <span data-ttu-id="241d3-369">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-369">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="241d3-370">public void copy()</span><span class="sxs-lookup"><span data-stu-id="241d3-370">public void copy()</span></span>                                                                                          | <span data-ttu-id="241d3-371">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="241d3-371">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="241d3-372">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="241d3-372">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="241d3-373">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-373">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="241d3-374">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="241d3-374">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="241d3-375">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-375">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="241d3-376">public void cut()</span><span class="sxs-lookup"><span data-stu-id="241d3-376">public void cut()</span></span>                                                                                           | <span data-ttu-id="241d3-377">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="241d3-377">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="241d3-378">public void paste()</span><span class="sxs-lookup"><span data-stu-id="241d3-378">public void paste()</span></span>                                                                                         | <span data-ttu-id="241d3-379">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="241d3-379">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="241d3-380">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-380">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="241d3-381">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="241d3-381">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-382">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="241d3-382">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-383">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-383">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-384">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="241d3-384">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="241d3-385">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-385">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-386">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="241d3-386">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="241d3-387">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-387">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="241d3-388">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="241d3-388">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="241d3-389">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="241d3-389">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="241d3-390">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="241d3-390">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="241d3-391">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="241d3-391">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="241d3-392">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="241d3-392">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="241d3-393">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="241d3-393">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="241d3-394">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="241d3-394">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="241d3-395">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="241d3-395">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="241d3-396">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-396">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="241d3-397">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="241d3-397">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="241d3-398">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-398">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="241d3-399">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="241d3-399">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="241d3-400">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-400">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="241d3-401">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="241d3-401">Method alignControl</span></span>

<span data-ttu-id="241d3-402">コントロールを配置するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-402">Indicates whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="241d3-403">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="241d3-403">Parameters - alignControl</span></span>

<span data-ttu-id="241d3-404">値</span><span class="sxs-lookup"><span data-stu-id="241d3-404">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="241d3-405">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="241d3-405">Return Value - alignControl</span></span>

<span data-ttu-id="241d3-406">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="241d3-406">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="241d3-407">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="241d3-407">Remarks - alignControl</span></span>

<span data-ttu-id="241d3-408">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-408">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="241d3-409">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="241d3-409">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="241d3-410">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="241d3-410">Parameters - alignment</span></span>

<span data-ttu-id="241d3-411">値</span><span class="sxs-lookup"><span data-stu-id="241d3-411">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="241d3-412">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="241d3-412">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="241d3-413">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="241d3-413">Method allowEdit</span></span>

<span data-ttu-id="241d3-414">ユーザーがコントロールの内容を変更できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-414">Indicates whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="241d3-415">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="241d3-415">Parameters - allowEdit</span></span>

<span data-ttu-id="241d3-416">値</span><span class="sxs-lookup"><span data-stu-id="241d3-416">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="241d3-417">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="241d3-417">Return Value - allowEdit</span></span>

<span data-ttu-id="241d3-418">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-418">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="241d3-419">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="241d3-419">Remarks - allowEdit</span></span>

<span data-ttu-id="241d3-420">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="241d3-420">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="241d3-421">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="241d3-421">Method allowSysSetup</span></span>

<span data-ttu-id="241d3-422">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-422">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="241d3-423">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="241d3-423">Return Value - allowSysSetup</span></span>

<span data-ttu-id="241d3-424">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-424">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="241d3-425">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-425">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="241d3-426">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-426">Parameters - arrayIndex</span></span>

<span data-ttu-id="241d3-427">値</span><span class="sxs-lookup"><span data-stu-id="241d3-427">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="241d3-428">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-428">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="241d3-429">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d3-429">Method autoDeclaration</span></span>

<span data-ttu-id="241d3-430">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-430">Indicates whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="241d3-431">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d3-431">Parameters - autoDeclaration</span></span>

<span data-ttu-id="241d3-432">値</span><span class="sxs-lookup"><span data-stu-id="241d3-432">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="241d3-433">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d3-433">Return Value - autoDeclaration</span></span>

<span data-ttu-id="241d3-434">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-434">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="241d3-435">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="241d3-435">Remarks - autoDeclaration</span></span>

<span data-ttu-id="241d3-436">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="241d3-436">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="241d3-437">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-437">Method backgroundColor</span></span>

<span data-ttu-id="241d3-438">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-438">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="241d3-439">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-439">Parameters - backgroundColor</span></span>

<span data-ttu-id="241d3-440">値</span><span class="sxs-lookup"><span data-stu-id="241d3-440">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="241d3-441">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-441">Return Value - backgroundColor</span></span>

<span data-ttu-id="241d3-442">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="241d3-442">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="241d3-443">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-443">Remarks - backgroundColor</span></span>

<span data-ttu-id="241d3-444">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d3-444">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="241d3-445">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="241d3-445">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="241d3-446">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="241d3-446">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="241d3-447">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="241d3-447">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="241d3-448">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="241d3-448">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="241d3-449">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="241d3-449">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="241d3-450">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="241d3-450">Method backStyle</span></span>

<span data-ttu-id="241d3-451">コントロールの背景色を透明にできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-451">Indicates whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="241d3-452">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="241d3-452">Parameters - backStyle</span></span>

<span data-ttu-id="241d3-453">値</span><span class="sxs-lookup"><span data-stu-id="241d3-453">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="241d3-454">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="241d3-454">Return Value - backStyle</span></span>

<span data-ttu-id="241d3-455">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="241d3-455">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="241d3-456">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="241d3-456">Method beginDrag</span></span>

<span data-ttu-id="241d3-457">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-457">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="241d3-458">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="241d3-458">Parameters - beginDrag</span></span>

<span data-ttu-id="241d3-459">x</span><span class="sxs-lookup"><span data-stu-id="241d3-459">x</span></span>  
<span data-ttu-id="241d3-460">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-460">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="241d3-461">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="241d3-461">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="241d3-462">y</span><span class="sxs-lookup"><span data-stu-id="241d3-462">y</span></span>  
<span data-ttu-id="241d3-463">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-463">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="241d3-464">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="241d3-464">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="241d3-465">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="241d3-465">Return Value - beginDrag</span></span>

<span data-ttu-id="241d3-466">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="241d3-466">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="241d3-467">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="241d3-467">Remarks - beginDrag</span></span>

<span data-ttu-id="241d3-468">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="241d3-468">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="241d3-469">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="241d3-469">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="241d3-470">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="241d3-470">Method bold</span></span>

<span data-ttu-id="241d3-471">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-471">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="241d3-472">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="241d3-472">Parameters - bold</span></span>

<span data-ttu-id="241d3-473">値</span><span class="sxs-lookup"><span data-stu-id="241d3-473">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="241d3-474">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="241d3-474">Return Value - bold</span></span>

<span data-ttu-id="241d3-475">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-475">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="241d3-476">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="241d3-476">Remarks - bold</span></span>

<span data-ttu-id="241d3-477">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d3-477">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="241d3-478">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="241d3-478">0 Use the default font weight.</span></span>
-   <span data-ttu-id="241d3-479">1 シン。</span><span class="sxs-lookup"><span data-stu-id="241d3-479">1 Thin.</span></span>
-   <span data-ttu-id="241d3-480">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="241d3-480">2 Extra-light.</span></span>
-   <span data-ttu-id="241d3-481">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="241d3-481">3 Light.</span></span>
-   <span data-ttu-id="241d3-482">4 標準。</span><span class="sxs-lookup"><span data-stu-id="241d3-482">4 Normal.</span></span>
-   <span data-ttu-id="241d3-483">5 中。</span><span class="sxs-lookup"><span data-stu-id="241d3-483">5 Medium.</span></span>
-   <span data-ttu-id="241d3-484">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="241d3-484">6 Semibold.</span></span>
-   <span data-ttu-id="241d3-485">7 太字。</span><span class="sxs-lookup"><span data-stu-id="241d3-485">7 Bold.</span></span>
-   <span data-ttu-id="241d3-486">8 極太。</span><span class="sxs-lookup"><span data-stu-id="241d3-486">8 Extra-bold.</span></span>
-   <span data-ttu-id="241d3-487">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="241d3-487">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="241d3-488">メソッド border</span><span class="sxs-lookup"><span data-stu-id="241d3-488">Method border</span></span>

<span data-ttu-id="241d3-489">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-489">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="241d3-490">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="241d3-490">Parameters - border</span></span>

<span data-ttu-id="241d3-491">値</span><span class="sxs-lookup"><span data-stu-id="241d3-491">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="241d3-492">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="241d3-492">Return Value - border</span></span>

<span data-ttu-id="241d3-493">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="241d3-493">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="241d3-494">備考 - border</span><span class="sxs-lookup"><span data-stu-id="241d3-494">Remarks - border</span></span>

<span data-ttu-id="241d3-495">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d3-495">The integer that is returned contains the style of the borderline of the control as follows.</span></span>

| <span data-ttu-id="241d3-496">先頭値</span><span class="sxs-lookup"><span data-stu-id="241d3-496">Value</span></span> | <span data-ttu-id="241d3-497">説明</span><span class="sxs-lookup"><span data-stu-id="241d3-497">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="241d3-498">0</span><span class="sxs-lookup"><span data-stu-id="241d3-498">0</span></span>     | <span data-ttu-id="241d3-499">自動</span><span class="sxs-lookup"><span data-stu-id="241d3-499">Auto</span></span>        |
| <span data-ttu-id="241d3-500">1</span><span class="sxs-lookup"><span data-stu-id="241d3-500">1</span></span>     | <span data-ttu-id="241d3-501">3D</span><span class="sxs-lookup"><span data-stu-id="241d3-501">3D</span></span>          |
| <span data-ttu-id="241d3-502">2</span><span class="sxs-lookup"><span data-stu-id="241d3-502">2</span></span>     | <span data-ttu-id="241d3-503">1 行</span><span class="sxs-lookup"><span data-stu-id="241d3-503">Single line</span></span> |
| <span data-ttu-id="241d3-504">3</span><span class="sxs-lookup"><span data-stu-id="241d3-504">3</span></span>     | <span data-ttu-id="241d3-505">集合住宅</span><span class="sxs-lookup"><span data-stu-id="241d3-505">Flat</span></span>        |
| <span data-ttu-id="241d3-506">4</span><span class="sxs-lookup"><span data-stu-id="241d3-506">4</span></span>     | <span data-ttu-id="241d3-507">None</span><span class="sxs-lookup"><span data-stu-id="241d3-507">None</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="241d3-508">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-508">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="241d3-509">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-509">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="241d3-510">値</span><span class="sxs-lookup"><span data-stu-id="241d3-510">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="241d3-511">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-511">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="241d3-512">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="241d3-512">Method calcControlSize</span></span>

<span data-ttu-id="241d3-513">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-513">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="241d3-514">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="241d3-514">Parameters - calcControlSize</span></span>

<span data-ttu-id="241d3-515">chars</span><span class="sxs-lookup"><span data-stu-id="241d3-515">chars</span></span>  
<span data-ttu-id="241d3-516">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="241d3-516">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="241d3-517">明細行</span><span class="sxs-lookup"><span data-stu-id="241d3-517">lines</span></span>  
<span data-ttu-id="241d3-518">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="241d3-518">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="241d3-519">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="241d3-519">Return Value - calcControlSize</span></span>

<span data-ttu-id="241d3-520">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="241d3-520">The container that holds the width and height.</span></span>

## <a name="method-changecase"></a><span data-ttu-id="241d3-521">メソッド changeCase</span><span class="sxs-lookup"><span data-stu-id="241d3-521">Method changeCase</span></span>

```xpp
public int changeCase([int value])
```

### <a name="parameters---changecase"></a><span data-ttu-id="241d3-522">パラメーター - changeCase</span><span class="sxs-lookup"><span data-stu-id="241d3-522">Parameters - changeCase</span></span>

<span data-ttu-id="241d3-523">値</span><span class="sxs-lookup"><span data-stu-id="241d3-523">value</span></span>  

### <a name="return-value---changecase"></a><span data-ttu-id="241d3-524">戻り値 - changeCase</span><span class="sxs-lookup"><span data-stu-id="241d3-524">Return Value - changeCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="241d3-525">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="241d3-525">Method characterSet</span></span>

<span data-ttu-id="241d3-526">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-526">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="241d3-527">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="241d3-527">Parameters - characterSet</span></span>

<span data-ttu-id="241d3-528">値</span><span class="sxs-lookup"><span data-stu-id="241d3-528">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="241d3-529">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="241d3-529">Return Value - characterSet</span></span>

<span data-ttu-id="241d3-530">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-530">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="241d3-531">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="241d3-531">Remarks - characterSet</span></span>

<span data-ttu-id="241d3-532">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-532">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="241d3-533">先頭値</span><span class="sxs-lookup"><span data-stu-id="241d3-533">Value</span></span> | <span data-ttu-id="241d3-534">説明</span><span class="sxs-lookup"><span data-stu-id="241d3-534">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="241d3-535">0</span><span class="sxs-lookup"><span data-stu-id="241d3-535">0</span></span>     | <span data-ttu-id="241d3-536">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-536">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="241d3-537">1</span><span class="sxs-lookup"><span data-stu-id="241d3-537">1</span></span>     | <span data-ttu-id="241d3-538">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-538">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="241d3-539">2</span><span class="sxs-lookup"><span data-stu-id="241d3-539">2</span></span>     | <span data-ttu-id="241d3-540">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-540">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="241d3-541">77</span><span class="sxs-lookup"><span data-stu-id="241d3-541">77</span></span>    | <span data-ttu-id="241d3-542">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-542">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="241d3-543">128</span><span class="sxs-lookup"><span data-stu-id="241d3-543">128</span></span>   | <span data-ttu-id="241d3-544">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-544">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="241d3-545">129</span><span class="sxs-lookup"><span data-stu-id="241d3-545">129</span></span>   | <span data-ttu-id="241d3-546">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-546">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="241d3-547">134</span><span class="sxs-lookup"><span data-stu-id="241d3-547">134</span></span>   | <span data-ttu-id="241d3-548">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-548">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="241d3-549">136</span><span class="sxs-lookup"><span data-stu-id="241d3-549">136</span></span>   | <span data-ttu-id="241d3-550">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-550">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="241d3-551">161</span><span class="sxs-lookup"><span data-stu-id="241d3-551">161</span></span>   | <span data-ttu-id="241d3-552">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-552">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="241d3-553">162</span><span class="sxs-lookup"><span data-stu-id="241d3-553">162</span></span>   | <span data-ttu-id="241d3-554">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-554">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="241d3-555">163</span><span class="sxs-lookup"><span data-stu-id="241d3-555">163</span></span>   | <span data-ttu-id="241d3-556">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-556">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="241d3-557">186</span><span class="sxs-lookup"><span data-stu-id="241d3-557">186</span></span>   | <span data-ttu-id="241d3-558">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-558">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="241d3-559">204</span><span class="sxs-lookup"><span data-stu-id="241d3-559">204</span></span>   | <span data-ttu-id="241d3-560">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-560">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="241d3-561">238</span><span class="sxs-lookup"><span data-stu-id="241d3-561">238</span></span>   | <span data-ttu-id="241d3-562">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-562">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="241d3-563">255</span><span class="sxs-lookup"><span data-stu-id="241d3-563">255</span></span>   | <span data-ttu-id="241d3-564">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-564">OEM\_CHARSET</span></span>         |

<span data-ttu-id="241d3-565">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="241d3-565">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="241d3-566">金額</span><span class="sxs-lookup"><span data-stu-id="241d3-566">Value</span></span> | <span data-ttu-id="241d3-567">説明</span><span class="sxs-lookup"><span data-stu-id="241d3-567">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="241d3-568">130</span><span class="sxs-lookup"><span data-stu-id="241d3-568">130</span></span>   | <span data-ttu-id="241d3-569">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-569">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="241d3-570">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="241d3-570">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="241d3-571">先頭値</span><span class="sxs-lookup"><span data-stu-id="241d3-571">Value</span></span> | <span data-ttu-id="241d3-572">説明</span><span class="sxs-lookup"><span data-stu-id="241d3-572">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="241d3-573">177</span><span class="sxs-lookup"><span data-stu-id="241d3-573">177</span></span>   | <span data-ttu-id="241d3-574">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-574">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="241d3-575">178</span><span class="sxs-lookup"><span data-stu-id="241d3-575">178</span></span>   | <span data-ttu-id="241d3-576">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-576">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="241d3-577">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="241d3-577">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="241d3-578">先頭値</span><span class="sxs-lookup"><span data-stu-id="241d3-578">Value</span></span> | <span data-ttu-id="241d3-579">説明</span><span class="sxs-lookup"><span data-stu-id="241d3-579">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="241d3-580">222</span><span class="sxs-lookup"><span data-stu-id="241d3-580">222</span></span>   | <span data-ttu-id="241d3-581">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="241d3-581">THAI\_CHARSET</span></span> |

<span data-ttu-id="241d3-582">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-582">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="241d3-583">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-583">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="241d3-584">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="241d3-584">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-charfrompos"></a><span data-ttu-id="241d3-585">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="241d3-585">Method charFromPos</span></span>

```xpp
public int charFromPos(int x, int y)
```

### <a name="parameters---charfrompos"></a><span data-ttu-id="241d3-586">パラメーター - charFromPos</span><span class="sxs-lookup"><span data-stu-id="241d3-586">Parameters - charFromPos</span></span>

<span data-ttu-id="241d3-587">x</span><span class="sxs-lookup"><span data-stu-id="241d3-587">x</span></span>  

<!-- -->

<span data-ttu-id="241d3-588">y</span><span class="sxs-lookup"><span data-stu-id="241d3-588">y</span></span>  

### <a name="return-value---charfrompos"></a><span data-ttu-id="241d3-589">戻り値 - charFromPos</span><span class="sxs-lookup"><span data-stu-id="241d3-589">Return Value - charFromPos</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="241d3-590">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d3-590">Method colorScheme</span></span>

<span data-ttu-id="241d3-591">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-591">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="241d3-592">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d3-592">Parameters - colorScheme</span></span>

<span data-ttu-id="241d3-593">値</span><span class="sxs-lookup"><span data-stu-id="241d3-593">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="241d3-594">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d3-594">Return Value - colorScheme</span></span>

<span data-ttu-id="241d3-595">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="241d3-595">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="241d3-596">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="241d3-596">Remarks - colorScheme</span></span>

<span data-ttu-id="241d3-597">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-597">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="241d3-598">先頭値</span><span class="sxs-lookup"><span data-stu-id="241d3-598">Value</span></span> | <span data-ttu-id="241d3-599">スタイル</span><span class="sxs-lookup"><span data-stu-id="241d3-599">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="241d3-600">0</span><span class="sxs-lookup"><span data-stu-id="241d3-600">0</span></span>     | <span data-ttu-id="241d3-601">既定</span><span class="sxs-lookup"><span data-stu-id="241d3-601">Default</span></span>               |
| <span data-ttu-id="241d3-602">1</span><span class="sxs-lookup"><span data-stu-id="241d3-602">1</span></span>     | <span data-ttu-id="241d3-603">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="241d3-603">The Windows palette</span></span>   |
| <span data-ttu-id="241d3-604">2</span><span class="sxs-lookup"><span data-stu-id="241d3-604">2</span></span>     | <span data-ttu-id="241d3-605">真の配色</span><span class="sxs-lookup"><span data-stu-id="241d3-605">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="241d3-606">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="241d3-606">Method configurationKey</span></span>

<span data-ttu-id="241d3-607">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-607">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="241d3-608">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="241d3-608">Parameters - configurationKey</span></span>

<span data-ttu-id="241d3-609">値</span><span class="sxs-lookup"><span data-stu-id="241d3-609">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="241d3-610">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="241d3-610">Return Value - configurationKey</span></span>

<span data-ttu-id="241d3-611">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="241d3-611">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="241d3-612">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="241d3-612">Remarks - configurationKey</span></span>

<span data-ttu-id="241d3-613">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-613">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="241d3-614">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="241d3-614">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="241d3-615">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="241d3-615">Method configurationKeyEx</span></span>

<span data-ttu-id="241d3-616">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-616">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="241d3-617">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="241d3-617">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="241d3-618">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="241d3-618">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="241d3-619">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="241d3-619">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="241d3-620">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="241d3-620">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="241d3-621">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d3-621">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="241d3-622">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d3-622">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="241d3-623">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="241d3-623">Method countryRegionCodes</span></span>

<span data-ttu-id="241d3-624">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-624">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="241d3-625">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="241d3-625">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="241d3-626">値</span><span class="sxs-lookup"><span data-stu-id="241d3-626">value</span></span>  
<span data-ttu-id="241d3-627">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-627">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="241d3-628">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="241d3-628">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="241d3-629">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="241d3-629">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="241d3-630">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="241d3-630">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="241d3-631">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="241d3-631">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="241d3-632">値</span><span class="sxs-lookup"><span data-stu-id="241d3-632">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="241d3-633">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="241d3-633">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="241d3-634">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="241d3-634">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="241d3-635">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="241d3-635">Parameters - dataField</span></span>

<span data-ttu-id="241d3-636">値</span><span class="sxs-lookup"><span data-stu-id="241d3-636">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="241d3-637">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="241d3-637">Return Value - dataField</span></span>

## <a name="method-datafieldarrayindex"></a><span data-ttu-id="241d3-638">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-638">Method dataFieldArrayIndex</span></span>

```xpp
public int dataFieldArrayIndex()
```

### <a name="return-value---datafieldarrayindex"></a><span data-ttu-id="241d3-639">戻り値 - dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-639">Return Value - dataFieldArrayIndex</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="241d3-640">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="241d3-640">Method dataFieldName</span></span>

```xpp
public FieldName dataFieldName()
```

### <a name="return-value---datafieldname"></a><span data-ttu-id="241d3-641">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="241d3-641">Return Value - dataFieldName</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="241d3-642">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-642">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="241d3-643">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-643">Parameters - dataMethod</span></span>

<span data-ttu-id="241d3-644">値</span><span class="sxs-lookup"><span data-stu-id="241d3-644">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="241d3-645">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-645">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="241d3-646">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="241d3-646">Method dataRelationPath</span></span>

<span data-ttu-id="241d3-647">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-647">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="241d3-648">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="241d3-648">Parameters - dataRelationPath</span></span>

<span data-ttu-id="241d3-649">値</span><span class="sxs-lookup"><span data-stu-id="241d3-649">value</span></span>  
<span data-ttu-id="241d3-650">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-650">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="241d3-651">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="241d3-651">Return Value - dataRelationPath</span></span>

<span data-ttu-id="241d3-652">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="241d3-652">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="241d3-653">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="241d3-653">Remarks - dataRelationPath</span></span>

<span data-ttu-id="241d3-654">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="241d3-654">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="241d3-655">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="241d3-655">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="241d3-656">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="241d3-656">Method dataSource</span></span>

<span data-ttu-id="241d3-657">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-657">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="241d3-658">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="241d3-658">Parameters - dataSource</span></span>

<span data-ttu-id="241d3-659">値</span><span class="sxs-lookup"><span data-stu-id="241d3-659">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="241d3-660">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="241d3-660">Return Value - dataSource</span></span>

<span data-ttu-id="241d3-661">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="241d3-661">The identifier of the data source that will be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="241d3-662">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="241d3-662">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="241d3-663">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="241d3-663">Parameters - direction</span></span>

<span data-ttu-id="241d3-664">値</span><span class="sxs-lookup"><span data-stu-id="241d3-664">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="241d3-665">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="241d3-665">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="241d3-666">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-666">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="241d3-667">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-667">Parameters - displayHeight</span></span>

<span data-ttu-id="241d3-668">値</span><span class="sxs-lookup"><span data-stu-id="241d3-668">value</span></span>  

<!-- -->

<span data-ttu-id="241d3-669">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-669">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="241d3-670">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-670">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="241d3-671">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-671">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="241d3-672">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-672">Parameters - displayHeightMode</span></span>

<span data-ttu-id="241d3-673">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-673">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="241d3-674">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-674">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="241d3-675">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-675">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="241d3-676">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-676">Parameters - displayHeightValue</span></span>

<span data-ttu-id="241d3-677">値</span><span class="sxs-lookup"><span data-stu-id="241d3-677">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="241d3-678">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-678">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="241d3-679">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="241d3-679">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="241d3-680">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="241d3-680">Parameters - displayLength</span></span>

<span data-ttu-id="241d3-681">値</span><span class="sxs-lookup"><span data-stu-id="241d3-681">value</span></span>  

<!-- -->

<span data-ttu-id="241d3-682">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-682">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="241d3-683">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="241d3-683">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="241d3-684">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-684">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="241d3-685">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-685">Parameters - displayLengthMode</span></span>

<span data-ttu-id="241d3-686">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-686">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="241d3-687">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-687">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="241d3-688">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-688">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="241d3-689">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-689">Parameters - displayLengthValue</span></span>

<span data-ttu-id="241d3-690">値</span><span class="sxs-lookup"><span data-stu-id="241d3-690">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="241d3-691">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-691">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="241d3-692">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="241d3-692">Method displayTarget</span></span>

<span data-ttu-id="241d3-693">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-693">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="241d3-694">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="241d3-694">Parameters - displayTarget</span></span>

<span data-ttu-id="241d3-695">値</span><span class="sxs-lookup"><span data-stu-id="241d3-695">value</span></span>  
<span data-ttu-id="241d3-696">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-696">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="241d3-697">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="241d3-697">Return Value - displayTarget</span></span>

<span data-ttu-id="241d3-698">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="241d3-698">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="241d3-699">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="241d3-699">Method dragDrop</span></span>

<span data-ttu-id="241d3-700">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-700">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="241d3-701">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="241d3-701">Parameters - dragDrop</span></span>

<span data-ttu-id="241d3-702">値</span><span class="sxs-lookup"><span data-stu-id="241d3-702">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="241d3-703">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="241d3-703">Return Value - dragDrop</span></span>

<span data-ttu-id="241d3-704">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="241d3-704">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="241d3-705">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="241d3-705">Method dragOver</span></span>

<span data-ttu-id="241d3-706">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-706">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="241d3-707">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="241d3-707">Parameters - dragOver</span></span>

<span data-ttu-id="241d3-708">dragSource</span><span class="sxs-lookup"><span data-stu-id="241d3-708">dragSource</span></span>  
<span data-ttu-id="241d3-709">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-709">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-710">dragMode</span><span class="sxs-lookup"><span data-stu-id="241d3-710">dragMode</span></span>  
<span data-ttu-id="241d3-711">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-711">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-712">x</span><span class="sxs-lookup"><span data-stu-id="241d3-712">x</span></span>  
<span data-ttu-id="241d3-713">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-713">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-714">y</span><span class="sxs-lookup"><span data-stu-id="241d3-714">y</span></span>  
<span data-ttu-id="241d3-715">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-715">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="241d3-716">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="241d3-716">Return Value - dragOver</span></span>

<span data-ttu-id="241d3-717">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="241d3-717">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="241d3-718">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="241d3-718">Method dragOverEx</span></span>

<span data-ttu-id="241d3-719">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-719">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="241d3-720">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="241d3-720">Parameters - dragOverEx</span></span>

<span data-ttu-id="241d3-721">dragSource</span><span class="sxs-lookup"><span data-stu-id="241d3-721">dragSource</span></span>  
<span data-ttu-id="241d3-722">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-722">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-723">dragMode</span><span class="sxs-lookup"><span data-stu-id="241d3-723">dragMode</span></span>  
<span data-ttu-id="241d3-724">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-724">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-725">x</span><span class="sxs-lookup"><span data-stu-id="241d3-725">x</span></span>  
<span data-ttu-id="241d3-726">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-726">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-727">y</span><span class="sxs-lookup"><span data-stu-id="241d3-727">y</span></span>  
<span data-ttu-id="241d3-728">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-728">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="241d3-729">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="241d3-729">Return Value - dragOverEx</span></span>

<span data-ttu-id="241d3-730">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="241d3-730">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="241d3-731">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="241d3-731">Method dragText</span></span>

<span data-ttu-id="241d3-732">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-732">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="241d3-733">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="241d3-733">Return Value - dragText</span></span>

<span data-ttu-id="241d3-734">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="241d3-734">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="241d3-735">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="241d3-735">Method enabled</span></span>

<span data-ttu-id="241d3-736">オブジェクトを有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-736">Indicates whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="241d3-737">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="241d3-737">Parameters - enabled</span></span>

<span data-ttu-id="241d3-738">値</span><span class="sxs-lookup"><span data-stu-id="241d3-738">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="241d3-739">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="241d3-739">Return Value - enabled</span></span>

<span data-ttu-id="241d3-740">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-740">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="241d3-741">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="241d3-741">Remarks - enabled</span></span>

<span data-ttu-id="241d3-742">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="241d3-742">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="241d3-743">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="241d3-743">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="241d3-744">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="241d3-744">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="241d3-745">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="241d3-745">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="241d3-746">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="241d3-746">Parameters - extendedDataType</span></span>

<span data-ttu-id="241d3-747">値</span><span class="sxs-lookup"><span data-stu-id="241d3-747">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="241d3-748">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="241d3-748">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="241d3-749">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="241d3-749">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="241d3-750">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="241d3-750">Parameters - fastTabSummary</span></span>

<span data-ttu-id="241d3-751">値</span><span class="sxs-lookup"><span data-stu-id="241d3-751">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="241d3-752">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="241d3-752">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="241d3-753">メソッド font</span><span class="sxs-lookup"><span data-stu-id="241d3-753">Method font</span></span>

<span data-ttu-id="241d3-754">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-754">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="241d3-755">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="241d3-755">Parameters - font</span></span>

<span data-ttu-id="241d3-756">値</span><span class="sxs-lookup"><span data-stu-id="241d3-756">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="241d3-757">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="241d3-757">Return Value - font</span></span>

<span data-ttu-id="241d3-758">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="241d3-758">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="241d3-759">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="241d3-759">Method fontSize</span></span>

<span data-ttu-id="241d3-760">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-760">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="241d3-761">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="241d3-761">Parameters - fontSize</span></span>

<span data-ttu-id="241d3-762">値</span><span class="sxs-lookup"><span data-stu-id="241d3-762">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="241d3-763">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="241d3-763">Return Value - fontSize</span></span>

<span data-ttu-id="241d3-764">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="241d3-764">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="241d3-765">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-765">Method foregroundColor</span></span>

<span data-ttu-id="241d3-766">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-766">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="241d3-767">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-767">Parameters - foregroundColor</span></span>

<span data-ttu-id="241d3-768">値</span><span class="sxs-lookup"><span data-stu-id="241d3-768">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="241d3-769">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-769">Return Value - foregroundColor</span></span>

<span data-ttu-id="241d3-770">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="241d3-770">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="241d3-771">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-771">Remarks - foregroundColor</span></span>

<span data-ttu-id="241d3-772">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="241d3-772">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="241d3-773">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="241d3-773">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="241d3-774">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="241d3-774">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="241d3-775">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="241d3-775">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="241d3-776">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="241d3-776">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="241d3-777">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="241d3-777">The maximum value for a single byte is 255.</span></span>

## <a name="method-getcursorpos"></a><span data-ttu-id="241d3-778">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="241d3-778">Method getCursorPos</span></span>

```xpp
public container getCursorPos()
```

### <a name="return-value---getcursorpos"></a><span data-ttu-id="241d3-779">戻り値 - getCursorPos</span><span class="sxs-lookup"><span data-stu-id="241d3-779">Return Value - getCursorPos</span></span>

## <a name="method-getfirstvisibleline"></a><span data-ttu-id="241d3-780">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="241d3-780">Method getFirstVisibleLine</span></span>

```xpp
public int getFirstVisibleLine()
```

### <a name="return-value---getfirstvisibleline"></a><span data-ttu-id="241d3-781">戻り値 - getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="241d3-781">Return Value - getFirstVisibleLine</span></span>

## <a name="method-getline"></a><span data-ttu-id="241d3-782">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="241d3-782">Method getLine</span></span>

```xpp
public str getLine(int lineNo)
```

### <a name="parameters---getline"></a><span data-ttu-id="241d3-783">パラメーター - getLine</span><span class="sxs-lookup"><span data-stu-id="241d3-783">Parameters - getLine</span></span>

<span data-ttu-id="241d3-784">lineNo</span><span class="sxs-lookup"><span data-stu-id="241d3-784">lineNo</span></span>  

### <a name="return-value---getline"></a><span data-ttu-id="241d3-785">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="241d3-785">Return Value - getLine</span></span>

## <a name="method-getlinecount"></a><span data-ttu-id="241d3-786">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="241d3-786">Method getLineCount</span></span>

```xpp
public int getLineCount()
```

### <a name="return-value---getlinecount"></a><span data-ttu-id="241d3-787">戻り値 - getLineCount</span><span class="sxs-lookup"><span data-stu-id="241d3-787">Return Value - getLineCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="241d3-788">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="241d3-788">Method getSelection</span></span>

```xpp
public container getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="241d3-789">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="241d3-789">Return Value - getSelection</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="241d3-790">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="241d3-790">Method hasChanged</span></span>

<span data-ttu-id="241d3-791">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-791">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="241d3-792">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="241d3-792">Parameters - hasChanged</span></span>

<span data-ttu-id="241d3-793">val</span><span class="sxs-lookup"><span data-stu-id="241d3-793">val</span></span>  
<span data-ttu-id="241d3-794">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-794">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="241d3-795">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="241d3-795">Return Value - hasChanged</span></span>

<span data-ttu-id="241d3-796">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-796">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="241d3-797">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="241d3-797">Method hasUserSetting</span></span>

<span data-ttu-id="241d3-798">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-798">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="241d3-799">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="241d3-799">Return Value - hasUserSetting</span></span>

<span data-ttu-id="241d3-800">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-800">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="241d3-801">メソッド height</span><span class="sxs-lookup"><span data-stu-id="241d3-801">Method height</span></span>

<span data-ttu-id="241d3-802">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-802">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="241d3-803">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="241d3-803">Parameters - height</span></span>

<span data-ttu-id="241d3-804">値</span><span class="sxs-lookup"><span data-stu-id="241d3-804">value</span></span>  

<!-- -->

<span data-ttu-id="241d3-805">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-805">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="241d3-806">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="241d3-806">Return Value - height</span></span>

<span data-ttu-id="241d3-807">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="241d3-807">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="241d3-808">備考 - height</span><span class="sxs-lookup"><span data-stu-id="241d3-808">Remarks - height</span></span>

<span data-ttu-id="241d3-809">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-809">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="241d3-810">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="241d3-810">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="241d3-811">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-811">Mode</span></span>            | <span data-ttu-id="241d3-812">高さの計算</span><span class="sxs-lookup"><span data-stu-id="241d3-812">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d3-813">-1 正確</span><span class="sxs-lookup"><span data-stu-id="241d3-813">-1 Exact</span></span>        | <span data-ttu-id="241d3-814">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-814">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="241d3-815">0 自動</span><span class="sxs-lookup"><span data-stu-id="241d3-815">0 Auto</span></span>          | <span data-ttu-id="241d3-816">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-816">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="241d3-817">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="241d3-817">1 Column height</span></span> | <span data-ttu-id="241d3-818">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="241d3-818">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="241d3-819">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="241d3-819">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="241d3-820">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-820">Method heightMode</span></span>

<span data-ttu-id="241d3-821">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-821">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="241d3-822">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-822">Parameters - heightMode</span></span>

<span data-ttu-id="241d3-823">値</span><span class="sxs-lookup"><span data-stu-id="241d3-823">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="241d3-824">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-824">Return Value - heightMode</span></span>

<span data-ttu-id="241d3-825">計算モード。</span><span class="sxs-lookup"><span data-stu-id="241d3-825">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="241d3-826">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-826">Remarks - heightMode</span></span>

<span data-ttu-id="241d3-827">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="241d3-827">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="241d3-828">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-828">Mode</span></span>          | <span data-ttu-id="241d3-829">高さの計算</span><span class="sxs-lookup"><span data-stu-id="241d3-829">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d3-830">正確</span><span class="sxs-lookup"><span data-stu-id="241d3-830">Exact</span></span>         | <span data-ttu-id="241d3-831">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-831">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="241d3-832">自動</span><span class="sxs-lookup"><span data-stu-id="241d3-832">Auto</span></span>          | <span data-ttu-id="241d3-833">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-833">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="241d3-834">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="241d3-834">Column height</span></span> | <span data-ttu-id="241d3-835">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="241d3-835">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="241d3-836">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="241d3-836">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="241d3-837">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-837">Method heightValue</span></span>

<span data-ttu-id="241d3-838">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-838">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="241d3-839">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-839">Parameters - heightValue</span></span>

<span data-ttu-id="241d3-840">値</span><span class="sxs-lookup"><span data-stu-id="241d3-840">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="241d3-841">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-841">Return Value - heightValue</span></span>

<span data-ttu-id="241d3-842">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="241d3-842">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="241d3-843">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-843">Remarks - heightValue</span></span>

<span data-ttu-id="241d3-844">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="241d3-844">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="241d3-845">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="241d3-845">Method helpField</span></span>

<span data-ttu-id="241d3-846">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-846">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="241d3-847">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="241d3-847">Return Value - helpField</span></span>

<span data-ttu-id="241d3-848">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="241d3-848">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="241d3-849">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="241d3-849">Remarks - helpField</span></span>

<span data-ttu-id="241d3-850">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="241d3-850">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="241d3-851">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="241d3-851">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="241d3-852">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="241d3-852">Method helpText</span></span>

<span data-ttu-id="241d3-853">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-853">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="241d3-854">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="241d3-854">Parameters - helpText</span></span>

<span data-ttu-id="241d3-855">値</span><span class="sxs-lookup"><span data-stu-id="241d3-855">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="241d3-856">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="241d3-856">Return Value - helpText</span></span>

<span data-ttu-id="241d3-857">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="241d3-857">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="241d3-858">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="241d3-858">Remarks - helpText</span></span>

<span data-ttu-id="241d3-859">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-859">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="241d3-860">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="241d3-860">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="241d3-861">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="241d3-861">Method hierarchyParent</span></span>

<span data-ttu-id="241d3-862">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-862">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="241d3-863">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="241d3-863">Parameters - hierarchyParent</span></span>

<span data-ttu-id="241d3-864">値</span><span class="sxs-lookup"><span data-stu-id="241d3-864">value</span></span>  
<span data-ttu-id="241d3-865">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="241d3-865">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="241d3-866">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="241d3-866">Return Value - hierarchyParent</span></span>

<span data-ttu-id="241d3-867">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="241d3-867">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="241d3-868">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="241d3-868">Method hWnd</span></span>

<span data-ttu-id="241d3-869">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-869">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="241d3-870">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="241d3-870">Return Value - hWnd</span></span>

<span data-ttu-id="241d3-871">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="241d3-871">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="241d3-872">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="241d3-872">Remarks - hWnd</span></span>

<span data-ttu-id="241d3-873">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="241d3-873">The handle can be used with the Windows API.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="241d3-874">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="241d3-874">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="241d3-875">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="241d3-875">Parameters - iMEMode</span></span>

<span data-ttu-id="241d3-876">値</span><span class="sxs-lookup"><span data-stu-id="241d3-876">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="241d3-877">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="241d3-877">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="241d3-878">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="241d3-878">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="241d3-879">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="241d3-879">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="241d3-880">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="241d3-880">Method isDisplayed</span></span>

<span data-ttu-id="241d3-881">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-881">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="241d3-882">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="241d3-882">Return Value - isDisplayed</span></span>

<span data-ttu-id="241d3-883">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="241d3-883">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="241d3-884">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="241d3-884">Remarks - isDisplayed</span></span>

<span data-ttu-id="241d3-885">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="241d3-885">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="241d3-886">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="241d3-886">Method isRestricted</span></span>

<span data-ttu-id="241d3-887">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-887">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="241d3-888">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="241d3-888">Return Value - isRestricted</span></span>

<span data-ttu-id="241d3-889">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="241d3-889">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="241d3-890">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="241d3-890">Method isUserSetupEnabled</span></span>

<span data-ttu-id="241d3-891">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-891">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="241d3-892">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="241d3-892">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="241d3-893">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="241d3-893">neededSetupRights</span></span>  
<span data-ttu-id="241d3-894">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="241d3-894">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="241d3-895">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="241d3-895">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="241d3-896">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-896">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="241d3-897">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="241d3-897">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="241d3-898">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="241d3-898">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d3-899">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="241d3-899">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="241d3-900">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="241d3-900">No changes can be made to the control.</span></span> <span data-ttu-id="241d3-901">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-901">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="241d3-902">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="241d3-902">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="241d3-903">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="241d3-903">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="241d3-904">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="241d3-904">The user cannot move the control.</span></span>   |
| <span data-ttu-id="241d3-905">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="241d3-905">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="241d3-906">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="241d3-906">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="241d3-907">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="241d3-907">The user can also move the control.</span></span> |

<span data-ttu-id="241d3-908">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="241d3-908">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="241d3-909">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="241d3-909">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="241d3-910">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="241d3-910">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="241d3-911">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="241d3-911">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="241d3-912">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="241d3-912">Parameters - italic</span></span>

<span data-ttu-id="241d3-913">値</span><span class="sxs-lookup"><span data-stu-id="241d3-913">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="241d3-914">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="241d3-914">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="241d3-915">メソッド label</span><span class="sxs-lookup"><span data-stu-id="241d3-915">Method label</span></span>

<span data-ttu-id="241d3-916">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-916">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="241d3-917">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="241d3-917">Parameters - label</span></span>

<span data-ttu-id="241d3-918">値</span><span class="sxs-lookup"><span data-stu-id="241d3-918">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="241d3-919">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="241d3-919">Return Value - label</span></span>

<span data-ttu-id="241d3-920">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="241d3-920">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="241d3-921">備考 - label</span><span class="sxs-lookup"><span data-stu-id="241d3-921">Remarks - label</span></span>

<span data-ttu-id="241d3-922">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-922">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="241d3-923">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="241d3-923">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="241d3-924">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="241d3-924">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="241d3-925">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="241d3-925">Parameters - labelAlignment</span></span>

<span data-ttu-id="241d3-926">値</span><span class="sxs-lookup"><span data-stu-id="241d3-926">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="241d3-927">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="241d3-927">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="241d3-928">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="241d3-928">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="241d3-929">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="241d3-929">Parameters - labelBold</span></span>

<span data-ttu-id="241d3-930">値</span><span class="sxs-lookup"><span data-stu-id="241d3-930">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="241d3-931">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="241d3-931">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="241d3-932">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="241d3-932">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="241d3-933">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="241d3-933">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="241d3-934">値</span><span class="sxs-lookup"><span data-stu-id="241d3-934">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="241d3-935">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="241d3-935">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="241d3-936">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="241d3-936">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="241d3-937">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="241d3-937">Parameters - labelFont</span></span>

<span data-ttu-id="241d3-938">値</span><span class="sxs-lookup"><span data-stu-id="241d3-938">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="241d3-939">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="241d3-939">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="241d3-940">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="241d3-940">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="241d3-941">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="241d3-941">Parameters - labelFontSize</span></span>

<span data-ttu-id="241d3-942">値</span><span class="sxs-lookup"><span data-stu-id="241d3-942">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="241d3-943">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="241d3-943">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="241d3-944">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-944">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="241d3-945">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-945">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="241d3-946">値</span><span class="sxs-lookup"><span data-stu-id="241d3-946">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="241d3-947">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="241d3-947">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="241d3-948">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="241d3-948">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="241d3-949">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="241d3-949">Parameters - labelGuide</span></span>

<span data-ttu-id="241d3-950">値</span><span class="sxs-lookup"><span data-stu-id="241d3-950">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="241d3-951">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="241d3-951">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="241d3-952">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-952">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="241d3-953">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-953">Parameters - labelHeight</span></span>

<span data-ttu-id="241d3-954">値</span><span class="sxs-lookup"><span data-stu-id="241d3-954">value</span></span>  

<!-- -->

<span data-ttu-id="241d3-955">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-955">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="241d3-956">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-956">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="241d3-957">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-957">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="241d3-958">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-958">Parameters - labelHeightMode</span></span>

<span data-ttu-id="241d3-959">値</span><span class="sxs-lookup"><span data-stu-id="241d3-959">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="241d3-960">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="241d3-960">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="241d3-961">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-961">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="241d3-962">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-962">Parameters - labelHeightValue</span></span>

<span data-ttu-id="241d3-963">値</span><span class="sxs-lookup"><span data-stu-id="241d3-963">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="241d3-964">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="241d3-964">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="241d3-965">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="241d3-965">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="241d3-966">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="241d3-966">Parameters - labelItalic</span></span>

<span data-ttu-id="241d3-967">値</span><span class="sxs-lookup"><span data-stu-id="241d3-967">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="241d3-968">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="241d3-968">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="241d3-969">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="241d3-969">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="241d3-970">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="241d3-970">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="241d3-971">x</span><span class="sxs-lookup"><span data-stu-id="241d3-971">x</span></span>  

<!-- -->

<span data-ttu-id="241d3-972">y</span><span class="sxs-lookup"><span data-stu-id="241d3-972">y</span></span>  

<!-- -->

<span data-ttu-id="241d3-973">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-973">button</span></span>  

<!-- -->

<span data-ttu-id="241d3-974">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-974">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="241d3-975">Shift</span><span class="sxs-lookup"><span data-stu-id="241d3-975">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="241d3-976">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="241d3-976">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="241d3-977">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="241d3-977">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="241d3-978">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="241d3-978">Parameters - labelMouseDown</span></span>

<span data-ttu-id="241d3-979">x</span><span class="sxs-lookup"><span data-stu-id="241d3-979">x</span></span>  

<!-- -->

<span data-ttu-id="241d3-980">y</span><span class="sxs-lookup"><span data-stu-id="241d3-980">y</span></span>  

<!-- -->

<span data-ttu-id="241d3-981">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-981">button</span></span>  

<!-- -->

<span data-ttu-id="241d3-982">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-982">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="241d3-983">Shift</span><span class="sxs-lookup"><span data-stu-id="241d3-983">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="241d3-984">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="241d3-984">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="241d3-985">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="241d3-985">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="241d3-986">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="241d3-986">Parameters - labelMouseUp</span></span>

<span data-ttu-id="241d3-987">x</span><span class="sxs-lookup"><span data-stu-id="241d3-987">x</span></span>  

<!-- -->

<span data-ttu-id="241d3-988">y</span><span class="sxs-lookup"><span data-stu-id="241d3-988">y</span></span>  

<!-- -->

<span data-ttu-id="241d3-989">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-989">button</span></span>  

<!-- -->

<span data-ttu-id="241d3-990">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-990">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="241d3-991">Shift</span><span class="sxs-lookup"><span data-stu-id="241d3-991">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="241d3-992">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="241d3-992">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="241d3-993">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="241d3-993">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="241d3-994">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="241d3-994">Parameters - labelPosition</span></span>

<span data-ttu-id="241d3-995">値</span><span class="sxs-lookup"><span data-stu-id="241d3-995">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="241d3-996">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="241d3-996">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="241d3-997">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="241d3-997">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="241d3-998">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="241d3-998">Parameters - labelUnderline</span></span>

<span data-ttu-id="241d3-999">値</span><span class="sxs-lookup"><span data-stu-id="241d3-999">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="241d3-1000">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="241d3-1000">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="241d3-1001">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="241d3-1001">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="241d3-1002">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="241d3-1002">Parameters - labelWidth</span></span>

<span data-ttu-id="241d3-1003">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1003">value</span></span>  

<!-- -->

<span data-ttu-id="241d3-1004">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1004">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="241d3-1005">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="241d3-1005">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="241d3-1006">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1006">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="241d3-1007">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1007">Parameters - labelWidthMode</span></span>

<span data-ttu-id="241d3-1008">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1008">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="241d3-1009">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1009">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="241d3-1010">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1010">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="241d3-1011">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1011">Parameters - labelWidthValue</span></span>

<span data-ttu-id="241d3-1012">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1012">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="241d3-1013">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1013">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="241d3-1014">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="241d3-1014">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="241d3-1015">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="241d3-1015">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="241d3-1016">メソッド left</span><span class="sxs-lookup"><span data-stu-id="241d3-1016">Method left</span></span>

<span data-ttu-id="241d3-1017">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1017">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="241d3-1018">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="241d3-1018">Parameters - left</span></span>

<span data-ttu-id="241d3-1019">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1019">value</span></span>  
<span data-ttu-id="241d3-1020">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1020">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="241d3-1021">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1021">mode</span></span>  
<span data-ttu-id="241d3-1022">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1022">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="241d3-1023">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="241d3-1023">Return Value - left</span></span>

<span data-ttu-id="241d3-1024">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="241d3-1024">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="241d3-1025">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1025">Method leftMode</span></span>

<span data-ttu-id="241d3-1026">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1026">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="241d3-1027">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1027">Parameters - leftMode</span></span>

<span data-ttu-id="241d3-1028">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1028">value</span></span>  
<span data-ttu-id="241d3-1029">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1029">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="241d3-1030">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1030">Return Value - leftMode</span></span>

<span data-ttu-id="241d3-1031">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="241d3-1031">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="241d3-1032">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1032">Method leftValue</span></span>

<span data-ttu-id="241d3-1033">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1033">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="241d3-1034">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1034">Parameters - leftValue</span></span>

<span data-ttu-id="241d3-1035">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1035">value</span></span>  
<span data-ttu-id="241d3-1036">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1036">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="241d3-1037">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1037">Return Value - leftValue</span></span>

<span data-ttu-id="241d3-1038">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="241d3-1038">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="241d3-1039">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="241d3-1039">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="241d3-1040">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="241d3-1040">Parameters - limitText</span></span>

<span data-ttu-id="241d3-1041">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1041">value</span></span>  

<!-- -->

<span data-ttu-id="241d3-1042">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1042">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="241d3-1043">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="241d3-1043">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="241d3-1044">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1044">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="241d3-1045">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1045">Parameters - limitTextMode</span></span>

<span data-ttu-id="241d3-1046">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1046">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="241d3-1047">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1047">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="241d3-1048">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1048">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="241d3-1049">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1049">Parameters - limitTextValue</span></span>

<span data-ttu-id="241d3-1050">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1050">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="241d3-1051">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1051">Return Value - limitTextValue</span></span>

## <a name="method-linefromchar"></a><span data-ttu-id="241d3-1052">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="241d3-1052">Method lineFromChar</span></span>

```xpp
public int lineFromChar(int charIndex)
```

### <a name="parameters---linefromchar"></a><span data-ttu-id="241d3-1053">パラメーター - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="241d3-1053">Parameters - lineFromChar</span></span>

<span data-ttu-id="241d3-1054">charIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-1054">charIndex</span></span>  

### <a name="return-value---linefromchar"></a><span data-ttu-id="241d3-1055">戻り値 - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="241d3-1055">Return Value - lineFromChar</span></span>

## <a name="method-lineindex"></a><span data-ttu-id="241d3-1056">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-1056">Method lineIndex</span></span>

```xpp
public int lineIndex(int lineNo)
```

### <a name="parameters---lineindex"></a><span data-ttu-id="241d3-1057">パラメーター - lineIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-1057">Parameters - lineIndex</span></span>

<span data-ttu-id="241d3-1058">lineNo</span><span class="sxs-lookup"><span data-stu-id="241d3-1058">lineNo</span></span>  

### <a name="return-value---lineindex"></a><span data-ttu-id="241d3-1059">戻り値 - lineIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-1059">Return Value - lineIndex</span></span>

## <a name="method-linelength"></a><span data-ttu-id="241d3-1060">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="241d3-1060">Method lineLength</span></span>

```xpp
public int lineLength(int lineNo)
```

### <a name="parameters---linelength"></a><span data-ttu-id="241d3-1061">パラメーター - lineLength</span><span class="sxs-lookup"><span data-stu-id="241d3-1061">Parameters - lineLength</span></span>

<span data-ttu-id="241d3-1062">lineNo</span><span class="sxs-lookup"><span data-stu-id="241d3-1062">lineNo</span></span>  

### <a name="return-value---linelength"></a><span data-ttu-id="241d3-1063">戻り値 - lineLength</span><span class="sxs-lookup"><span data-stu-id="241d3-1063">Return Value - lineLength</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="241d3-1064">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="241d3-1064">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="241d3-1065">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="241d3-1065">Parameters - lookupButton</span></span>

<span data-ttu-id="241d3-1066">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1066">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="241d3-1067">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="241d3-1067">Return Value - lookupButton</span></span>

## <a name="method-lookuponly"></a><span data-ttu-id="241d3-1068">メソッド lookupOnly</span><span class="sxs-lookup"><span data-stu-id="241d3-1068">Method lookupOnly</span></span>

```xpp
public boolean lookupOnly([boolean value])
```

### <a name="parameters---lookuponly"></a><span data-ttu-id="241d3-1069">パラメーター - lookupOnly</span><span class="sxs-lookup"><span data-stu-id="241d3-1069">Parameters - lookupOnly</span></span>

<span data-ttu-id="241d3-1070">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1070">value</span></span>  

### <a name="return-value---lookuponly"></a><span data-ttu-id="241d3-1071">戻り値 - lookupOnly</span><span class="sxs-lookup"><span data-stu-id="241d3-1071">Return Value - lookupOnly</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="241d3-1072">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="241d3-1072">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="241d3-1073">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="241d3-1073">Parameters - mandatory</span></span>

<span data-ttu-id="241d3-1074">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1074">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="241d3-1075">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="241d3-1075">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="241d3-1076">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="241d3-1076">Method markAsUserAdd</span></span>

<span data-ttu-id="241d3-1077">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="241d3-1077">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="241d3-1078">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="241d3-1078">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="241d3-1079">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1079">value</span></span>  
<span data-ttu-id="241d3-1080">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1080">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="241d3-1081">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="241d3-1081">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="241d3-1082">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-1082">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="241d3-1083">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="241d3-1083">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="241d3-1084">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="241d3-1084">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="241d3-1085">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="241d3-1085">Method mouseDblClick</span></span>

<span data-ttu-id="241d3-1086">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1086">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="241d3-1087">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="241d3-1087">Parameters - mouseDblClick</span></span>

<span data-ttu-id="241d3-1088">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1088">x</span></span>  
<span data-ttu-id="241d3-1089">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1089">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1090">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1090">y</span></span>  
<span data-ttu-id="241d3-1091">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1091">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1092">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-1092">button</span></span>  
<span data-ttu-id="241d3-1093">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1093">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1094">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-1094">Ctrl</span></span>  
<span data-ttu-id="241d3-1095">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1095">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1096">シフト</span><span class="sxs-lookup"><span data-stu-id="241d3-1096">Shift</span></span>  
<span data-ttu-id="241d3-1097">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1097">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="241d3-1098">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="241d3-1098">Return Value - mouseDblClick</span></span>

<span data-ttu-id="241d3-1099">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1099">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="241d3-1100">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="241d3-1100">Remarks - mouseDblClick</span></span>

<span data-ttu-id="241d3-1101">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1101">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="241d3-1102">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="241d3-1102">Method mouseDown</span></span>

<span data-ttu-id="241d3-1103">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1103">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="241d3-1104">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="241d3-1104">Parameters - mouseDown</span></span>

<span data-ttu-id="241d3-1105">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1105">x</span></span>  
<span data-ttu-id="241d3-1106">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1106">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1107">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1107">y</span></span>  
<span data-ttu-id="241d3-1108">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1108">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1109">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-1109">button</span></span>  
<span data-ttu-id="241d3-1110">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1110">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1111">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-1111">Ctrl</span></span>  
<span data-ttu-id="241d3-1112">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1112">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1113">シフト</span><span class="sxs-lookup"><span data-stu-id="241d3-1113">Shift</span></span>  
<span data-ttu-id="241d3-1114">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1114">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="241d3-1115">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="241d3-1115">Return Value - mouseDown</span></span>

<span data-ttu-id="241d3-1116">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1116">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="241d3-1117">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="241d3-1117">Remarks - mouseDown</span></span>

<span data-ttu-id="241d3-1118">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1118">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="241d3-1119">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1119">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="241d3-1120">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="241d3-1120">Method mouseMove</span></span>

<span data-ttu-id="241d3-1121">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1121">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="241d3-1122">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="241d3-1122">Parameters - mouseMove</span></span>

<span data-ttu-id="241d3-1123">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1123">x</span></span>  
<span data-ttu-id="241d3-1124">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1124">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1125">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1125">y</span></span>  
<span data-ttu-id="241d3-1126">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1126">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1127">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-1127">button</span></span>  
<span data-ttu-id="241d3-1128">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1128">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1129">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-1129">Ctrl</span></span>  
<span data-ttu-id="241d3-1130">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1130">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1131">シフト</span><span class="sxs-lookup"><span data-stu-id="241d3-1131">Shift</span></span>  
<span data-ttu-id="241d3-1132">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1132">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="241d3-1133">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="241d3-1133">Return Value - mouseMove</span></span>

<span data-ttu-id="241d3-1134">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1134">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="241d3-1135">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="241d3-1135">Remarks - mouseMove</span></span>

<span data-ttu-id="241d3-1136">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1136">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="241d3-1137">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="241d3-1137">Method mouseUp</span></span>

<span data-ttu-id="241d3-1138">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1138">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="241d3-1139">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="241d3-1139">Parameters - mouseUp</span></span>

<span data-ttu-id="241d3-1140">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1140">x</span></span>  
<span data-ttu-id="241d3-1141">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1141">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1142">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1142">y</span></span>  
<span data-ttu-id="241d3-1143">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1143">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1144">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-1144">button</span></span>  
<span data-ttu-id="241d3-1145">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1145">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1146">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-1146">Ctrl</span></span>  
<span data-ttu-id="241d3-1147">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1147">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1148">シフト</span><span class="sxs-lookup"><span data-stu-id="241d3-1148">Shift</span></span>  
<span data-ttu-id="241d3-1149">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1149">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="241d3-1150">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="241d3-1150">Return Value - mouseUp</span></span>

<span data-ttu-id="241d3-1151">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1151">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="241d3-1152">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="241d3-1152">Remarks - mouseUp</span></span>

<span data-ttu-id="241d3-1153">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1153">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="241d3-1154">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1154">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-multiline"></a><span data-ttu-id="241d3-1155">メソッド multiLine</span><span class="sxs-lookup"><span data-stu-id="241d3-1155">Method multiLine</span></span>

```xpp
public boolean multiLine([boolean value])
```

### <a name="parameters---multiline"></a><span data-ttu-id="241d3-1156">パラメーター - multiLine</span><span class="sxs-lookup"><span data-stu-id="241d3-1156">Parameters - multiLine</span></span>

<span data-ttu-id="241d3-1157">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1157">value</span></span>  

### <a name="return-value---multiline"></a><span data-ttu-id="241d3-1158">戻り値 - multiLine</span><span class="sxs-lookup"><span data-stu-id="241d3-1158">Return Value - multiLine</span></span>

## <a name="method-name"></a><span data-ttu-id="241d3-1159">メソッド名</span><span class="sxs-lookup"><span data-stu-id="241d3-1159">Method name</span></span>

<span data-ttu-id="241d3-1160">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1160">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="241d3-1161">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="241d3-1161">Parameters - name</span></span>

<span data-ttu-id="241d3-1162">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1162">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="241d3-1163">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="241d3-1163">Return Value - name</span></span>

<span data-ttu-id="241d3-1164">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="241d3-1164">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="241d3-1165">備考 - name</span><span class="sxs-lookup"><span data-stu-id="241d3-1165">Remarks - name</span></span>

<span data-ttu-id="241d3-1166">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="241d3-1166">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="241d3-1167">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="241d3-1167">It must start with a letter.</span></span>
-   <span data-ttu-id="241d3-1168">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="241d3-1168">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="241d3-1169">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1169">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="241d3-1170">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="241d3-1170">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="241d3-1171">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="241d3-1171">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="241d3-1172">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="241d3-1172">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="241d3-1173">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="241d3-1173">Parameters - neededPermission</span></span>

<span data-ttu-id="241d3-1174">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1174">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="241d3-1175">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="241d3-1175">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="241d3-1176">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="241d3-1176">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="241d3-1177">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="241d3-1177">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="241d3-1178">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="241d3-1178">Method parentControl</span></span>

<span data-ttu-id="241d3-1179">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1179">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="241d3-1180">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="241d3-1180">Return Value - parentControl</span></span>

<span data-ttu-id="241d3-1181">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="241d3-1181">The parent control for the control.</span></span>

## <a name="method-passwordstyle"></a><span data-ttu-id="241d3-1182">メソッド passwordStyle</span><span class="sxs-lookup"><span data-stu-id="241d3-1182">Method passwordStyle</span></span>

```xpp
public boolean passwordStyle([boolean value])
```

### <a name="parameters---passwordstyle"></a><span data-ttu-id="241d3-1183">パラメーター - passwordStyle</span><span class="sxs-lookup"><span data-stu-id="241d3-1183">Parameters - passwordStyle</span></span>

<span data-ttu-id="241d3-1184">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1184">value</span></span>  

### <a name="return-value---passwordstyle"></a><span data-ttu-id="241d3-1185">戻り値 - passwordStyle</span><span class="sxs-lookup"><span data-stu-id="241d3-1185">Return Value - passwordStyle</span></span>

## <a name="method-posfromchar"></a><span data-ttu-id="241d3-1186">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="241d3-1186">Method posFromChar</span></span>

```xpp
public container posFromChar(int charIndex)
```

### <a name="parameters---posfromchar"></a><span data-ttu-id="241d3-1187">パラメーター - posFromChar</span><span class="sxs-lookup"><span data-stu-id="241d3-1187">Parameters - posFromChar</span></span>

<span data-ttu-id="241d3-1188">charIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-1188">charIndex</span></span>  

### <a name="return-value---posfromchar"></a><span data-ttu-id="241d3-1189">戻り値 - posFromChar</span><span class="sxs-lookup"><span data-stu-id="241d3-1189">Return Value - posFromChar</span></span>

## <a name="method-presencedatafield"></a><span data-ttu-id="241d3-1190">メソッド presenceDataField</span><span class="sxs-lookup"><span data-stu-id="241d3-1190">Method presenceDataField</span></span>

```xpp
public FieldId presenceDataField([FieldId value])
```

### <a name="parameters---presencedatafield"></a><span data-ttu-id="241d3-1191">パラメーター - presenceDataField</span><span class="sxs-lookup"><span data-stu-id="241d3-1191">Parameters - presenceDataField</span></span>

<span data-ttu-id="241d3-1192">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1192">value</span></span>  

### <a name="return-value---presencedatafield"></a><span data-ttu-id="241d3-1193">戻り値 - presenceDataField</span><span class="sxs-lookup"><span data-stu-id="241d3-1193">Return Value - presenceDataField</span></span>

## <a name="method-presencedatasource"></a><span data-ttu-id="241d3-1194">メソッド presenceDataSource</span><span class="sxs-lookup"><span data-stu-id="241d3-1194">Method presenceDataSource</span></span>

```xpp
public int presenceDataSource([AnyType value])
```

### <a name="parameters---presencedatasource"></a><span data-ttu-id="241d3-1195">パラメーター - presenceDataSource</span><span class="sxs-lookup"><span data-stu-id="241d3-1195">Parameters - presenceDataSource</span></span>

<span data-ttu-id="241d3-1196">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1196">value</span></span>  

### <a name="return-value---presencedatasource"></a><span data-ttu-id="241d3-1197">戻り値 - presenceDataSource</span><span class="sxs-lookup"><span data-stu-id="241d3-1197">Return Value - presenceDataSource</span></span>

## <a name="method-presenceindicatorallowed"></a><span data-ttu-id="241d3-1198">メソッド presenceIndicatorAllowed</span><span class="sxs-lookup"><span data-stu-id="241d3-1198">Method presenceIndicatorAllowed</span></span>

```xpp
public int presenceIndicatorAllowed([int value])
```

### <a name="parameters---presenceindicatorallowed"></a><span data-ttu-id="241d3-1199">パラメーター - presenceIndicatorAllowed</span><span class="sxs-lookup"><span data-stu-id="241d3-1199">Parameters - presenceIndicatorAllowed</span></span>

<span data-ttu-id="241d3-1200">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1200">value</span></span>  

### <a name="return-value---presenceindicatorallowed"></a><span data-ttu-id="241d3-1201">戻り値 - presenceIndicatorAllowed</span><span class="sxs-lookup"><span data-stu-id="241d3-1201">Return Value - presenceIndicatorAllowed</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="241d3-1202">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="241d3-1202">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="241d3-1203">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="241d3-1203">Parameters - previewPartRef</span></span>

<span data-ttu-id="241d3-1204">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1204">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="241d3-1205">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="241d3-1205">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="241d3-1206">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="241d3-1206">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="241d3-1207">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="241d3-1207">Parameters - promptrect</span></span>

<span data-ttu-id="241d3-1208">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1208">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="241d3-1209">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="241d3-1209">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="241d3-1210">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1210">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="241d3-1211">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1211">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="241d3-1212">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1212">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="241d3-1213">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1213">Return Value - replaceOnLookup</span></span>

## <a name="method-resolveambiguousreference"></a><span data-ttu-id="241d3-1214">メソッド resolveAmbiguousReference</span><span class="sxs-lookup"><span data-stu-id="241d3-1214">Method resolveAmbiguousReference</span></span>

```xpp
public str resolveAmbiguousReference()
```

### <a name="return-value---resolveambiguousreference"></a><span data-ttu-id="241d3-1215">戻り値 - resolveAmbiguousReference</span><span class="sxs-lookup"><span data-stu-id="241d3-1215">Return Value - resolveAmbiguousReference</span></span>

## <a name="method-disambiguationlookuptarget"></a><span data-ttu-id="241d3-1216">メソッド disambiguationLookupTarget</span><span class="sxs-lookup"><span data-stu-id="241d3-1216">Method disambiguationLookupTarget</span></span>

```xpp
public FieldBinding disambiguationLookupTarget()
```

### <a name="return-value---disambiguationlookuptarget"></a><span data-ttu-id="241d3-1217">戻り値 - disambiguationLookupTarget</span><span class="sxs-lookup"><span data-stu-id="241d3-1217">Return Value - disambiguationLookupTarget</span></span>

## <a name="method-lookupdisambiguatereference"></a><span data-ttu-id="241d3-1218">メソッド lookupDisambiguateReference</span><span class="sxs-lookup"><span data-stu-id="241d3-1218">Method lookupDisambiguateReference</span></span>

```xpp
public str lookupDisambiguateReference(FieldBinding fieldBinding)
```

### <a name="parameters---lookupdisambiguatereference"></a><span data-ttu-id="241d3-1219">パラメーター - lookupDisambiguateReference</span><span class="sxs-lookup"><span data-stu-id="241d3-1219">Parameters - lookupDisambiguateReference</span></span>

<span data-ttu-id="241d3-1220">fieldBinding</span><span class="sxs-lookup"><span data-stu-id="241d3-1220">fieldBinding</span></span>  

### <a name="return-value---lookupdisambiguatereference"></a><span data-ttu-id="241d3-1221">戻り値 - lookupDisambiguateReference</span><span class="sxs-lookup"><span data-stu-id="241d3-1221">Return Value - lookupDisambiguateReference</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="241d3-1222">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="241d3-1222">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="241d3-1223">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="241d3-1223">Parameters - searchAfterInput</span></span>

<span data-ttu-id="241d3-1224">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1224">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="241d3-1225">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="241d3-1225">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="241d3-1226">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1226">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="241d3-1227">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1227">Parameters - searchMode</span></span>

<span data-ttu-id="241d3-1228">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1228">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="241d3-1229">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1229">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="241d3-1230">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="241d3-1230">Method securityKey</span></span>

<span data-ttu-id="241d3-1231">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1231">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="241d3-1232">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="241d3-1232">Parameters - securityKey</span></span>

<span data-ttu-id="241d3-1233">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1233">value</span></span>  
<span data-ttu-id="241d3-1234">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1234">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="241d3-1235">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="241d3-1235">Return Value - securityKey</span></span>

<span data-ttu-id="241d3-1236">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1236">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="241d3-1237">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="241d3-1237">Method showContextMenu</span></span>

<span data-ttu-id="241d3-1238">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1238">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="241d3-1239">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="241d3-1239">Parameters - showContextMenu</span></span>

<span data-ttu-id="241d3-1240">menuHandle</span><span class="sxs-lookup"><span data-stu-id="241d3-1240">menuHandle</span></span>  
<span data-ttu-id="241d3-1241">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="241d3-1241">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="241d3-1242">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="241d3-1242">Return Value - showContextMenu</span></span>

<span data-ttu-id="241d3-1243">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1243">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="241d3-1244">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="241d3-1244">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="241d3-1245">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="241d3-1245">Parameters - showLabel</span></span>

<span data-ttu-id="241d3-1246">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1246">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="241d3-1247">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="241d3-1247">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="241d3-1248">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="241d3-1248">Method skip</span></span>

<span data-ttu-id="241d3-1249">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1249">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="241d3-1250">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="241d3-1250">Parameters - skip</span></span>

<span data-ttu-id="241d3-1251">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1251">value</span></span>  
<span data-ttu-id="241d3-1252">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1252">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="241d3-1253">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="241d3-1253">Return Value - skip</span></span>

<span data-ttu-id="241d3-1254">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="241d3-1254">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="241d3-1255">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="241d3-1255">Remarks - skip</span></span>

<span data-ttu-id="241d3-1256">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1256">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="241d3-1257">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="241d3-1257">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="241d3-1258">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="241d3-1258">Parameters - sort</span></span>

<span data-ttu-id="241d3-1259">sortDirection</span><span class="sxs-lookup"><span data-stu-id="241d3-1259">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="241d3-1260">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="241d3-1260">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="241d3-1261">メソッド style</span><span class="sxs-lookup"><span data-stu-id="241d3-1261">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="241d3-1262">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="241d3-1262">Parameters - style</span></span>

<span data-ttu-id="241d3-1263">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1263">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="241d3-1264">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="241d3-1264">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="241d3-1265">メソッド text</span><span class="sxs-lookup"><span data-stu-id="241d3-1265">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="241d3-1266">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="241d3-1266">Parameters - text</span></span>

<span data-ttu-id="241d3-1267">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1267">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="241d3-1268">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="241d3-1268">Return Value - text</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="241d3-1269">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="241d3-1269">Method toolTip</span></span>

<span data-ttu-id="241d3-1270">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1270">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="241d3-1271">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="241d3-1271">Return Value - toolTip</span></span>

<span data-ttu-id="241d3-1272">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="241d3-1272">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="241d3-1273">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="241d3-1273">Remarks - toolTip</span></span>

<span data-ttu-id="241d3-1274">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1274">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="241d3-1275">メソッド top</span><span class="sxs-lookup"><span data-stu-id="241d3-1275">Method top</span></span>

<span data-ttu-id="241d3-1276">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1276">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="241d3-1277">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="241d3-1277">Parameters - top</span></span>

<span data-ttu-id="241d3-1278">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1278">value</span></span>  
<span data-ttu-id="241d3-1279">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1279">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="241d3-1280">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1280">mode</span></span>  
<span data-ttu-id="241d3-1281">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1281">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="241d3-1282">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="241d3-1282">Return Value - top</span></span>

<span data-ttu-id="241d3-1283">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="241d3-1283">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="241d3-1284">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1284">Method topMode</span></span>

<span data-ttu-id="241d3-1285">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1285">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="241d3-1286">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1286">Parameters - topMode</span></span>

<span data-ttu-id="241d3-1287">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1287">value</span></span>  
<span data-ttu-id="241d3-1288">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1288">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="241d3-1289">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1289">Return Value - topMode</span></span>

<span data-ttu-id="241d3-1290">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="241d3-1290">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="241d3-1291">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1291">Method topValue</span></span>

<span data-ttu-id="241d3-1292">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1292">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="241d3-1293">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1293">Parameters - topValue</span></span>

<span data-ttu-id="241d3-1294">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1294">value</span></span>  
<span data-ttu-id="241d3-1295">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1295">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="241d3-1296">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1296">Return Value - topValue</span></span>

<span data-ttu-id="241d3-1297">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="241d3-1297">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="241d3-1298">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="241d3-1298">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="241d3-1299">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="241d3-1299">Parameters - type</span></span>

<span data-ttu-id="241d3-1300">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1300">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="241d3-1301">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="241d3-1301">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="241d3-1302">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="241d3-1302">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="241d3-1303">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="241d3-1303">Parameters - underline</span></span>

<span data-ttu-id="241d3-1304">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1304">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="241d3-1305">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="241d3-1305">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="241d3-1306">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="241d3-1306">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="241d3-1307">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="241d3-1307">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="241d3-1308">データ</span><span class="sxs-lookup"><span data-stu-id="241d3-1308">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="241d3-1309">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="241d3-1309">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="241d3-1310">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="241d3-1310">Method userData</span></span>

<span data-ttu-id="241d3-1311">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1311">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="241d3-1312">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="241d3-1312">Parameters - userData</span></span>

<span data-ttu-id="241d3-1313">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1313">value</span></span>  
<span data-ttu-id="241d3-1314">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1314">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="241d3-1315">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="241d3-1315">Return Value - userData</span></span>

<span data-ttu-id="241d3-1316">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="241d3-1316">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="241d3-1317">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="241d3-1317">Method userDataItem</span></span>

<span data-ttu-id="241d3-1318">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1318">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="241d3-1319">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="241d3-1319">Parameters - userDataItem</span></span>

<span data-ttu-id="241d3-1320">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1320">value</span></span>  
<span data-ttu-id="241d3-1321">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1321">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="241d3-1322">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="241d3-1322">Return Value - userDataItem</span></span>

<span data-ttu-id="241d3-1323">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="241d3-1323">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="241d3-1324">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="241d3-1324">Method userDataItems</span></span>

<span data-ttu-id="241d3-1325">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1325">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="241d3-1326">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="241d3-1326">Parameters - userDataItems</span></span>

<span data-ttu-id="241d3-1327">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1327">value</span></span>  
<span data-ttu-id="241d3-1328">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1328">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="241d3-1329">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="241d3-1329">Return Value - userDataItems</span></span>

<span data-ttu-id="241d3-1330">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="241d3-1330">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="241d3-1331">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="241d3-1331">Method userDisable</span></span>

<span data-ttu-id="241d3-1332">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1332">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="241d3-1333">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="241d3-1333">Parameters - userDisable</span></span>

<span data-ttu-id="241d3-1334">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1334">value</span></span>  
<span data-ttu-id="241d3-1335">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1335">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="241d3-1336">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="241d3-1336">Return Value - userDisable</span></span>

<span data-ttu-id="241d3-1337">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1337">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="241d3-1338">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="241d3-1338">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="241d3-1339">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="241d3-1339">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="241d3-1340">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1340">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="241d3-1341">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="241d3-1341">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="241d3-1342">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-1342">Method userHeight</span></span>

<span data-ttu-id="241d3-1343">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1343">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="241d3-1344">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-1344">Parameters - userHeight</span></span>

<span data-ttu-id="241d3-1345">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1345">value</span></span>  
<span data-ttu-id="241d3-1346">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1346">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="241d3-1347">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="241d3-1347">Return Value - userHeight</span></span>

<span data-ttu-id="241d3-1348">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="241d3-1348">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="241d3-1349">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="241d3-1349">Method userHide</span></span>

<span data-ttu-id="241d3-1350">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1350">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="241d3-1351">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="241d3-1351">Parameters - userHide</span></span>

<span data-ttu-id="241d3-1352">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1352">value</span></span>  
<span data-ttu-id="241d3-1353">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1353">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="241d3-1354">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="241d3-1354">Return Value - userHide</span></span>

<span data-ttu-id="241d3-1355">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1355">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="241d3-1356">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="241d3-1356">Remarks - userHide</span></span>

<span data-ttu-id="241d3-1357">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1357">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="241d3-1358">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1358">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="241d3-1359">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1359">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="241d3-1360">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="241d3-1360">Method userOrgContainer</span></span>

<span data-ttu-id="241d3-1361">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1361">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="241d3-1362">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="241d3-1362">Parameters - userOrgContainer</span></span>

<span data-ttu-id="241d3-1363">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1363">value</span></span>  
<span data-ttu-id="241d3-1364">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1364">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="241d3-1365">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="241d3-1365">Return Value - userOrgContainer</span></span>

<span data-ttu-id="241d3-1366">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="241d3-1366">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="241d3-1367">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="241d3-1367">Method userOrgSibling</span></span>

<span data-ttu-id="241d3-1368">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1368">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="241d3-1369">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="241d3-1369">Parameters - userOrgSibling</span></span>

<span data-ttu-id="241d3-1370">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1370">value</span></span>  
<span data-ttu-id="241d3-1371">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1371">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="241d3-1372">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="241d3-1372">Return Value - userOrgSibling</span></span>

<span data-ttu-id="241d3-1373">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="241d3-1373">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="241d3-1374">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="241d3-1374">Method userPromptText</span></span>

<span data-ttu-id="241d3-1375">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1375">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="241d3-1376">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="241d3-1376">Parameters - userPromptText</span></span>

<span data-ttu-id="241d3-1377">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1377">value</span></span>  
<span data-ttu-id="241d3-1378">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1378">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="241d3-1379">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="241d3-1379">Return Value - userPromptText</span></span>

<span data-ttu-id="241d3-1380">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="241d3-1380">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="241d3-1381">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="241d3-1381">Method userSecurityLevel</span></span>

<span data-ttu-id="241d3-1382">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1382">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="241d3-1383">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="241d3-1383">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="241d3-1384">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1384">value</span></span>  
<span data-ttu-id="241d3-1385">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1385">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="241d3-1386">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="241d3-1386">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="241d3-1387">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="241d3-1387">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="241d3-1388">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="241d3-1388">Method userSkip</span></span>

<span data-ttu-id="241d3-1389">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1389">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="241d3-1390">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="241d3-1390">Parameters - userSkip</span></span>

<span data-ttu-id="241d3-1391">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1391">value</span></span>  
<span data-ttu-id="241d3-1392">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1392">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="241d3-1393">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1393">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="241d3-1394">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="241d3-1394">Return Value - userSkip</span></span>

<span data-ttu-id="241d3-1395">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="241d3-1395">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="241d3-1396">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="241d3-1396">Method userWidth</span></span>

<span data-ttu-id="241d3-1397">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1397">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="241d3-1398">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="241d3-1398">Parameters - userWidth</span></span>

<span data-ttu-id="241d3-1399">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1399">value</span></span>  
<span data-ttu-id="241d3-1400">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1400">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="241d3-1401">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="241d3-1401">Return Value - userWidth</span></span>

<span data-ttu-id="241d3-1402">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1402">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="241d3-1403">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="241d3-1403">Remarks - userWidth</span></span>

<span data-ttu-id="241d3-1404">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1404">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="241d3-1405">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="241d3-1405">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="241d3-1406">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1406">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="241d3-1407">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="241d3-1407">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="241d3-1408">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="241d3-1408">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="241d3-1409">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="241d3-1409">Method verticalSpacing</span></span>

<span data-ttu-id="241d3-1410">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1410">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="241d3-1411">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="241d3-1411">Parameters - verticalSpacing</span></span>

<span data-ttu-id="241d3-1412">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1412">value</span></span>  
<span data-ttu-id="241d3-1413">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1413">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="241d3-1414">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1414">mode</span></span>  
<span data-ttu-id="241d3-1415">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1415">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="241d3-1416">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="241d3-1416">Return Value - verticalSpacing</span></span>

<span data-ttu-id="241d3-1417">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="241d3-1417">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="241d3-1418">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1418">Method verticalSpacingMode</span></span>

<span data-ttu-id="241d3-1419">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1419">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="241d3-1420">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1420">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="241d3-1421">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1421">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="241d3-1422">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1422">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="241d3-1423">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="241d3-1423">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="241d3-1424">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1424">Method verticalSpacingValue</span></span>

<span data-ttu-id="241d3-1425">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1425">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="241d3-1426">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1426">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="241d3-1427">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1427">value</span></span>  
<span data-ttu-id="241d3-1428">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="241d3-1428">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="241d3-1429">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1429">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="241d3-1430">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="241d3-1430">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="241d3-1431">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1431">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="241d3-1432">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1432">Parameters - viewEditMode</span></span>

<span data-ttu-id="241d3-1433">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1433">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="241d3-1434">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1434">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="241d3-1435">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="241d3-1435">Method visible</span></span>

<span data-ttu-id="241d3-1436">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1436">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="241d3-1437">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="241d3-1437">Parameters - visible</span></span>

<span data-ttu-id="241d3-1438">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1438">value</span></span>  
<span data-ttu-id="241d3-1439">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1439">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="241d3-1440">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="241d3-1440">Return Value - visible</span></span>

<span data-ttu-id="241d3-1441">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="241d3-1441">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="241d3-1442">メソッド width</span><span class="sxs-lookup"><span data-stu-id="241d3-1442">Method width</span></span>

<span data-ttu-id="241d3-1443">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1443">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="241d3-1444">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="241d3-1444">Parameters - width</span></span>

<span data-ttu-id="241d3-1445">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1445">value</span></span>  

<!-- -->

<span data-ttu-id="241d3-1446">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1446">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="241d3-1447">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="241d3-1447">Return Value - width</span></span>

<span data-ttu-id="241d3-1448">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="241d3-1448">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="241d3-1449">備考 - width</span><span class="sxs-lookup"><span data-stu-id="241d3-1449">Remarks - width</span></span>

<span data-ttu-id="241d3-1450">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1450">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="241d3-1451">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1451">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="241d3-1452">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1452">Mode</span></span>           | <span data-ttu-id="241d3-1453">幅計算</span><span class="sxs-lookup"><span data-stu-id="241d3-1453">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d3-1454">-1 正確</span><span class="sxs-lookup"><span data-stu-id="241d3-1454">-1 Exact</span></span>       | <span data-ttu-id="241d3-1455">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1455">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="241d3-1456">0 自動</span><span class="sxs-lookup"><span data-stu-id="241d3-1456">0 Auto</span></span>         | <span data-ttu-id="241d3-1457">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1457">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="241d3-1458">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="241d3-1458">1 Column width</span></span> | <span data-ttu-id="241d3-1459">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="241d3-1459">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="241d3-1460">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1460">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="241d3-1461">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1461">Method widthMode</span></span>

<span data-ttu-id="241d3-1462">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1462">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="241d3-1463">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1463">Parameters - widthMode</span></span>

<span data-ttu-id="241d3-1464">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1464">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="241d3-1465">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1465">Return Value - widthMode</span></span>

<span data-ttu-id="241d3-1466">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1466">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="241d3-1467">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1467">Remarks - widthMode</span></span>

<span data-ttu-id="241d3-1468">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1468">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="241d3-1469">モード</span><span class="sxs-lookup"><span data-stu-id="241d3-1469">Mode</span></span>         | <span data-ttu-id="241d3-1470">幅計算</span><span class="sxs-lookup"><span data-stu-id="241d3-1470">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d3-1471">正確</span><span class="sxs-lookup"><span data-stu-id="241d3-1471">Exact</span></span>        | <span data-ttu-id="241d3-1472">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1472">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="241d3-1473">自動</span><span class="sxs-lookup"><span data-stu-id="241d3-1473">Auto</span></span>         | <span data-ttu-id="241d3-1474">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1474">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="241d3-1475">列の幅</span><span class="sxs-lookup"><span data-stu-id="241d3-1475">Column width</span></span> | <span data-ttu-id="241d3-1476">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="241d3-1476">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="241d3-1477">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="241d3-1477">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="241d3-1478">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1478">Method widthValue</span></span>

<span data-ttu-id="241d3-1479">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1479">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="241d3-1480">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1480">Parameters - widthValue</span></span>

<span data-ttu-id="241d3-1481">値</span><span class="sxs-lookup"><span data-stu-id="241d3-1481">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="241d3-1482">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1482">Return Value - widthValue</span></span>

<span data-ttu-id="241d3-1483">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="241d3-1483">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="241d3-1484">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="241d3-1484">Remarks - widthValue</span></span>

<span data-ttu-id="241d3-1485">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1485">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-presencerefresh"></a><span data-ttu-id="241d3-1486">メソッド presenceRefresh</span><span class="sxs-lookup"><span data-stu-id="241d3-1486">Method presenceRefresh</span></span>

```xpp
public void presenceRefresh()
```

## <a name="method-onlookup"></a><span data-ttu-id="241d3-1487">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1487">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="241d3-1488">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1488">Parameters - OnLookup</span></span>

<span data-ttu-id="241d3-1489">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1489">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1490">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1490">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="241d3-1491">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="241d3-1491">Method lostFocus</span></span>

<span data-ttu-id="241d3-1492">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1492">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="241d3-1493">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="241d3-1493">Method mouseEnter</span></span>

<span data-ttu-id="241d3-1494">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1494">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="241d3-1495">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="241d3-1495">Parameters - mouseEnter</span></span>

<span data-ttu-id="241d3-1496">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1496">x</span></span>  
<span data-ttu-id="241d3-1497">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1497">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1498">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1498">y</span></span>  
<span data-ttu-id="241d3-1499">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1499">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1500">ボタン</span><span class="sxs-lookup"><span data-stu-id="241d3-1500">button</span></span>  
<span data-ttu-id="241d3-1501">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1501">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1502">Ctrl</span><span class="sxs-lookup"><span data-stu-id="241d3-1502">Ctrl</span></span>  
<span data-ttu-id="241d3-1503">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1503">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="241d3-1504">シフト</span><span class="sxs-lookup"><span data-stu-id="241d3-1504">Shift</span></span>  
<span data-ttu-id="241d3-1505">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1505">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-performtypelookup"></a><span data-ttu-id="241d3-1506">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1506">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="241d3-1507">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1507">Parameters - performTypeLookup</span></span>

<span data-ttu-id="241d3-1508">userType</span><span class="sxs-lookup"><span data-stu-id="241d3-1508">userType</span></span>  

<!-- -->

<span data-ttu-id="241d3-1509">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="241d3-1509">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="241d3-1510">会社</span><span class="sxs-lookup"><span data-stu-id="241d3-1510">company</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="241d3-1511">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="241d3-1511">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="241d3-1512">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="241d3-1512">Parameters - OnLeaving</span></span>

<span data-ttu-id="241d3-1513">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1513">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1514">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1514">e</span></span>  

## <a name="method-undo"></a><span data-ttu-id="241d3-1515">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="241d3-1515">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="241d3-1516">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-1516">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="241d3-1517">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="241d3-1517">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="241d3-1518">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="241d3-1518">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="241d3-1519">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="241d3-1519">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="241d3-1520">overrideObject</span><span class="sxs-lookup"><span data-stu-id="241d3-1520">overrideObject</span></span>  

## <a name="method-context"></a><span data-ttu-id="241d3-1521">メソッド context</span><span class="sxs-lookup"><span data-stu-id="241d3-1521">Method context</span></span>

<span data-ttu-id="241d3-1522">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1522">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="241d3-1523">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="241d3-1523">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="241d3-1524">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="241d3-1524">Parameters - OnGotFocus</span></span>

<span data-ttu-id="241d3-1525">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1525">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1526">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1526">e</span></span>  

## <a name="method-setselection"></a><span data-ttu-id="241d3-1527">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="241d3-1527">Method setSelection</span></span>

```xpp
public void setSelection(int charIndexFrom, int charIndexTo)
```

### <a name="parameters---setselection"></a><span data-ttu-id="241d3-1528">パラメーター - setSelection</span><span class="sxs-lookup"><span data-stu-id="241d3-1528">Parameters - setSelection</span></span>

<span data-ttu-id="241d3-1529">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="241d3-1529">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="241d3-1530">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="241d3-1530">charIndexTo</span></span>  

## <a name="method-scrollcursor"></a><span data-ttu-id="241d3-1531">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="241d3-1531">Method scrollCursor</span></span>

```xpp
public void scrollCursor()
```

## <a name="method-enter"></a><span data-ttu-id="241d3-1532">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="241d3-1532">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-inputsearch"></a><span data-ttu-id="241d3-1533">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="241d3-1533">Method inputSearch</span></span>

<span data-ttu-id="241d3-1534">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1534">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="241d3-1535">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="241d3-1535">Parameters - inputSearch</span></span>

<span data-ttu-id="241d3-1536">searchStr</span><span class="sxs-lookup"><span data-stu-id="241d3-1536">searchStr</span></span>  
<span data-ttu-id="241d3-1537">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="241d3-1537">The string value to use to filter data; optional.</span></span>

## <a name="method-performdblookup"></a><span data-ttu-id="241d3-1538">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1538">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="241d3-1539">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1539">Parameters - performDBLookup</span></span>

<span data-ttu-id="241d3-1540">fieldId</span><span class="sxs-lookup"><span data-stu-id="241d3-1540">fieldId</span></span>  

<!-- -->

<span data-ttu-id="241d3-1541">tableId</span><span class="sxs-lookup"><span data-stu-id="241d3-1541">tableId</span></span>  

<!-- -->

<span data-ttu-id="241d3-1542">会社</span><span class="sxs-lookup"><span data-stu-id="241d3-1542">company</span></span>  

## <a name="method-filter"></a><span data-ttu-id="241d3-1543">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="241d3-1543">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="241d3-1544">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="241d3-1544">Parameters - filter</span></span>

<span data-ttu-id="241d3-1545">filterStr</span><span class="sxs-lookup"><span data-stu-id="241d3-1545">filterStr</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="241d3-1546">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="241d3-1546">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="241d3-1547">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="241d3-1547">Parameters - OnModified</span></span>

<span data-ttu-id="241d3-1548">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1548">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1549">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1549">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="241d3-1550">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="241d3-1550">Method dropEx</span></span>

<span data-ttu-id="241d3-1551">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1551">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="241d3-1552">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="241d3-1552">Parameters - dropEx</span></span>

<span data-ttu-id="241d3-1553">dragSource</span><span class="sxs-lookup"><span data-stu-id="241d3-1553">dragSource</span></span>  
<span data-ttu-id="241d3-1554">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1554">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-1555">dragMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1555">dragMode</span></span>  
<span data-ttu-id="241d3-1556">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1556">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-1557">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1557">x</span></span>  
<span data-ttu-id="241d3-1558">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1558">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-1559">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1559">y</span></span>  
<span data-ttu-id="241d3-1560">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1560">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="241d3-1561">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="241d3-1561">Method mouseLeave</span></span>

<span data-ttu-id="241d3-1562">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1562">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="241d3-1563">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="241d3-1563">Method displayControl</span></span>

<span data-ttu-id="241d3-1564">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1564">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-copy"></a><span data-ttu-id="241d3-1565">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="241d3-1565">Method copy</span></span>

<span data-ttu-id="241d3-1566">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="241d3-1566">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-gotfocus"></a><span data-ttu-id="241d3-1567">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="241d3-1567">Method gotFocus</span></span>

<span data-ttu-id="241d3-1568">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1568">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-dragleave"></a><span data-ttu-id="241d3-1569">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="241d3-1569">Method dragLeave</span></span>

<span data-ttu-id="241d3-1570">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1570">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-cut"></a><span data-ttu-id="241d3-1571">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="241d3-1571">Method cut</span></span>

<span data-ttu-id="241d3-1572">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="241d3-1572">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-paste"></a><span data-ttu-id="241d3-1573">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="241d3-1573">Method paste</span></span>

<span data-ttu-id="241d3-1574">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1574">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-onvalidating"></a><span data-ttu-id="241d3-1575">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="241d3-1575">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="241d3-1576">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="241d3-1576">Parameters - OnValidating</span></span>

<span data-ttu-id="241d3-1577">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1577">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1578">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1578">e</span></span>  

## <a name="method-setcursorpos"></a><span data-ttu-id="241d3-1579">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="241d3-1579">Method setCursorPos</span></span>

```xpp
public void setCursorPos(int x, int y)
```

### <a name="parameters---setcursorpos"></a><span data-ttu-id="241d3-1580">パラメーター - setCursorPos</span><span class="sxs-lookup"><span data-stu-id="241d3-1580">Parameters - setCursorPos</span></span>

<span data-ttu-id="241d3-1581">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1581">x</span></span>  

<!-- -->

<span data-ttu-id="241d3-1582">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1582">y</span></span>  

## <a name="method-performformlookup"></a><span data-ttu-id="241d3-1583">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1583">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="241d3-1584">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1584">Parameters - performFormLookup</span></span>

<span data-ttu-id="241d3-1585">フォーム</span><span class="sxs-lookup"><span data-stu-id="241d3-1585">form</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="241d3-1586">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="241d3-1586">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="241d3-1587">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="241d3-1587">Parameters - OnLostFocus</span></span>

<span data-ttu-id="241d3-1588">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1588">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1589">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1589">e</span></span>  

## <a name="method-linescroll"></a><span data-ttu-id="241d3-1590">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="241d3-1590">Method lineScroll</span></span>

```xpp
public void lineScroll(int dx, int dy)
```

### <a name="parameters---linescroll"></a><span data-ttu-id="241d3-1591">パラメーター - lineScroll</span><span class="sxs-lookup"><span data-stu-id="241d3-1591">Parameters - lineScroll</span></span>

<span data-ttu-id="241d3-1592">dx</span><span class="sxs-lookup"><span data-stu-id="241d3-1592">dx</span></span>  

<!-- -->

<span data-ttu-id="241d3-1593">dy</span><span class="sxs-lookup"><span data-stu-id="241d3-1593">dy</span></span>  

## <a name="method-onenter"></a><span data-ttu-id="241d3-1594">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="241d3-1594">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="241d3-1595">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="241d3-1595">Parameters - OnEnter</span></span>

<span data-ttu-id="241d3-1596">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1596">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1597">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1597">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="241d3-1598">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="241d3-1598">Method prefColumnSize</span></span>

<span data-ttu-id="241d3-1599">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1599">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="241d3-1600">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="241d3-1600">Parameters - prefColumnSize</span></span>

<span data-ttu-id="241d3-1601">width</span><span class="sxs-lookup"><span data-stu-id="241d3-1601">width</span></span>  
<span data-ttu-id="241d3-1602">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="241d3-1602">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="241d3-1603">height</span><span class="sxs-lookup"><span data-stu-id="241d3-1603">height</span></span>  
<span data-ttu-id="241d3-1604">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="241d3-1604">The preferred height of the control.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="241d3-1605">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="241d3-1605">Method resetUserSetting</span></span>

<span data-ttu-id="241d3-1606">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="241d3-1606">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-textchange"></a><span data-ttu-id="241d3-1607">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="241d3-1607">Method textChange</span></span>

```xpp
public void textChange()
```

## <a name="method-jumpref"></a><span data-ttu-id="241d3-1608">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="241d3-1608">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-lookup"></a><span data-ttu-id="241d3-1609">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="241d3-1609">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-pastetext"></a><span data-ttu-id="241d3-1610">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="241d3-1610">Method pasteText</span></span>

```xpp
public void pasteText(str pasteStr, [boolean InsertSel])
```

### <a name="parameters---pastetext"></a><span data-ttu-id="241d3-1611">パラメーター - pasteText</span><span class="sxs-lookup"><span data-stu-id="241d3-1611">Parameters - pasteText</span></span>

<span data-ttu-id="241d3-1612">pasteStr</span><span class="sxs-lookup"><span data-stu-id="241d3-1612">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="241d3-1613">InsertSel</span><span class="sxs-lookup"><span data-stu-id="241d3-1613">InsertSel</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="241d3-1614">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="241d3-1614">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="241d3-1615">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="241d3-1615">Parameters - OnValidated</span></span>

<span data-ttu-id="241d3-1616">sender</span><span class="sxs-lookup"><span data-stu-id="241d3-1616">sender</span></span>  

<!-- -->

<span data-ttu-id="241d3-1617">e</span><span class="sxs-lookup"><span data-stu-id="241d3-1617">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="241d3-1618">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="241d3-1618">Method drop</span></span>

<span data-ttu-id="241d3-1619">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1619">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="241d3-1620">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="241d3-1620">Parameters - drop</span></span>

<span data-ttu-id="241d3-1621">dragSource</span><span class="sxs-lookup"><span data-stu-id="241d3-1621">dragSource</span></span>  
<span data-ttu-id="241d3-1622">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1622">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-1623">dragMode</span><span class="sxs-lookup"><span data-stu-id="241d3-1623">dragMode</span></span>  
<span data-ttu-id="241d3-1624">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1624">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-1625">x</span><span class="sxs-lookup"><span data-stu-id="241d3-1625">x</span></span>  
<span data-ttu-id="241d3-1626">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1626">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="241d3-1627">y</span><span class="sxs-lookup"><span data-stu-id="241d3-1627">y</span></span>  
<span data-ttu-id="241d3-1628">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="241d3-1628">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="241d3-1629">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="241d3-1629">Method setFocus</span></span>

<span data-ttu-id="241d3-1630">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1630">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-enddrag"></a><span data-ttu-id="241d3-1631">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="241d3-1631">Method endDrag</span></span>

<span data-ttu-id="241d3-1632">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="241d3-1632">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="241d3-1633">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="241d3-1633">Remarks - endDrag</span></span>

<span data-ttu-id="241d3-1634">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="241d3-1634">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="241d3-1635">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="241d3-1635">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>


