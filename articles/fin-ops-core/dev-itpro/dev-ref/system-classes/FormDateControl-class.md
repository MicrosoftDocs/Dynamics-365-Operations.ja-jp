---
title: FormDateControl クラス
description: このトピックでは、FormDateControl クラスについて説明します。
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
ms.openlocfilehash: c065a68d77eb9325e002ee080b424a231d065145
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502629"
---
# <a name="class-formdatecontrol"></a><span data-ttu-id="4e684-103">クラス FormDateControl</span><span class="sxs-lookup"><span data-stu-id="4e684-103">Class FormDateControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormDateControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="4e684-104">備考</span><span class="sxs-lookup"><span data-stu-id="4e684-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="4e684-105">例</span><span class="sxs-lookup"><span data-stu-id="4e684-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="4e684-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="4e684-106">Methods</span></span>

| <span data-ttu-id="4e684-107">方法</span><span class="sxs-lookup"><span data-stu-id="4e684-107">Method</span></span>                                                                                                      | <span data-ttu-id="4e684-108">説明</span><span class="sxs-lookup"><span data-stu-id="4e684-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e684-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="4e684-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="4e684-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="4e684-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="4e684-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="4e684-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="4e684-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="4e684-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="4e684-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="4e684-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="4e684-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="4e684-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="4e684-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="4e684-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="4e684-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="4e684-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="4e684-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="4e684-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-126">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="4e684-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="4e684-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="4e684-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="4e684-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="4e684-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="4e684-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="4e684-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="4e684-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-133">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="4e684-134">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="4e684-134">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-135">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-135">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="4e684-136">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-136">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="4e684-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-137">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="4e684-138">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-138">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="4e684-139">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="4e684-139">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="4e684-140">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-140">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="4e684-141">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-141">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="4e684-142">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-142">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="4e684-143">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-143">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-144">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-144">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-145">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="4e684-145">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-146">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="4e684-146">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-147">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-147">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-148">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-148">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="4e684-149">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-149">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="4e684-150">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-150">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="4e684-151">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-151">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="4e684-152">public int dateDay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-152">public int dateDay(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="4e684-153">public int dateFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-153">public int dateFormat(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-154">public int dateMonth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-154">public int dateMonth(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-155">public int dateSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-155">public int dateSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="4e684-156">public Date dateValue(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-156">public Date dateValue(\[Date value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="4e684-157">public int dateYear(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-157">public int dateYear(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="4e684-158">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-158">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-159">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-159">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-160">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-160">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-161">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-161">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-162">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-162">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-163">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-163">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-164">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-164">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-165">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-165">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="4e684-166">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-166">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="4e684-167">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-167">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="4e684-168">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-168">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="4e684-169">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="4e684-169">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="4e684-170">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-170">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="4e684-171">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="4e684-171">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="4e684-172">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-172">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="4e684-173">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="4e684-173">public str dragText()</span></span>                                                                                       | <span data-ttu-id="4e684-174">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-174">Retrieves the text that id displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="4e684-175">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-175">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="4e684-176">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-176">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="4e684-177">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-177">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-178">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-178">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-179">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-179">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="4e684-180">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-180">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="4e684-181">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-181">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="4e684-182">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-182">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="4e684-183">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-183">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="4e684-184">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-184">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="4e684-185">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="4e684-185">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="4e684-186">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="4e684-186">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-187">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="4e684-187">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="4e684-188">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="4e684-188">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="4e684-189">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="4e684-189">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="4e684-190">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="4e684-190">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="4e684-191">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-191">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="4e684-192">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="4e684-192">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="4e684-193">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-193">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="4e684-194">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-194">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="4e684-195">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-195">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="4e684-196">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-196">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="4e684-197">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-197">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="4e684-198">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-198">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="4e684-199">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-199">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="4e684-200">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="4e684-200">public str helpField()</span></span>                                                                                      | <span data-ttu-id="4e684-201">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-201">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="4e684-202">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-202">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="4e684-203">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-203">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="4e684-204">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-204">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="4e684-205">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-205">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="4e684-206">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="4e684-206">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="4e684-207">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-207">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="4e684-208">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-208">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="4e684-209">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="4e684-209">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-210">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="4e684-210">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="4e684-211">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-211">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="4e684-212">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="4e684-212">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="4e684-213">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-213">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="4e684-214">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="4e684-214">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="4e684-215">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-215">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="4e684-216">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="4e684-216">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-217">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-217">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-218">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-218">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="4e684-219">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-219">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="4e684-220">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-220">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-221">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-221">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-222">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-222">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-223">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-223">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-224">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-224">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="4e684-225">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-225">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="4e684-226">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-226">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-227">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-227">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="4e684-228">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-228">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="4e684-229">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-229">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-230">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-230">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="4e684-231">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-231">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-232">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-232">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-233">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-233">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="4e684-234">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-234">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="4e684-235">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-235">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-236">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-236">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="4e684-237">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-237">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-238">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-238">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="4e684-239">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="4e684-239">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-240">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-240">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="4e684-241">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-241">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="4e684-242">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-242">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="4e684-243">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-243">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="4e684-244">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-244">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="4e684-245">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-245">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="4e684-246">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-246">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-247">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-247">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-248">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-248">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-249">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="4e684-249">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-250">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="4e684-250">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="4e684-251">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="4e684-251">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="4e684-252">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-252">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-253">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-253">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-254">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-254">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="4e684-255">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="4e684-255">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="4e684-256">public str maxDateLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-256">public str maxDateLabel(\[str value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-257">public str maxDateLabelText()</span><span class="sxs-lookup"><span data-stu-id="4e684-257">public str maxDateLabelText()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="4e684-258">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="4e684-258">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="4e684-259">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-259">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="4e684-260">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-260">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="4e684-261">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-261">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="4e684-262">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-262">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="4e684-263">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-263">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="4e684-264">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-264">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="4e684-265">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-265">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="4e684-266">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-266">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="4e684-267">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-267">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="4e684-268">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-268">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="4e684-269">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-269">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-270">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="4e684-270">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="4e684-271">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="4e684-271">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="4e684-272">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-272">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="4e684-273">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="4e684-273">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-274">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-274">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-275">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-275">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-276">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-276">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="4e684-277">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-277">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-278">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-278">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-279">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-279">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="4e684-280">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-280">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="4e684-281">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="4e684-281">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="4e684-282">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-282">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="4e684-283">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-283">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-284">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-284">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="4e684-285">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-285">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="4e684-286">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="4e684-286">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-287">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-287">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="4e684-288">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="4e684-288">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="4e684-289">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-289">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="4e684-290">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-290">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="4e684-291">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-291">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="4e684-292">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-292">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="4e684-293">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-293">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="4e684-294">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-294">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="4e684-295">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-295">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="4e684-296">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-296">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="4e684-297">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-297">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="4e684-298">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-298">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="4e684-299">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="4e684-299">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-300">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-300">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="4e684-301">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-301">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="4e684-302">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-302">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="4e684-303">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-303">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="4e684-304">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-304">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="4e684-305">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-305">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="4e684-306">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-306">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="4e684-307">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-307">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="4e684-308">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-308">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-309">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-309">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="4e684-310">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-310">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="4e684-311">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-311">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="4e684-312">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-312">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="4e684-313">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-313">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="4e684-314">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-314">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="4e684-315">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-315">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="4e684-316">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-316">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="4e684-317">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-317">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="4e684-318">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-318">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="4e684-319">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-319">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="4e684-320">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-320">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="4e684-321">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-321">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="4e684-322">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-322">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="4e684-323">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-323">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="4e684-324">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-324">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="4e684-325">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="4e684-325">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="4e684-326">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-326">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="4e684-327">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-327">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="4e684-328">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-328">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="4e684-329">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-329">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="4e684-330">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-330">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="4e684-331">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-331">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="4e684-332">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-332">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-333">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-333">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="4e684-334">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-334">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="4e684-335">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4e684-335">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="4e684-336">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-336">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="4e684-337">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-337">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="4e684-338">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-338">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="4e684-339">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4e684-339">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="4e684-340">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-340">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="4e684-341">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="4e684-341">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="4e684-342">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-342">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="4e684-343">public void cut()</span><span class="sxs-lookup"><span data-stu-id="4e684-343">public void cut()</span></span>                                                                                           | <span data-ttu-id="4e684-344">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="4e684-344">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="4e684-345">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-345">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-346">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="4e684-346">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-347">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="4e684-347">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="4e684-348">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-348">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="4e684-349">public void copy()</span><span class="sxs-lookup"><span data-stu-id="4e684-349">public void copy()</span></span>                                                                                          | <span data-ttu-id="4e684-350">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="4e684-350">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="4e684-351">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="4e684-351">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="4e684-352">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-352">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="4e684-353">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-353">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="4e684-354">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="4e684-354">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-355">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="4e684-355">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-356">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="4e684-356">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-357">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="4e684-357">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-358">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-358">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="4e684-359">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="4e684-359">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-360">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="4e684-360">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="4e684-361">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-361">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="4e684-362">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="4e684-362">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="4e684-363">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-363">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-364">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-364">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="4e684-365">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="4e684-365">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="4e684-366">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="4e684-366">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="4e684-367">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-367">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="4e684-368">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-368">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="4e684-369">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="4e684-369">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="4e684-370">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-370">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="4e684-371">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="4e684-371">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="4e684-372">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="4e684-372">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="4e684-373">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="4e684-373">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="4e684-374">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-374">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="4e684-375">public void undo()</span><span class="sxs-lookup"><span data-stu-id="4e684-375">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="4e684-376">public void context()</span><span class="sxs-lookup"><span data-stu-id="4e684-376">public void context()</span></span>                                                                                       | <span data-ttu-id="4e684-377">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-377">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="4e684-378">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="4e684-378">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="4e684-379">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="4e684-379">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="4e684-380">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-380">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-381">public void paste()</span><span class="sxs-lookup"><span data-stu-id="4e684-381">public void paste()</span></span>                                                                                         | <span data-ttu-id="4e684-382">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4e684-382">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="4e684-383">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="4e684-383">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="4e684-384">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="4e684-384">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="4e684-385">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-385">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="4e684-386">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="4e684-386">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="4e684-387">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-387">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="4e684-388">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="4e684-388">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="4e684-389">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-389">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="4e684-390">public void enter()</span><span class="sxs-lookup"><span data-stu-id="4e684-390">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="4e684-391">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="4e684-391">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="4e684-392">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="4e684-392">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="4e684-393">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="4e684-393">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="4e684-394">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="4e684-394">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="4e684-395">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="4e684-395">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="4e684-396">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="4e684-396">public void displayControl()</span></span>                                                                                | <span data-ttu-id="4e684-397">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-397">Displays the control.</span></span>                                                                                                                                                   |

## <a name="method-aligncontrol"></a><span data-ttu-id="4e684-398">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="4e684-398">Method alignControl</span></span>

<span data-ttu-id="4e684-399">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-399">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="4e684-400">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="4e684-400">Parameters - alignControl</span></span>

<span data-ttu-id="4e684-401">値</span><span class="sxs-lookup"><span data-stu-id="4e684-401">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="4e684-402">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="4e684-402">Return Value - alignControl</span></span>

<span data-ttu-id="4e684-403">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="4e684-403">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="4e684-404">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="4e684-404">Remarks - alignControl</span></span>

<span data-ttu-id="4e684-405">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-405">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="4e684-406">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="4e684-406">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="4e684-407">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="4e684-407">Parameters - alignment</span></span>

<span data-ttu-id="4e684-408">値</span><span class="sxs-lookup"><span data-stu-id="4e684-408">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="4e684-409">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="4e684-409">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="4e684-410">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="4e684-410">Method allowEdit</span></span>

<span data-ttu-id="4e684-411">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-411">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="4e684-412">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="4e684-412">Parameters - allowEdit</span></span>

<span data-ttu-id="4e684-413">値</span><span class="sxs-lookup"><span data-stu-id="4e684-413">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="4e684-414">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="4e684-414">Return Value - allowEdit</span></span>

<span data-ttu-id="4e684-415">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-415">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="4e684-416">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="4e684-416">Remarks - allowEdit</span></span>

<span data-ttu-id="4e684-417">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="4e684-417">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="4e684-418">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="4e684-418">Method allowSysSetup</span></span>

<span data-ttu-id="4e684-419">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-419">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="4e684-420">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="4e684-420">Return Value - allowSysSetup</span></span>

<span data-ttu-id="4e684-421">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-421">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="4e684-422">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-422">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="4e684-423">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-423">Parameters - arrayIndex</span></span>

<span data-ttu-id="4e684-424">値</span><span class="sxs-lookup"><span data-stu-id="4e684-424">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="4e684-425">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-425">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="4e684-426">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4e684-426">Method autoDeclaration</span></span>

<span data-ttu-id="4e684-427">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-427">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="4e684-428">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4e684-428">Parameters - autoDeclaration</span></span>

<span data-ttu-id="4e684-429">値</span><span class="sxs-lookup"><span data-stu-id="4e684-429">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="4e684-430">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4e684-430">Return Value - autoDeclaration</span></span>

<span data-ttu-id="4e684-431">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-431">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="4e684-432">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4e684-432">Remarks - autoDeclaration</span></span>

<span data-ttu-id="4e684-433">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="4e684-433">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="4e684-434">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-434">Method backgroundColor</span></span>

<span data-ttu-id="4e684-435">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-435">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="4e684-436">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-436">Parameters - backgroundColor</span></span>

<span data-ttu-id="4e684-437">値</span><span class="sxs-lookup"><span data-stu-id="4e684-437">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="4e684-438">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-438">Return Value - backgroundColor</span></span>

<span data-ttu-id="4e684-439">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="4e684-439">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="4e684-440">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-440">Remarks - backgroundColor</span></span>

<span data-ttu-id="4e684-441">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e684-441">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="4e684-442">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4e684-442">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="4e684-443">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4e684-443">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="4e684-444">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4e684-444">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="4e684-445">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4e684-445">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="4e684-446">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="4e684-446">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="4e684-447">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="4e684-447">Method backStyle</span></span>

<span data-ttu-id="4e684-448">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-448">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="4e684-449">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="4e684-449">Parameters - backStyle</span></span>

<span data-ttu-id="4e684-450">値</span><span class="sxs-lookup"><span data-stu-id="4e684-450">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="4e684-451">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="4e684-451">Return Value - backStyle</span></span>

<span data-ttu-id="4e684-452">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="4e684-452">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="4e684-453">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="4e684-453">Method beginDrag</span></span>

<span data-ttu-id="4e684-454">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-454">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="4e684-455">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="4e684-455">Parameters - beginDrag</span></span>

<span data-ttu-id="4e684-456">x</span><span class="sxs-lookup"><span data-stu-id="4e684-456">x</span></span>  
<span data-ttu-id="4e684-457">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-457">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="4e684-458">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="4e684-458">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="4e684-459">y</span><span class="sxs-lookup"><span data-stu-id="4e684-459">y</span></span>  
<span data-ttu-id="4e684-460">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-460">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="4e684-461">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="4e684-461">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="4e684-462">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="4e684-462">Return Value - beginDrag</span></span>

<span data-ttu-id="4e684-463">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="4e684-463">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="4e684-464">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="4e684-464">Remarks - beginDrag</span></span>

<span data-ttu-id="4e684-465">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="4e684-465">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="4e684-466">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="4e684-466">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="4e684-467">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="4e684-467">Method bold</span></span>

<span data-ttu-id="4e684-468">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-468">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="4e684-469">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="4e684-469">Parameters - bold</span></span>

<span data-ttu-id="4e684-470">値</span><span class="sxs-lookup"><span data-stu-id="4e684-470">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="4e684-471">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="4e684-471">Return Value - bold</span></span>

<span data-ttu-id="4e684-472">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-472">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="4e684-473">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="4e684-473">Remarks - bold</span></span>

<span data-ttu-id="4e684-474">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e684-474">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="4e684-475">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="4e684-475">0 Use the default font weight.</span></span>
-   <span data-ttu-id="4e684-476">1 シン。</span><span class="sxs-lookup"><span data-stu-id="4e684-476">1 Thin.</span></span>
-   <span data-ttu-id="4e684-477">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="4e684-477">2 Extra-light.</span></span>
-   <span data-ttu-id="4e684-478">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="4e684-478">3 Light.</span></span>
-   <span data-ttu-id="4e684-479">4 標準。</span><span class="sxs-lookup"><span data-stu-id="4e684-479">4 Normal.</span></span>
-   <span data-ttu-id="4e684-480">5 中。</span><span class="sxs-lookup"><span data-stu-id="4e684-480">5 Medium.</span></span>
-   <span data-ttu-id="4e684-481">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="4e684-481">6 Semibold.</span></span>
-   <span data-ttu-id="4e684-482">7 太字。</span><span class="sxs-lookup"><span data-stu-id="4e684-482">7 Bold.</span></span>
-   <span data-ttu-id="4e684-483">8 極太。</span><span class="sxs-lookup"><span data-stu-id="4e684-483">8 Extra-bold.</span></span>
-   <span data-ttu-id="4e684-484">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="4e684-484">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="4e684-485">メソッド border</span><span class="sxs-lookup"><span data-stu-id="4e684-485">Method border</span></span>

<span data-ttu-id="4e684-486">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-486">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="4e684-487">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="4e684-487">Parameters - border</span></span>

<span data-ttu-id="4e684-488">値</span><span class="sxs-lookup"><span data-stu-id="4e684-488">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="4e684-489">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="4e684-489">Return Value - border</span></span>

<span data-ttu-id="4e684-490">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="4e684-490">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="4e684-491">備考 - border</span><span class="sxs-lookup"><span data-stu-id="4e684-491">Remarks - border</span></span>

<span data-ttu-id="4e684-492">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e684-492">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="4e684-493">値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-493">Value.</span></span> | <span data-ttu-id="4e684-494">説明。</span><span class="sxs-lookup"><span data-stu-id="4e684-494">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="4e684-495">0</span><span class="sxs-lookup"><span data-stu-id="4e684-495">0</span></span>      | <span data-ttu-id="4e684-496">自動。</span><span class="sxs-lookup"><span data-stu-id="4e684-496">Auto.</span></span>        |
| <span data-ttu-id="4e684-497">1</span><span class="sxs-lookup"><span data-stu-id="4e684-497">1</span></span>      | <span data-ttu-id="4e684-498">3D。</span><span class="sxs-lookup"><span data-stu-id="4e684-498">3D.</span></span>          |
| <span data-ttu-id="4e684-499">2</span><span class="sxs-lookup"><span data-stu-id="4e684-499">2</span></span>      | <span data-ttu-id="4e684-500">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="4e684-500">Single line.</span></span> |
| <span data-ttu-id="4e684-501">3</span><span class="sxs-lookup"><span data-stu-id="4e684-501">3</span></span>      | <span data-ttu-id="4e684-502">均一。</span><span class="sxs-lookup"><span data-stu-id="4e684-502">Flat.</span></span>        |
| <span data-ttu-id="4e684-503">4</span><span class="sxs-lookup"><span data-stu-id="4e684-503">4</span></span>      | <span data-ttu-id="4e684-504">なし。</span><span class="sxs-lookup"><span data-stu-id="4e684-504">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="4e684-505">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-505">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="4e684-506">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-506">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="4e684-507">値</span><span class="sxs-lookup"><span data-stu-id="4e684-507">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="4e684-508">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-508">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="4e684-509">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="4e684-509">Method calcControlSize</span></span>

<span data-ttu-id="4e684-510">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-510">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="4e684-511">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="4e684-511">Parameters - calcControlSize</span></span>

<span data-ttu-id="4e684-512">chars</span><span class="sxs-lookup"><span data-stu-id="4e684-512">chars</span></span>  
<span data-ttu-id="4e684-513">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="4e684-513">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="4e684-514">明細行</span><span class="sxs-lookup"><span data-stu-id="4e684-514">lines</span></span>  
<span data-ttu-id="4e684-515">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="4e684-515">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="4e684-516">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="4e684-516">Return Value - calcControlSize</span></span>

<span data-ttu-id="4e684-517">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="4e684-517">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="4e684-518">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="4e684-518">Method characterSet</span></span>

<span data-ttu-id="4e684-519">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-519">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="4e684-520">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="4e684-520">Parameters - characterSet</span></span>

<span data-ttu-id="4e684-521">値</span><span class="sxs-lookup"><span data-stu-id="4e684-521">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="4e684-522">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="4e684-522">Return Value - characterSet</span></span>

<span data-ttu-id="4e684-523">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-523">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="4e684-524">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="4e684-524">Remarks - characterSet</span></span>

<span data-ttu-id="4e684-525">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-525">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="4e684-526">値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-526">Value.</span></span> | <span data-ttu-id="4e684-527">説明。</span><span class="sxs-lookup"><span data-stu-id="4e684-527">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="4e684-528">0</span><span class="sxs-lookup"><span data-stu-id="4e684-528">0</span></span>      | <span data-ttu-id="4e684-529">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-529">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="4e684-530">1</span><span class="sxs-lookup"><span data-stu-id="4e684-530">1</span></span>      | <span data-ttu-id="4e684-531">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-531">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="4e684-532">2</span><span class="sxs-lookup"><span data-stu-id="4e684-532">2</span></span>      | <span data-ttu-id="4e684-533">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-533">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="4e684-534">77</span><span class="sxs-lookup"><span data-stu-id="4e684-534">77</span></span>     | <span data-ttu-id="4e684-535">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-535">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="4e684-536">128</span><span class="sxs-lookup"><span data-stu-id="4e684-536">128</span></span>    | <span data-ttu-id="4e684-537">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-537">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="4e684-538">129</span><span class="sxs-lookup"><span data-stu-id="4e684-538">129</span></span>    | <span data-ttu-id="4e684-539">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-539">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="4e684-540">134</span><span class="sxs-lookup"><span data-stu-id="4e684-540">134</span></span>    | <span data-ttu-id="4e684-541">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-541">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="4e684-542">136</span><span class="sxs-lookup"><span data-stu-id="4e684-542">136</span></span>    | <span data-ttu-id="4e684-543">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-543">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="4e684-544">161</span><span class="sxs-lookup"><span data-stu-id="4e684-544">161</span></span>    | <span data-ttu-id="4e684-545">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-545">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="4e684-546">162</span><span class="sxs-lookup"><span data-stu-id="4e684-546">162</span></span>    | <span data-ttu-id="4e684-547">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-547">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="4e684-548">163</span><span class="sxs-lookup"><span data-stu-id="4e684-548">163</span></span>    | <span data-ttu-id="4e684-549">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-549">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="4e684-550">186</span><span class="sxs-lookup"><span data-stu-id="4e684-550">186</span></span>    | <span data-ttu-id="4e684-551">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-551">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="4e684-552">204</span><span class="sxs-lookup"><span data-stu-id="4e684-552">204</span></span>    | <span data-ttu-id="4e684-553">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-553">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="4e684-554">238</span><span class="sxs-lookup"><span data-stu-id="4e684-554">238</span></span>    | <span data-ttu-id="4e684-555">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-555">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="4e684-556">255</span><span class="sxs-lookup"><span data-stu-id="4e684-556">255</span></span>    | <span data-ttu-id="4e684-557">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-557">OEM\_CHARSET</span></span>         |

<span data-ttu-id="4e684-558">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-558">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="4e684-559">値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-559">Value.</span></span> | <span data-ttu-id="4e684-560">説明。</span><span class="sxs-lookup"><span data-stu-id="4e684-560">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="4e684-561">130</span><span class="sxs-lookup"><span data-stu-id="4e684-561">130</span></span>    | <span data-ttu-id="4e684-562">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-562">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="4e684-563">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-563">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="4e684-564">値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-564">Value.</span></span> | <span data-ttu-id="4e684-565">説明。</span><span class="sxs-lookup"><span data-stu-id="4e684-565">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="4e684-566">177</span><span class="sxs-lookup"><span data-stu-id="4e684-566">177</span></span>    | <span data-ttu-id="4e684-567">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-567">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="4e684-568">178</span><span class="sxs-lookup"><span data-stu-id="4e684-568">178</span></span>    | <span data-ttu-id="4e684-569">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-569">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="4e684-570">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-570">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="4e684-571">値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-571">Value.</span></span> | <span data-ttu-id="4e684-572">説明。</span><span class="sxs-lookup"><span data-stu-id="4e684-572">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="4e684-573">222</span><span class="sxs-lookup"><span data-stu-id="4e684-573">222</span></span>    | <span data-ttu-id="4e684-574">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4e684-574">THAI\_CHARSET</span></span> |

<span data-ttu-id="4e684-575">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-575">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="4e684-576">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-576">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="4e684-577">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e684-577">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-charfrompos"></a><span data-ttu-id="4e684-578">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="4e684-578">Method charFromPos</span></span>

```xpp
public int charFromPos(int x, int y)
```

### <a name="parameters---charfrompos"></a><span data-ttu-id="4e684-579">パラメーター - charFromPos</span><span class="sxs-lookup"><span data-stu-id="4e684-579">Parameters - charFromPos</span></span>

<span data-ttu-id="4e684-580">x</span><span class="sxs-lookup"><span data-stu-id="4e684-580">x</span></span>  

<!-- -->

<span data-ttu-id="4e684-581">y</span><span class="sxs-lookup"><span data-stu-id="4e684-581">y</span></span>  

### <a name="return-value---charfrompos"></a><span data-ttu-id="4e684-582">戻り値 - charFromPos</span><span class="sxs-lookup"><span data-stu-id="4e684-582">Return Value - charFromPos</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="4e684-583">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="4e684-583">Method colorScheme</span></span>

<span data-ttu-id="4e684-584">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-584">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="4e684-585">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4e684-585">Parameters - colorScheme</span></span>

<span data-ttu-id="4e684-586">値</span><span class="sxs-lookup"><span data-stu-id="4e684-586">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="4e684-587">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4e684-587">Return Value - colorScheme</span></span>

<span data-ttu-id="4e684-588">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="4e684-588">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="4e684-589">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4e684-589">Remarks - colorScheme</span></span>

<span data-ttu-id="4e684-590">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-590">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="4e684-591">値です。</span><span class="sxs-lookup"><span data-stu-id="4e684-591">Value.</span></span> | <span data-ttu-id="4e684-592">スタイル。</span><span class="sxs-lookup"><span data-stu-id="4e684-592">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="4e684-593">0</span><span class="sxs-lookup"><span data-stu-id="4e684-593">0</span></span>      | <span data-ttu-id="4e684-594">既定。</span><span class="sxs-lookup"><span data-stu-id="4e684-594">Default.</span></span>                       |
| <span data-ttu-id="4e684-595">1</span><span class="sxs-lookup"><span data-stu-id="4e684-595">1</span></span>      | <span data-ttu-id="4e684-596">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="4e684-596">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="4e684-597">2</span><span class="sxs-lookup"><span data-stu-id="4e684-597">2</span></span>      | <span data-ttu-id="4e684-598">真の配色。</span><span class="sxs-lookup"><span data-stu-id="4e684-598">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="4e684-599">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="4e684-599">Method configurationKey</span></span>

<span data-ttu-id="4e684-600">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-600">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="4e684-601">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="4e684-601">Parameters - configurationKey</span></span>

<span data-ttu-id="4e684-602">値</span><span class="sxs-lookup"><span data-stu-id="4e684-602">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="4e684-603">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="4e684-603">Return Value - configurationKey</span></span>

<span data-ttu-id="4e684-604">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="4e684-604">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="4e684-605">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="4e684-605">Remarks - configurationKey</span></span>

<span data-ttu-id="4e684-606">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-606">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="4e684-607">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="4e684-607">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="4e684-608">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="4e684-608">Method configurationKeyEx</span></span>

<span data-ttu-id="4e684-609">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-609">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="4e684-610">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="4e684-610">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="4e684-611">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="4e684-611">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="4e684-612">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="4e684-612">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="4e684-613">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="4e684-613">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="4e684-614">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e684-614">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="4e684-615">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e684-615">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="4e684-616">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="4e684-616">Method countryRegionCodes</span></span>

<span data-ttu-id="4e684-617">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-617">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="4e684-618">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="4e684-618">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="4e684-619">値</span><span class="sxs-lookup"><span data-stu-id="4e684-619">value</span></span>  
<span data-ttu-id="4e684-620">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-620">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="4e684-621">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="4e684-621">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="4e684-622">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="4e684-622">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="4e684-623">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="4e684-623">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="4e684-624">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="4e684-624">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="4e684-625">値</span><span class="sxs-lookup"><span data-stu-id="4e684-625">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="4e684-626">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="4e684-626">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="4e684-627">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="4e684-627">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="4e684-628">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="4e684-628">Parameters - dataField</span></span>

<span data-ttu-id="4e684-629">値</span><span class="sxs-lookup"><span data-stu-id="4e684-629">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="4e684-630">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="4e684-630">Return Value - dataField</span></span>

## <a name="method-datafieldarrayindex"></a><span data-ttu-id="4e684-631">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-631">Method dataFieldArrayIndex</span></span>

```xpp
public int dataFieldArrayIndex()
```

### <a name="return-value---datafieldarrayindex"></a><span data-ttu-id="4e684-632">戻り値 - dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-632">Return Value - dataFieldArrayIndex</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="4e684-633">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="4e684-633">Method dataFieldName</span></span>

```xpp
public FieldName dataFieldName()
```

### <a name="return-value---datafieldname"></a><span data-ttu-id="4e684-634">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="4e684-634">Return Value - dataFieldName</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="4e684-635">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-635">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="4e684-636">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-636">Parameters - dataMethod</span></span>

<span data-ttu-id="4e684-637">値</span><span class="sxs-lookup"><span data-stu-id="4e684-637">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="4e684-638">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-638">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="4e684-639">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="4e684-639">Method dataRelationPath</span></span>

<span data-ttu-id="4e684-640">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-640">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="4e684-641">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="4e684-641">Parameters - dataRelationPath</span></span>

<span data-ttu-id="4e684-642">値</span><span class="sxs-lookup"><span data-stu-id="4e684-642">value</span></span>  
<span data-ttu-id="4e684-643">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-643">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="4e684-644">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="4e684-644">Return Value - dataRelationPath</span></span>

<span data-ttu-id="4e684-645">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="4e684-645">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="4e684-646">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="4e684-646">Remarks - dataRelationPath</span></span>

<span data-ttu-id="4e684-647">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="4e684-647">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="4e684-648">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="4e684-648">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="4e684-649">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="4e684-649">Method dataSource</span></span>

<span data-ttu-id="4e684-650">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-650">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="4e684-651">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="4e684-651">Parameters - dataSource</span></span>

<span data-ttu-id="4e684-652">値</span><span class="sxs-lookup"><span data-stu-id="4e684-652">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="4e684-653">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="4e684-653">Return Value - dataSource</span></span>

<span data-ttu-id="4e684-654">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="4e684-654">The identifier of the data source to be used.</span></span>

## <a name="method-dateday"></a><span data-ttu-id="4e684-655">メソッド dateDay</span><span class="sxs-lookup"><span data-stu-id="4e684-655">Method dateDay</span></span>

```xpp
public int dateDay([int value])
```

### <a name="parameters---dateday"></a><span data-ttu-id="4e684-656">パラメーター - dateDay</span><span class="sxs-lookup"><span data-stu-id="4e684-656">Parameters - dateDay</span></span>

<span data-ttu-id="4e684-657">値</span><span class="sxs-lookup"><span data-stu-id="4e684-657">value</span></span>  

### <a name="return-value---dateday"></a><span data-ttu-id="4e684-658">戻り値 - dateDay</span><span class="sxs-lookup"><span data-stu-id="4e684-658">Return Value - dateDay</span></span>

## <a name="method-dateformat"></a><span data-ttu-id="4e684-659">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="4e684-659">Method dateFormat</span></span>

```xpp
public int dateFormat([int value])
```

### <a name="parameters---dateformat"></a><span data-ttu-id="4e684-660">パラメーター - dateFormat</span><span class="sxs-lookup"><span data-stu-id="4e684-660">Parameters - dateFormat</span></span>

<span data-ttu-id="4e684-661">値</span><span class="sxs-lookup"><span data-stu-id="4e684-661">value</span></span>  

### <a name="return-value---dateformat"></a><span data-ttu-id="4e684-662">戻り値 - dateFormat</span><span class="sxs-lookup"><span data-stu-id="4e684-662">Return Value - dateFormat</span></span>

## <a name="method-datemonth"></a><span data-ttu-id="4e684-663">メソッド dateMonth</span><span class="sxs-lookup"><span data-stu-id="4e684-663">Method dateMonth</span></span>

```xpp
public int dateMonth([int value])
```

### <a name="parameters---datemonth"></a><span data-ttu-id="4e684-664">パラメーター - dateMonth</span><span class="sxs-lookup"><span data-stu-id="4e684-664">Parameters - dateMonth</span></span>

<span data-ttu-id="4e684-665">値</span><span class="sxs-lookup"><span data-stu-id="4e684-665">value</span></span>  

### <a name="return-value---datemonth"></a><span data-ttu-id="4e684-666">戻り値 - dateMonth</span><span class="sxs-lookup"><span data-stu-id="4e684-666">Return Value - dateMonth</span></span>

## <a name="method-dateseparator"></a><span data-ttu-id="4e684-667">メソッド dateSeparator</span><span class="sxs-lookup"><span data-stu-id="4e684-667">Method dateSeparator</span></span>

```xpp
public int dateSeparator([int value])
```

### <a name="parameters---dateseparator"></a><span data-ttu-id="4e684-668">パラメーター - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="4e684-668">Parameters - dateSeparator</span></span>

<span data-ttu-id="4e684-669">値</span><span class="sxs-lookup"><span data-stu-id="4e684-669">value</span></span>  

### <a name="return-value---dateseparator"></a><span data-ttu-id="4e684-670">戻り値 - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="4e684-670">Return Value - dateSeparator</span></span>

## <a name="method-datevalue"></a><span data-ttu-id="4e684-671">メソッド dateValue</span><span class="sxs-lookup"><span data-stu-id="4e684-671">Method dateValue</span></span>

```xpp
public Date dateValue([Date value])
```

### <a name="parameters---datevalue"></a><span data-ttu-id="4e684-672">パラメーター - dateValue</span><span class="sxs-lookup"><span data-stu-id="4e684-672">Parameters - dateValue</span></span>

<span data-ttu-id="4e684-673">値</span><span class="sxs-lookup"><span data-stu-id="4e684-673">value</span></span>  

### <a name="return-value---datevalue"></a><span data-ttu-id="4e684-674">戻り値 - dateValue</span><span class="sxs-lookup"><span data-stu-id="4e684-674">Return Value - dateValue</span></span>

## <a name="method-dateyear"></a><span data-ttu-id="4e684-675">メソッド dateYear</span><span class="sxs-lookup"><span data-stu-id="4e684-675">Method dateYear</span></span>

```xpp
public int dateYear([int value])
```

### <a name="parameters---dateyear"></a><span data-ttu-id="4e684-676">パラメーター - dateYear</span><span class="sxs-lookup"><span data-stu-id="4e684-676">Parameters - dateYear</span></span>

<span data-ttu-id="4e684-677">値</span><span class="sxs-lookup"><span data-stu-id="4e684-677">value</span></span>  

### <a name="return-value---dateyear"></a><span data-ttu-id="4e684-678">戻り値 - dateYear</span><span class="sxs-lookup"><span data-stu-id="4e684-678">Return Value - dateYear</span></span>

## <a name="method-direction"></a><span data-ttu-id="4e684-679">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="4e684-679">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="4e684-680">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="4e684-680">Parameters - direction</span></span>

<span data-ttu-id="4e684-681">値</span><span class="sxs-lookup"><span data-stu-id="4e684-681">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="4e684-682">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="4e684-682">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="4e684-683">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-683">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="4e684-684">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-684">Parameters - displayHeight</span></span>

<span data-ttu-id="4e684-685">値</span><span class="sxs-lookup"><span data-stu-id="4e684-685">value</span></span>  

<!-- -->

<span data-ttu-id="4e684-686">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-686">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="4e684-687">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-687">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="4e684-688">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-688">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="4e684-689">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-689">Parameters - displayHeightMode</span></span>

<span data-ttu-id="4e684-690">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-690">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="4e684-691">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-691">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="4e684-692">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-692">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="4e684-693">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-693">Parameters - displayHeightValue</span></span>

<span data-ttu-id="4e684-694">値</span><span class="sxs-lookup"><span data-stu-id="4e684-694">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="4e684-695">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-695">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="4e684-696">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="4e684-696">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="4e684-697">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="4e684-697">Parameters - displayLength</span></span>

<span data-ttu-id="4e684-698">値</span><span class="sxs-lookup"><span data-stu-id="4e684-698">value</span></span>  

<!-- -->

<span data-ttu-id="4e684-699">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-699">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="4e684-700">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="4e684-700">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="4e684-701">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-701">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="4e684-702">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-702">Parameters - displayLengthMode</span></span>

<span data-ttu-id="4e684-703">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-703">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="4e684-704">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-704">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="4e684-705">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-705">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="4e684-706">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-706">Parameters - displayLengthValue</span></span>

<span data-ttu-id="4e684-707">値</span><span class="sxs-lookup"><span data-stu-id="4e684-707">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="4e684-708">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-708">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="4e684-709">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="4e684-709">Method displayTarget</span></span>

<span data-ttu-id="4e684-710">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-710">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="4e684-711">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="4e684-711">Parameters - displayTarget</span></span>

<span data-ttu-id="4e684-712">値</span><span class="sxs-lookup"><span data-stu-id="4e684-712">value</span></span>  
<span data-ttu-id="4e684-713">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-713">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="4e684-714">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="4e684-714">Return Value - displayTarget</span></span>

<span data-ttu-id="4e684-715">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="4e684-715">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="4e684-716">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="4e684-716">Method dragDrop</span></span>

<span data-ttu-id="4e684-717">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-717">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="4e684-718">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="4e684-718">Parameters - dragDrop</span></span>

<span data-ttu-id="4e684-719">値</span><span class="sxs-lookup"><span data-stu-id="4e684-719">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="4e684-720">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="4e684-720">Return Value - dragDrop</span></span>

<span data-ttu-id="4e684-721">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="4e684-721">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="4e684-722">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="4e684-722">Method dragOver</span></span>

<span data-ttu-id="4e684-723">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-723">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="4e684-724">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="4e684-724">Parameters - dragOver</span></span>

<span data-ttu-id="4e684-725">dragSource</span><span class="sxs-lookup"><span data-stu-id="4e684-725">dragSource</span></span>  
<span data-ttu-id="4e684-726">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-726">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-727">dragMode</span><span class="sxs-lookup"><span data-stu-id="4e684-727">dragMode</span></span>  
<span data-ttu-id="4e684-728">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-728">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-729">x</span><span class="sxs-lookup"><span data-stu-id="4e684-729">x</span></span>  
<span data-ttu-id="4e684-730">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-730">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-731">y</span><span class="sxs-lookup"><span data-stu-id="4e684-731">y</span></span>  
<span data-ttu-id="4e684-732">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-732">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="4e684-733">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="4e684-733">Return Value - dragOver</span></span>

<span data-ttu-id="4e684-734">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="4e684-734">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="4e684-735">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="4e684-735">Method dragOverEx</span></span>

<span data-ttu-id="4e684-736">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-736">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="4e684-737">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="4e684-737">Parameters - dragOverEx</span></span>

<span data-ttu-id="4e684-738">dragSource</span><span class="sxs-lookup"><span data-stu-id="4e684-738">dragSource</span></span>  
<span data-ttu-id="4e684-739">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-739">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-740">dragMode</span><span class="sxs-lookup"><span data-stu-id="4e684-740">dragMode</span></span>  
<span data-ttu-id="4e684-741">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-741">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-742">x</span><span class="sxs-lookup"><span data-stu-id="4e684-742">x</span></span>  
<span data-ttu-id="4e684-743">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-743">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-744">y</span><span class="sxs-lookup"><span data-stu-id="4e684-744">y</span></span>  
<span data-ttu-id="4e684-745">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-745">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="4e684-746">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="4e684-746">Return Value - dragOverEx</span></span>

<span data-ttu-id="4e684-747">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="4e684-747">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="4e684-748">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="4e684-748">Method dragText</span></span>

<span data-ttu-id="4e684-749">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-749">Retrieves the text that id displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="4e684-750">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="4e684-750">Return Value - dragText</span></span>

<span data-ttu-id="4e684-751">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="4e684-751">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="4e684-752">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="4e684-752">Method enabled</span></span>

<span data-ttu-id="4e684-753">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-753">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="4e684-754">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="4e684-754">Parameters - enabled</span></span>

<span data-ttu-id="4e684-755">値</span><span class="sxs-lookup"><span data-stu-id="4e684-755">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="4e684-756">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="4e684-756">Return Value - enabled</span></span>

<span data-ttu-id="4e684-757">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-757">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="4e684-758">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="4e684-758">Remarks - enabled</span></span>

<span data-ttu-id="4e684-759">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="4e684-759">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="4e684-760">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4e684-760">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="4e684-761">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4e684-761">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="4e684-762">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="4e684-762">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="4e684-763">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="4e684-763">Parameters - extendedDataType</span></span>

<span data-ttu-id="4e684-764">値</span><span class="sxs-lookup"><span data-stu-id="4e684-764">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="4e684-765">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="4e684-765">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="4e684-766">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="4e684-766">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="4e684-767">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="4e684-767">Parameters - fastTabSummary</span></span>

<span data-ttu-id="4e684-768">値</span><span class="sxs-lookup"><span data-stu-id="4e684-768">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="4e684-769">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="4e684-769">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="4e684-770">メソッド font</span><span class="sxs-lookup"><span data-stu-id="4e684-770">Method font</span></span>

<span data-ttu-id="4e684-771">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-771">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="4e684-772">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="4e684-772">Parameters - font</span></span>

<span data-ttu-id="4e684-773">値</span><span class="sxs-lookup"><span data-stu-id="4e684-773">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="4e684-774">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="4e684-774">Return Value - font</span></span>

<span data-ttu-id="4e684-775">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="4e684-775">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="4e684-776">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="4e684-776">Method fontSize</span></span>

<span data-ttu-id="4e684-777">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-777">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="4e684-778">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="4e684-778">Parameters - fontSize</span></span>

<span data-ttu-id="4e684-779">値</span><span class="sxs-lookup"><span data-stu-id="4e684-779">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="4e684-780">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="4e684-780">Return Value - fontSize</span></span>

<span data-ttu-id="4e684-781">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="4e684-781">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="4e684-782">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-782">Method foregroundColor</span></span>

<span data-ttu-id="4e684-783">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-783">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="4e684-784">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-784">Parameters - foregroundColor</span></span>

<span data-ttu-id="4e684-785">値</span><span class="sxs-lookup"><span data-stu-id="4e684-785">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="4e684-786">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-786">Return Value - foregroundColor</span></span>

<span data-ttu-id="4e684-787">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="4e684-787">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="4e684-788">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-788">Remarks - foregroundColor</span></span>

<span data-ttu-id="4e684-789">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e684-789">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="4e684-790">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4e684-790">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="4e684-791">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4e684-791">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="4e684-792">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4e684-792">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="4e684-793">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4e684-793">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="4e684-794">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="4e684-794">The maximum value for a single byte is 255.</span></span>

## <a name="method-getcursorpos"></a><span data-ttu-id="4e684-795">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="4e684-795">Method getCursorPos</span></span>

```xpp
public container getCursorPos()
```

### <a name="return-value---getcursorpos"></a><span data-ttu-id="4e684-796">戻り値 - getCursorPos</span><span class="sxs-lookup"><span data-stu-id="4e684-796">Return Value - getCursorPos</span></span>

## <a name="method-getfirstvisibleline"></a><span data-ttu-id="4e684-797">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="4e684-797">Method getFirstVisibleLine</span></span>

```xpp
public int getFirstVisibleLine()
```

### <a name="return-value---getfirstvisibleline"></a><span data-ttu-id="4e684-798">戻り値 - getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="4e684-798">Return Value - getFirstVisibleLine</span></span>

## <a name="method-getline"></a><span data-ttu-id="4e684-799">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="4e684-799">Method getLine</span></span>

```xpp
public str getLine(int lineNo)
```

### <a name="parameters---getline"></a><span data-ttu-id="4e684-800">パラメーター - getLine</span><span class="sxs-lookup"><span data-stu-id="4e684-800">Parameters - getLine</span></span>

<span data-ttu-id="4e684-801">lineNo</span><span class="sxs-lookup"><span data-stu-id="4e684-801">lineNo</span></span>  

### <a name="return-value---getline"></a><span data-ttu-id="4e684-802">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="4e684-802">Return Value - getLine</span></span>

## <a name="method-getlinecount"></a><span data-ttu-id="4e684-803">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="4e684-803">Method getLineCount</span></span>

```xpp
public int getLineCount()
```

### <a name="return-value---getlinecount"></a><span data-ttu-id="4e684-804">戻り値 - getLineCount</span><span class="sxs-lookup"><span data-stu-id="4e684-804">Return Value - getLineCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="4e684-805">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="4e684-805">Method getSelection</span></span>

```xpp
public container getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="4e684-806">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="4e684-806">Return Value - getSelection</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="4e684-807">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="4e684-807">Method hasChanged</span></span>

<span data-ttu-id="4e684-808">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-808">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="4e684-809">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="4e684-809">Parameters - hasChanged</span></span>

<span data-ttu-id="4e684-810">val</span><span class="sxs-lookup"><span data-stu-id="4e684-810">val</span></span>  
<span data-ttu-id="4e684-811">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-811">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="4e684-812">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="4e684-812">Return Value - hasChanged</span></span>

<span data-ttu-id="4e684-813">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-813">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="4e684-814">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="4e684-814">Method hasUserSetting</span></span>

<span data-ttu-id="4e684-815">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-815">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="4e684-816">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="4e684-816">Return Value - hasUserSetting</span></span>

<span data-ttu-id="4e684-817">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-817">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="4e684-818">メソッド height</span><span class="sxs-lookup"><span data-stu-id="4e684-818">Method height</span></span>

<span data-ttu-id="4e684-819">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-819">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="4e684-820">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="4e684-820">Parameters - height</span></span>

<span data-ttu-id="4e684-821">値</span><span class="sxs-lookup"><span data-stu-id="4e684-821">value</span></span>  

<!-- -->

<span data-ttu-id="4e684-822">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-822">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="4e684-823">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="4e684-823">Return Value - height</span></span>

<span data-ttu-id="4e684-824">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="4e684-824">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="4e684-825">備考 - height</span><span class="sxs-lookup"><span data-stu-id="4e684-825">Remarks - height</span></span>

<span data-ttu-id="4e684-826">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-826">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="4e684-827">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="4e684-827">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="4e684-828">モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-828">Mode.</span></span>            | <span data-ttu-id="4e684-829">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="4e684-829">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e684-830">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="4e684-830">-1 Exact.</span></span>        | <span data-ttu-id="4e684-831">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-831">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4e684-832">0 自動。</span><span class="sxs-lookup"><span data-stu-id="4e684-832">0 Auto.</span></span>          | <span data-ttu-id="4e684-833">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-833">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4e684-834">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="4e684-834">1 Column height.</span></span> | <span data-ttu-id="4e684-835">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="4e684-835">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="4e684-836">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="4e684-836">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="4e684-837">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-837">Method heightMode</span></span>

<span data-ttu-id="4e684-838">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-838">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="4e684-839">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-839">Parameters - heightMode</span></span>

<span data-ttu-id="4e684-840">値</span><span class="sxs-lookup"><span data-stu-id="4e684-840">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="4e684-841">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-841">Return Value - heightMode</span></span>

<span data-ttu-id="4e684-842">計算モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-842">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="4e684-843">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-843">Remarks - heightMode</span></span>

<span data-ttu-id="4e684-844">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="4e684-844">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="4e684-845">モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-845">Mode.</span></span>          | <span data-ttu-id="4e684-846">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="4e684-846">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e684-847">正確。</span><span class="sxs-lookup"><span data-stu-id="4e684-847">Exact.</span></span>         | <span data-ttu-id="4e684-848">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-848">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4e684-849">自動。</span><span class="sxs-lookup"><span data-stu-id="4e684-849">Auto.</span></span>          | <span data-ttu-id="4e684-850">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-850">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4e684-851">列の高さ</span><span class="sxs-lookup"><span data-stu-id="4e684-851">Column height.</span></span> | <span data-ttu-id="4e684-852">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="4e684-852">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="4e684-853">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="4e684-853">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="4e684-854">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-854">Method heightValue</span></span>

<span data-ttu-id="4e684-855">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-855">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="4e684-856">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-856">Parameters - heightValue</span></span>

<span data-ttu-id="4e684-857">値</span><span class="sxs-lookup"><span data-stu-id="4e684-857">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="4e684-858">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-858">Return Value - heightValue</span></span>

<span data-ttu-id="4e684-859">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="4e684-859">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="4e684-860">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-860">Remarks - heightValue</span></span>

<span data-ttu-id="4e684-861">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="4e684-861">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="4e684-862">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="4e684-862">Method helpField</span></span>

<span data-ttu-id="4e684-863">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-863">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="4e684-864">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="4e684-864">Return Value - helpField</span></span>

<span data-ttu-id="4e684-865">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="4e684-865">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="4e684-866">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="4e684-866">Remarks - helpField</span></span>

<span data-ttu-id="4e684-867">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="4e684-867">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="4e684-868">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e684-868">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="4e684-869">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="4e684-869">Method helpText</span></span>

<span data-ttu-id="4e684-870">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-870">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="4e684-871">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="4e684-871">Parameters - helpText</span></span>

<span data-ttu-id="4e684-872">値</span><span class="sxs-lookup"><span data-stu-id="4e684-872">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="4e684-873">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="4e684-873">Return Value - helpText</span></span>

<span data-ttu-id="4e684-874">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="4e684-874">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="4e684-875">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="4e684-875">Remarks - helpText</span></span>

<span data-ttu-id="4e684-876">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-876">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="4e684-877">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="4e684-877">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="4e684-878">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="4e684-878">Method hierarchyParent</span></span>

<span data-ttu-id="4e684-879">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-879">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="4e684-880">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="4e684-880">Parameters - hierarchyParent</span></span>

<span data-ttu-id="4e684-881">値</span><span class="sxs-lookup"><span data-stu-id="4e684-881">value</span></span>  
<span data-ttu-id="4e684-882">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="4e684-882">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="4e684-883">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="4e684-883">Return Value - hierarchyParent</span></span>

<span data-ttu-id="4e684-884">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="4e684-884">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="4e684-885">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="4e684-885">Method hWnd</span></span>

<span data-ttu-id="4e684-886">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-886">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="4e684-887">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="4e684-887">Return Value - hWnd</span></span>

<span data-ttu-id="4e684-888">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="4e684-888">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="4e684-889">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="4e684-889">Remarks - hWnd</span></span>

<span data-ttu-id="4e684-890">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="4e684-890">The handle can be used with the Windows API.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="4e684-891">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="4e684-891">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="4e684-892">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="4e684-892">Parameters - iMEMode</span></span>

<span data-ttu-id="4e684-893">値</span><span class="sxs-lookup"><span data-stu-id="4e684-893">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="4e684-894">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="4e684-894">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="4e684-895">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="4e684-895">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="4e684-896">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="4e684-896">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="4e684-897">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="4e684-897">Method isDisplayed</span></span>

<span data-ttu-id="4e684-898">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-898">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="4e684-899">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="4e684-899">Return Value - isDisplayed</span></span>

<span data-ttu-id="4e684-900">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="4e684-900">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="4e684-901">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="4e684-901">Remarks - isDisplayed</span></span>

<span data-ttu-id="4e684-902">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4e684-902">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="4e684-903">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="4e684-903">Method isRestricted</span></span>

<span data-ttu-id="4e684-904">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-904">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="4e684-905">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="4e684-905">Return Value - isRestricted</span></span>

<span data-ttu-id="4e684-906">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="4e684-906">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="4e684-907">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="4e684-907">Method isUserSetupEnabled</span></span>

<span data-ttu-id="4e684-908">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-908">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="4e684-909">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="4e684-909">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="4e684-910">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="4e684-910">neededSetupRights</span></span>  
<span data-ttu-id="4e684-911">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値、オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-911">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control; optional.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="4e684-912">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="4e684-912">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="4e684-913">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-913">true if the control, design, and parent containers allow for the level of customization that specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="4e684-914">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="4e684-914">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="4e684-915">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="4e684-915">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e684-916">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="4e684-916">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="4e684-917">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="4e684-917">No changes can be made to the control.</span></span> <span data-ttu-id="4e684-918">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-918">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="4e684-919">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="4e684-919">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="4e684-920">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="4e684-920">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="4e684-921">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="4e684-921">The user cannot move the control.</span></span>   |
| <span data-ttu-id="4e684-922">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="4e684-922">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="4e684-923">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="4e684-923">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="4e684-924">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="4e684-924">The user can also move the control.</span></span> |

<span data-ttu-id="4e684-925">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e684-925">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="4e684-926">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="4e684-926">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="4e684-927">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="4e684-927">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="4e684-928">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="4e684-928">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="4e684-929">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="4e684-929">Parameters - italic</span></span>

<span data-ttu-id="4e684-930">値</span><span class="sxs-lookup"><span data-stu-id="4e684-930">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="4e684-931">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="4e684-931">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="4e684-932">メソッド label</span><span class="sxs-lookup"><span data-stu-id="4e684-932">Method label</span></span>

<span data-ttu-id="4e684-933">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-933">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="4e684-934">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="4e684-934">Parameters - label</span></span>

<span data-ttu-id="4e684-935">値</span><span class="sxs-lookup"><span data-stu-id="4e684-935">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="4e684-936">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="4e684-936">Return Value - label</span></span>

<span data-ttu-id="4e684-937">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="4e684-937">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="4e684-938">備考 - label</span><span class="sxs-lookup"><span data-stu-id="4e684-938">Remarks - label</span></span>

<span data-ttu-id="4e684-939">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-939">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="4e684-940">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="4e684-940">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="4e684-941">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="4e684-941">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="4e684-942">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="4e684-942">Parameters - labelAlignment</span></span>

<span data-ttu-id="4e684-943">値</span><span class="sxs-lookup"><span data-stu-id="4e684-943">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="4e684-944">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="4e684-944">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="4e684-945">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="4e684-945">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="4e684-946">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="4e684-946">Parameters - labelBold</span></span>

<span data-ttu-id="4e684-947">値</span><span class="sxs-lookup"><span data-stu-id="4e684-947">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="4e684-948">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="4e684-948">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="4e684-949">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="4e684-949">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="4e684-950">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="4e684-950">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="4e684-951">値</span><span class="sxs-lookup"><span data-stu-id="4e684-951">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="4e684-952">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="4e684-952">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="4e684-953">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="4e684-953">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="4e684-954">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="4e684-954">Parameters - labelFont</span></span>

<span data-ttu-id="4e684-955">値</span><span class="sxs-lookup"><span data-stu-id="4e684-955">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="4e684-956">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="4e684-956">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="4e684-957">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="4e684-957">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="4e684-958">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="4e684-958">Parameters - labelFontSize</span></span>

<span data-ttu-id="4e684-959">値</span><span class="sxs-lookup"><span data-stu-id="4e684-959">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="4e684-960">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="4e684-960">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="4e684-961">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-961">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="4e684-962">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-962">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="4e684-963">値</span><span class="sxs-lookup"><span data-stu-id="4e684-963">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="4e684-964">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="4e684-964">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="4e684-965">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="4e684-965">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="4e684-966">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="4e684-966">Parameters - labelGuide</span></span>

<span data-ttu-id="4e684-967">値</span><span class="sxs-lookup"><span data-stu-id="4e684-967">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="4e684-968">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="4e684-968">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="4e684-969">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-969">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="4e684-970">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-970">Parameters - labelHeight</span></span>

<span data-ttu-id="4e684-971">値</span><span class="sxs-lookup"><span data-stu-id="4e684-971">value</span></span>  

<!-- -->

<span data-ttu-id="4e684-972">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-972">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="4e684-973">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-973">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="4e684-974">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-974">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="4e684-975">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-975">Parameters - labelHeightMode</span></span>

<span data-ttu-id="4e684-976">値</span><span class="sxs-lookup"><span data-stu-id="4e684-976">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="4e684-977">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="4e684-977">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="4e684-978">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-978">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="4e684-979">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-979">Parameters - labelHeightValue</span></span>

<span data-ttu-id="4e684-980">値</span><span class="sxs-lookup"><span data-stu-id="4e684-980">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="4e684-981">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="4e684-981">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="4e684-982">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="4e684-982">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="4e684-983">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="4e684-983">Parameters - labelItalic</span></span>

<span data-ttu-id="4e684-984">値</span><span class="sxs-lookup"><span data-stu-id="4e684-984">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="4e684-985">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="4e684-985">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="4e684-986">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="4e684-986">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="4e684-987">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="4e684-987">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="4e684-988">x</span><span class="sxs-lookup"><span data-stu-id="4e684-988">x</span></span>  

<!-- -->

<span data-ttu-id="4e684-989">y</span><span class="sxs-lookup"><span data-stu-id="4e684-989">y</span></span>  

<!-- -->

<span data-ttu-id="4e684-990">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-990">button</span></span>  

<!-- -->

<span data-ttu-id="4e684-991">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-991">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="4e684-992">Shift</span><span class="sxs-lookup"><span data-stu-id="4e684-992">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="4e684-993">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="4e684-993">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="4e684-994">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="4e684-994">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="4e684-995">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="4e684-995">Parameters - labelMouseDown</span></span>

<span data-ttu-id="4e684-996">x</span><span class="sxs-lookup"><span data-stu-id="4e684-996">x</span></span>  

<!-- -->

<span data-ttu-id="4e684-997">y</span><span class="sxs-lookup"><span data-stu-id="4e684-997">y</span></span>  

<!-- -->

<span data-ttu-id="4e684-998">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-998">button</span></span>  

<!-- -->

<span data-ttu-id="4e684-999">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-999">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="4e684-1000">Shift</span><span class="sxs-lookup"><span data-stu-id="4e684-1000">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="4e684-1001">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="4e684-1001">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="4e684-1002">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="4e684-1002">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="4e684-1003">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="4e684-1003">Parameters - labelMouseUp</span></span>

<span data-ttu-id="4e684-1004">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1004">x</span></span>  

<!-- -->

<span data-ttu-id="4e684-1005">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1005">y</span></span>  

<!-- -->

<span data-ttu-id="4e684-1006">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-1006">button</span></span>  

<!-- -->

<span data-ttu-id="4e684-1007">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-1007">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="4e684-1008">Shift</span><span class="sxs-lookup"><span data-stu-id="4e684-1008">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="4e684-1009">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="4e684-1009">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="4e684-1010">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="4e684-1010">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="4e684-1011">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="4e684-1011">Parameters - labelPosition</span></span>

<span data-ttu-id="4e684-1012">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1012">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="4e684-1013">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="4e684-1013">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="4e684-1014">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="4e684-1014">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="4e684-1015">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="4e684-1015">Parameters - labelUnderline</span></span>

<span data-ttu-id="4e684-1016">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1016">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="4e684-1017">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="4e684-1017">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="4e684-1018">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="4e684-1018">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="4e684-1019">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="4e684-1019">Parameters - labelWidth</span></span>

<span data-ttu-id="4e684-1020">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1020">value</span></span>  

<!-- -->

<span data-ttu-id="4e684-1021">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1021">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="4e684-1022">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="4e684-1022">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="4e684-1023">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1023">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="4e684-1024">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1024">Parameters - labelWidthMode</span></span>

<span data-ttu-id="4e684-1025">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1025">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="4e684-1026">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1026">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="4e684-1027">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1027">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="4e684-1028">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1028">Parameters - labelWidthValue</span></span>

<span data-ttu-id="4e684-1029">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1029">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="4e684-1030">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1030">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="4e684-1031">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="4e684-1031">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="4e684-1032">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="4e684-1032">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="4e684-1033">メソッド left</span><span class="sxs-lookup"><span data-stu-id="4e684-1033">Method left</span></span>

<span data-ttu-id="4e684-1034">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1034">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="4e684-1035">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="4e684-1035">Parameters - left</span></span>

<span data-ttu-id="4e684-1036">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1036">value</span></span>  
<span data-ttu-id="4e684-1037">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1037">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="4e684-1038">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1038">mode</span></span>  
<span data-ttu-id="4e684-1039">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1039">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="4e684-1040">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="4e684-1040">Return Value - left</span></span>

<span data-ttu-id="4e684-1041">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="4e684-1041">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="4e684-1042">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1042">Method leftMode</span></span>

<span data-ttu-id="4e684-1043">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1043">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="4e684-1044">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1044">Parameters - leftMode</span></span>

<span data-ttu-id="4e684-1045">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1045">value</span></span>  
<span data-ttu-id="4e684-1046">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1046">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="4e684-1047">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1047">Return Value - leftMode</span></span>

<span data-ttu-id="4e684-1048">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-1048">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="4e684-1049">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1049">Method leftValue</span></span>

<span data-ttu-id="4e684-1050">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1050">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="4e684-1051">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1051">Parameters - leftValue</span></span>

<span data-ttu-id="4e684-1052">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1052">value</span></span>  
<span data-ttu-id="4e684-1053">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1053">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="4e684-1054">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1054">Return Value - leftValue</span></span>

<span data-ttu-id="4e684-1055">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="4e684-1055">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="4e684-1056">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="4e684-1056">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="4e684-1057">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="4e684-1057">Parameters - limitText</span></span>

<span data-ttu-id="4e684-1058">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1058">value</span></span>  

<!-- -->

<span data-ttu-id="4e684-1059">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1059">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="4e684-1060">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="4e684-1060">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="4e684-1061">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1061">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="4e684-1062">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1062">Parameters - limitTextMode</span></span>

<span data-ttu-id="4e684-1063">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1063">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="4e684-1064">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1064">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="4e684-1065">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1065">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="4e684-1066">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1066">Parameters - limitTextValue</span></span>

<span data-ttu-id="4e684-1067">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1067">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="4e684-1068">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1068">Return Value - limitTextValue</span></span>

## <a name="method-linefromchar"></a><span data-ttu-id="4e684-1069">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="4e684-1069">Method lineFromChar</span></span>

```xpp
public int lineFromChar(int charIndex)
```

### <a name="parameters---linefromchar"></a><span data-ttu-id="4e684-1070">パラメーター - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="4e684-1070">Parameters - lineFromChar</span></span>

<span data-ttu-id="4e684-1071">charIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-1071">charIndex</span></span>  

### <a name="return-value---linefromchar"></a><span data-ttu-id="4e684-1072">戻り値 - lineFromChar</span><span class="sxs-lookup"><span data-stu-id="4e684-1072">Return Value - lineFromChar</span></span>

## <a name="method-lineindex"></a><span data-ttu-id="4e684-1073">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-1073">Method lineIndex</span></span>

```xpp
public int lineIndex(int lineNo)
```

### <a name="parameters---lineindex"></a><span data-ttu-id="4e684-1074">パラメーター - lineIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-1074">Parameters - lineIndex</span></span>

<span data-ttu-id="4e684-1075">lineNo</span><span class="sxs-lookup"><span data-stu-id="4e684-1075">lineNo</span></span>  

### <a name="return-value---lineindex"></a><span data-ttu-id="4e684-1076">戻り値 - lineIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-1076">Return Value - lineIndex</span></span>

## <a name="method-linelength"></a><span data-ttu-id="4e684-1077">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="4e684-1077">Method lineLength</span></span>

```xpp
public int lineLength(int lineNo)
```

### <a name="parameters---linelength"></a><span data-ttu-id="4e684-1078">パラメーター - lineLength</span><span class="sxs-lookup"><span data-stu-id="4e684-1078">Parameters - lineLength</span></span>

<span data-ttu-id="4e684-1079">lineNo</span><span class="sxs-lookup"><span data-stu-id="4e684-1079">lineNo</span></span>  

### <a name="return-value---linelength"></a><span data-ttu-id="4e684-1080">戻り値 - lineLength</span><span class="sxs-lookup"><span data-stu-id="4e684-1080">Return Value - lineLength</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="4e684-1081">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="4e684-1081">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="4e684-1082">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="4e684-1082">Parameters - lookupButton</span></span>

<span data-ttu-id="4e684-1083">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1083">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="4e684-1084">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="4e684-1084">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="4e684-1085">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="4e684-1085">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="4e684-1086">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="4e684-1086">Parameters - mandatory</span></span>

<span data-ttu-id="4e684-1087">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1087">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="4e684-1088">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="4e684-1088">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="4e684-1089">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="4e684-1089">Method markAsUserAdd</span></span>

<span data-ttu-id="4e684-1090">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="4e684-1090">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="4e684-1091">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="4e684-1091">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="4e684-1092">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1092">value</span></span>  
<span data-ttu-id="4e684-1093">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1093">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="4e684-1094">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="4e684-1094">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="4e684-1095">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-1095">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-maxdatelabel"></a><span data-ttu-id="4e684-1096">メソッド maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="4e684-1096">Method maxDateLabel</span></span>

```xpp
public str maxDateLabel([str value])
```

### <a name="parameters---maxdatelabel"></a><span data-ttu-id="4e684-1097">パラメーター - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="4e684-1097">Parameters - maxDateLabel</span></span>

<span data-ttu-id="4e684-1098">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1098">value</span></span>  

### <a name="return-value---maxdatelabel"></a><span data-ttu-id="4e684-1099">戻り値 - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="4e684-1099">Return Value - maxDateLabel</span></span>

## <a name="method-maxdatelabeltext"></a><span data-ttu-id="4e684-1100">メソッド maxDateLabelText</span><span class="sxs-lookup"><span data-stu-id="4e684-1100">Method maxDateLabelText</span></span>

```xpp
public str maxDateLabelText()
```

### <a name="return-value---maxdatelabeltext"></a><span data-ttu-id="4e684-1101">戻り値 - maxDateLabelText</span><span class="sxs-lookup"><span data-stu-id="4e684-1101">Return Value - maxDateLabelText</span></span>

## <a name="method-modified"></a><span data-ttu-id="4e684-1102">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="4e684-1102">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="4e684-1103">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="4e684-1103">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="4e684-1104">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="4e684-1104">Method mouseDblClick</span></span>

<span data-ttu-id="4e684-1105">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1105">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="4e684-1106">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="4e684-1106">Parameters - mouseDblClick</span></span>

<span data-ttu-id="4e684-1107">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1107">x</span></span>  
<span data-ttu-id="4e684-1108">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1108">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1109">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1109">y</span></span>  
<span data-ttu-id="4e684-1110">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1110">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1111">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-1111">button</span></span>  
<span data-ttu-id="4e684-1112">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1112">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1113">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-1113">Ctrl</span></span>  
<span data-ttu-id="4e684-1114">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1114">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1115">シフト</span><span class="sxs-lookup"><span data-stu-id="4e684-1115">Shift</span></span>  
<span data-ttu-id="4e684-1116">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1116">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="4e684-1117">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="4e684-1117">Return Value - mouseDblClick</span></span>

<span data-ttu-id="4e684-1118">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1118">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="4e684-1119">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="4e684-1119">Remarks - mouseDblClick</span></span>

<span data-ttu-id="4e684-1120">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1120">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="4e684-1121">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="4e684-1121">Method mouseDown</span></span>

<span data-ttu-id="4e684-1122">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1122">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="4e684-1123">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="4e684-1123">Parameters - mouseDown</span></span>

<span data-ttu-id="4e684-1124">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1124">x</span></span>  
<span data-ttu-id="4e684-1125">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1125">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1126">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1126">y</span></span>  
<span data-ttu-id="4e684-1127">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1127">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1128">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-1128">button</span></span>  
<span data-ttu-id="4e684-1129">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1129">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1130">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-1130">Ctrl</span></span>  
<span data-ttu-id="4e684-1131">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1131">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1132">シフト</span><span class="sxs-lookup"><span data-stu-id="4e684-1132">Shift</span></span>  
<span data-ttu-id="4e684-1133">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1133">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="4e684-1134">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="4e684-1134">Return Value - mouseDown</span></span>

<span data-ttu-id="4e684-1135">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1135">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="4e684-1136">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="4e684-1136">Remarks - mouseDown</span></span>

<span data-ttu-id="4e684-1137">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1137">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="4e684-1138">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1138">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="4e684-1139">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="4e684-1139">Method mouseMove</span></span>

<span data-ttu-id="4e684-1140">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1140">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="4e684-1141">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="4e684-1141">Parameters - mouseMove</span></span>

<span data-ttu-id="4e684-1142">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1142">x</span></span>  
<span data-ttu-id="4e684-1143">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1143">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1144">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1144">y</span></span>  
<span data-ttu-id="4e684-1145">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1145">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1146">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-1146">button</span></span>  
<span data-ttu-id="4e684-1147">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1147">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1148">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-1148">Ctrl</span></span>  
<span data-ttu-id="4e684-1149">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1149">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1150">シフト</span><span class="sxs-lookup"><span data-stu-id="4e684-1150">Shift</span></span>  
<span data-ttu-id="4e684-1151">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1151">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="4e684-1152">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="4e684-1152">Return Value - mouseMove</span></span>

<span data-ttu-id="4e684-1153">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1153">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="4e684-1154">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="4e684-1154">Remarks - mouseMove</span></span>

<span data-ttu-id="4e684-1155">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1155">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="4e684-1156">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="4e684-1156">Method mouseUp</span></span>

<span data-ttu-id="4e684-1157">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1157">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="4e684-1158">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="4e684-1158">Parameters - mouseUp</span></span>

<span data-ttu-id="4e684-1159">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1159">x</span></span>  
<span data-ttu-id="4e684-1160">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1160">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1161">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1161">y</span></span>  
<span data-ttu-id="4e684-1162">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1162">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1163">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-1163">button</span></span>  
<span data-ttu-id="4e684-1164">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1164">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1165">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-1165">Ctrl</span></span>  
<span data-ttu-id="4e684-1166">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1166">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1167">シフト</span><span class="sxs-lookup"><span data-stu-id="4e684-1167">Shift</span></span>  
<span data-ttu-id="4e684-1168">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1168">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="4e684-1169">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="4e684-1169">Return Value - mouseUp</span></span>

<span data-ttu-id="4e684-1170">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1170">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="4e684-1171">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="4e684-1171">Remarks - mouseUp</span></span>

<span data-ttu-id="4e684-1172">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1172">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="4e684-1173">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1173">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="4e684-1174">メソッド名</span><span class="sxs-lookup"><span data-stu-id="4e684-1174">Method name</span></span>

<span data-ttu-id="4e684-1175">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1175">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="4e684-1176">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="4e684-1176">Parameters - name</span></span>

<span data-ttu-id="4e684-1177">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1177">value</span></span>  
<span data-ttu-id="4e684-1178">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1178">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="4e684-1179">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="4e684-1179">Return Value - name</span></span>

<span data-ttu-id="4e684-1180">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="4e684-1180">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="4e684-1181">備考 - name</span><span class="sxs-lookup"><span data-stu-id="4e684-1181">Remarks - name</span></span>

<span data-ttu-id="4e684-1182">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e684-1182">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="4e684-1183">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e684-1183">It must start with a letter.</span></span>
-   <span data-ttu-id="4e684-1184">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="4e684-1184">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="4e684-1185">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1185">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="4e684-1186">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="4e684-1186">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="4e684-1187">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="4e684-1187">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="4e684-1188">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="4e684-1188">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="4e684-1189">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="4e684-1189">Parameters - neededPermission</span></span>

<span data-ttu-id="4e684-1190">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1190">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="4e684-1191">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="4e684-1191">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="4e684-1192">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="4e684-1192">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="4e684-1193">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="4e684-1193">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="4e684-1194">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="4e684-1194">Method parentControl</span></span>

<span data-ttu-id="4e684-1195">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1195">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="4e684-1196">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="4e684-1196">Return Value - parentControl</span></span>

<span data-ttu-id="4e684-1197">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="4e684-1197">The parent control for the control.</span></span>

## <a name="method-posfromchar"></a><span data-ttu-id="4e684-1198">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="4e684-1198">Method posFromChar</span></span>

```xpp
public container posFromChar(int charIndex)
```

### <a name="parameters---posfromchar"></a><span data-ttu-id="4e684-1199">パラメーター - posFromChar</span><span class="sxs-lookup"><span data-stu-id="4e684-1199">Parameters - posFromChar</span></span>

<span data-ttu-id="4e684-1200">charIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-1200">charIndex</span></span>  

### <a name="return-value---posfromchar"></a><span data-ttu-id="4e684-1201">戻り値 - posFromChar</span><span class="sxs-lookup"><span data-stu-id="4e684-1201">Return Value - posFromChar</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="4e684-1202">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="4e684-1202">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="4e684-1203">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="4e684-1203">Parameters - previewPartRef</span></span>

<span data-ttu-id="4e684-1204">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1204">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="4e684-1205">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="4e684-1205">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="4e684-1206">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="4e684-1206">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="4e684-1207">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="4e684-1207">Parameters - promptrect</span></span>

<span data-ttu-id="4e684-1208">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1208">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="4e684-1209">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="4e684-1209">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="4e684-1210">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1210">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="4e684-1211">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1211">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="4e684-1212">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1212">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="4e684-1213">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1213">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="4e684-1214">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="4e684-1214">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="4e684-1215">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="4e684-1215">Parameters - searchAfterInput</span></span>

<span data-ttu-id="4e684-1216">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1216">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="4e684-1217">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="4e684-1217">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="4e684-1218">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1218">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="4e684-1219">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1219">Parameters - searchMode</span></span>

<span data-ttu-id="4e684-1220">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1220">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="4e684-1221">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1221">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="4e684-1222">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="4e684-1222">Method securityKey</span></span>

<span data-ttu-id="4e684-1223">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1223">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="4e684-1224">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="4e684-1224">Parameters - securityKey</span></span>

<span data-ttu-id="4e684-1225">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1225">value</span></span>  
<span data-ttu-id="4e684-1226">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1226">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="4e684-1227">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="4e684-1227">Return Value - securityKey</span></span>

<span data-ttu-id="4e684-1228">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1228">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="4e684-1229">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="4e684-1229">Method showContextMenu</span></span>

<span data-ttu-id="4e684-1230">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1230">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="4e684-1231">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="4e684-1231">Parameters - showContextMenu</span></span>

<span data-ttu-id="4e684-1232">menuHandle</span><span class="sxs-lookup"><span data-stu-id="4e684-1232">menuHandle</span></span>  
<span data-ttu-id="4e684-1233">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="4e684-1233">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="4e684-1234">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="4e684-1234">Return Value - showContextMenu</span></span>

<span data-ttu-id="4e684-1235">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1235">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="4e684-1236">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="4e684-1236">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="4e684-1237">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="4e684-1237">Parameters - showLabel</span></span>

<span data-ttu-id="4e684-1238">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1238">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="4e684-1239">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="4e684-1239">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="4e684-1240">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="4e684-1240">Method skip</span></span>

<span data-ttu-id="4e684-1241">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1241">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="4e684-1242">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="4e684-1242">Parameters - skip</span></span>

<span data-ttu-id="4e684-1243">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1243">value</span></span>  
<span data-ttu-id="4e684-1244">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1244">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="4e684-1245">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="4e684-1245">Return Value - skip</span></span>

<span data-ttu-id="4e684-1246">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-1246">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="4e684-1247">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="4e684-1247">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="4e684-1248">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="4e684-1248">Parameters - sort</span></span>

<span data-ttu-id="4e684-1249">sortDirection</span><span class="sxs-lookup"><span data-stu-id="4e684-1249">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="4e684-1250">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="4e684-1250">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="4e684-1251">メソッド style</span><span class="sxs-lookup"><span data-stu-id="4e684-1251">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="4e684-1252">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="4e684-1252">Parameters - style</span></span>

<span data-ttu-id="4e684-1253">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1253">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="4e684-1254">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="4e684-1254">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="4e684-1255">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="4e684-1255">Method toolTip</span></span>

<span data-ttu-id="4e684-1256">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1256">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="4e684-1257">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="4e684-1257">Return Value - toolTip</span></span>

<span data-ttu-id="4e684-1258">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="4e684-1258">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="4e684-1259">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="4e684-1259">Remarks - toolTip</span></span>

<span data-ttu-id="4e684-1260">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1260">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="4e684-1261">メソッド top</span><span class="sxs-lookup"><span data-stu-id="4e684-1261">Method top</span></span>

<span data-ttu-id="4e684-1262">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1262">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="4e684-1263">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="4e684-1263">Parameters - top</span></span>

<span data-ttu-id="4e684-1264">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1264">value</span></span>  
<span data-ttu-id="4e684-1265">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1265">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="4e684-1266">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1266">mode</span></span>  
<span data-ttu-id="4e684-1267">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1267">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="4e684-1268">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="4e684-1268">Return Value - top</span></span>

<span data-ttu-id="4e684-1269">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="4e684-1269">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="4e684-1270">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1270">Method topMode</span></span>

<span data-ttu-id="4e684-1271">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1271">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="4e684-1272">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1272">Parameters - topMode</span></span>

<span data-ttu-id="4e684-1273">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1273">value</span></span>  
<span data-ttu-id="4e684-1274">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1274">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="4e684-1275">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1275">Return Value - topMode</span></span>

<span data-ttu-id="4e684-1276">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-1276">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="4e684-1277">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1277">Method topValue</span></span>

<span data-ttu-id="4e684-1278">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1278">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="4e684-1279">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1279">Parameters - topValue</span></span>

<span data-ttu-id="4e684-1280">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1280">value</span></span>  
<span data-ttu-id="4e684-1281">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1281">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="4e684-1282">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1282">Return Value - topValue</span></span>

<span data-ttu-id="4e684-1283">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="4e684-1283">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="4e684-1284">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="4e684-1284">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="4e684-1285">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="4e684-1285">Parameters - type</span></span>

<span data-ttu-id="4e684-1286">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1286">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="4e684-1287">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="4e684-1287">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="4e684-1288">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="4e684-1288">Method underline</span></span>

<span data-ttu-id="4e684-1289">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1289">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="4e684-1290">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="4e684-1290">Parameters - underline</span></span>

<span data-ttu-id="4e684-1291">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1291">value</span></span>  
<span data-ttu-id="4e684-1292">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1292">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="4e684-1293">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="4e684-1293">Return Value - underline</span></span>

<span data-ttu-id="4e684-1294">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4e684-1294">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="4e684-1295">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="4e684-1295">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="4e684-1296">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="4e684-1296">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="4e684-1297">データ</span><span class="sxs-lookup"><span data-stu-id="4e684-1297">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="4e684-1298">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="4e684-1298">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="4e684-1299">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="4e684-1299">Method userData</span></span>

<span data-ttu-id="4e684-1300">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1300">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="4e684-1301">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="4e684-1301">Parameters - userData</span></span>

<span data-ttu-id="4e684-1302">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1302">value</span></span>  
<span data-ttu-id="4e684-1303">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1303">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="4e684-1304">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="4e684-1304">Return Value - userData</span></span>

<span data-ttu-id="4e684-1305">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="4e684-1305">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="4e684-1306">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="4e684-1306">Method userDataItem</span></span>

<span data-ttu-id="4e684-1307">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1307">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="4e684-1308">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="4e684-1308">Parameters - userDataItem</span></span>

<span data-ttu-id="4e684-1309">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1309">value</span></span>  
<span data-ttu-id="4e684-1310">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1310">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="4e684-1311">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="4e684-1311">Return Value - userDataItem</span></span>

<span data-ttu-id="4e684-1312">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="4e684-1312">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="4e684-1313">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="4e684-1313">Method userDataItems</span></span>

<span data-ttu-id="4e684-1314">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1314">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="4e684-1315">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="4e684-1315">Parameters - userDataItems</span></span>

<span data-ttu-id="4e684-1316">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1316">value</span></span>  
<span data-ttu-id="4e684-1317">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1317">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="4e684-1318">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="4e684-1318">Return Value - userDataItems</span></span>

<span data-ttu-id="4e684-1319">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="4e684-1319">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="4e684-1320">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="4e684-1320">Method userDisable</span></span>

<span data-ttu-id="4e684-1321">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1321">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="4e684-1322">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="4e684-1322">Parameters - userDisable</span></span>

<span data-ttu-id="4e684-1323">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1323">value</span></span>  
<span data-ttu-id="4e684-1324">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1324">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="4e684-1325">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="4e684-1325">Return Value - userDisable</span></span>

<span data-ttu-id="4e684-1326">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1326">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="4e684-1327">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="4e684-1327">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="4e684-1328">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="4e684-1328">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="4e684-1329">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1329">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="4e684-1330">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="4e684-1330">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="4e684-1331">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-1331">Method userHeight</span></span>

<span data-ttu-id="4e684-1332">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1332">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="4e684-1333">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-1333">Parameters - userHeight</span></span>

<span data-ttu-id="4e684-1334">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1334">value</span></span>  
<span data-ttu-id="4e684-1335">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1335">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="4e684-1336">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="4e684-1336">Return Value - userHeight</span></span>

<span data-ttu-id="4e684-1337">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="4e684-1337">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="4e684-1338">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="4e684-1338">Method userHide</span></span>

<span data-ttu-id="4e684-1339">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1339">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="4e684-1340">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="4e684-1340">Parameters - userHide</span></span>

<span data-ttu-id="4e684-1341">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1341">value</span></span>  
<span data-ttu-id="4e684-1342">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1342">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="4e684-1343">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="4e684-1343">Return Value - userHide</span></span>

<span data-ttu-id="4e684-1344">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1344">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="4e684-1345">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="4e684-1345">Remarks - userHide</span></span>

<span data-ttu-id="4e684-1346">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1346">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="4e684-1347">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1347">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="4e684-1348">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1348">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="4e684-1349">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="4e684-1349">Method userOrgContainer</span></span>

<span data-ttu-id="4e684-1350">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1350">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="4e684-1351">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="4e684-1351">Parameters - userOrgContainer</span></span>

<span data-ttu-id="4e684-1352">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1352">value</span></span>  
<span data-ttu-id="4e684-1353">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1353">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="4e684-1354">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="4e684-1354">Return Value - userOrgContainer</span></span>

<span data-ttu-id="4e684-1355">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="4e684-1355">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="4e684-1356">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="4e684-1356">Method userOrgSibling</span></span>

<span data-ttu-id="4e684-1357">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1357">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="4e684-1358">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="4e684-1358">Parameters - userOrgSibling</span></span>

<span data-ttu-id="4e684-1359">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1359">value</span></span>  
<span data-ttu-id="4e684-1360">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1360">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="4e684-1361">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="4e684-1361">Return Value - userOrgSibling</span></span>

<span data-ttu-id="4e684-1362">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="4e684-1362">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="4e684-1363">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="4e684-1363">Method userPromptText</span></span>

<span data-ttu-id="4e684-1364">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1364">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="4e684-1365">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="4e684-1365">Parameters - userPromptText</span></span>

<span data-ttu-id="4e684-1366">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1366">value</span></span>  
<span data-ttu-id="4e684-1367">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1367">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="4e684-1368">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="4e684-1368">Return Value - userPromptText</span></span>

<span data-ttu-id="4e684-1369">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="4e684-1369">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="4e684-1370">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="4e684-1370">Method userSecurityLevel</span></span>

<span data-ttu-id="4e684-1371">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1371">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="4e684-1372">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="4e684-1372">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="4e684-1373">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1373">value</span></span>  
<span data-ttu-id="4e684-1374">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1374">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="4e684-1375">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="4e684-1375">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="4e684-1376">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="4e684-1376">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="4e684-1377">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="4e684-1377">Method userSkip</span></span>

<span data-ttu-id="4e684-1378">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1378">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="4e684-1379">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="4e684-1379">Parameters - userSkip</span></span>

<span data-ttu-id="4e684-1380">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1380">value</span></span>  
<span data-ttu-id="4e684-1381">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1381">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="4e684-1382">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1382">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="4e684-1383">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="4e684-1383">Return Value - userSkip</span></span>

<span data-ttu-id="4e684-1384">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="4e684-1384">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="4e684-1385">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="4e684-1385">Method userWidth</span></span>

<span data-ttu-id="4e684-1386">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1386">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="4e684-1387">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="4e684-1387">Parameters - userWidth</span></span>

<span data-ttu-id="4e684-1388">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1388">value</span></span>  
<span data-ttu-id="4e684-1389">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1389">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="4e684-1390">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="4e684-1390">Return Value - userWidth</span></span>

<span data-ttu-id="4e684-1391">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1391">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="4e684-1392">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="4e684-1392">Remarks - userWidth</span></span>

<span data-ttu-id="4e684-1393">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1393">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="4e684-1394">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="4e684-1394">For example, if the user has specified 30 characters as the width for the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="4e684-1395">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1395">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="4e684-1396">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="4e684-1396">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="4e684-1397">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="4e684-1397">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="4e684-1398">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="4e684-1398">Method verticalSpacing</span></span>

<span data-ttu-id="4e684-1399">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1399">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="4e684-1400">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="4e684-1400">Parameters - verticalSpacing</span></span>

<span data-ttu-id="4e684-1401">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1401">value</span></span>  
<span data-ttu-id="4e684-1402">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1402">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="4e684-1403">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1403">mode</span></span>  
<span data-ttu-id="4e684-1404">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1404">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="4e684-1405">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="4e684-1405">Return Value - verticalSpacing</span></span>

<span data-ttu-id="4e684-1406">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="4e684-1406">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="4e684-1407">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1407">Method verticalSpacingMode</span></span>

<span data-ttu-id="4e684-1408">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1408">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="4e684-1409">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1409">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="4e684-1410">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1410">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="4e684-1411">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1411">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="4e684-1412">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-1412">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="4e684-1413">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1413">Method verticalSpacingValue</span></span>

<span data-ttu-id="4e684-1414">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1414">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="4e684-1415">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1415">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="4e684-1416">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1416">value</span></span>  
<span data-ttu-id="4e684-1417">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="4e684-1417">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="4e684-1418">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1418">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="4e684-1419">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="4e684-1419">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="4e684-1420">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1420">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="4e684-1421">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1421">Parameters - viewEditMode</span></span>

<span data-ttu-id="4e684-1422">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1422">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="4e684-1423">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1423">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="4e684-1424">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="4e684-1424">Method visible</span></span>

<span data-ttu-id="4e684-1425">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1425">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="4e684-1426">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="4e684-1426">Parameters - visible</span></span>

<span data-ttu-id="4e684-1427">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1427">value</span></span>  
<span data-ttu-id="4e684-1428">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1428">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="4e684-1429">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="4e684-1429">Return Value - visible</span></span>

<span data-ttu-id="4e684-1430">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="4e684-1430">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="4e684-1431">メソッド width</span><span class="sxs-lookup"><span data-stu-id="4e684-1431">Method width</span></span>

<span data-ttu-id="4e684-1432">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1432">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="4e684-1433">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="4e684-1433">Parameters - width</span></span>

<span data-ttu-id="4e684-1434">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1434">value</span></span>  

<!-- -->

<span data-ttu-id="4e684-1435">モード</span><span class="sxs-lookup"><span data-stu-id="4e684-1435">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="4e684-1436">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="4e684-1436">Return Value - width</span></span>

<span data-ttu-id="4e684-1437">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="4e684-1437">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="4e684-1438">備考 - width</span><span class="sxs-lookup"><span data-stu-id="4e684-1438">Remarks - width</span></span>

<span data-ttu-id="4e684-1439">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1439">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="4e684-1440">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="4e684-1440">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="4e684-1441">モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-1441">Mode.</span></span>           | <span data-ttu-id="4e684-1442">幅計算。</span><span class="sxs-lookup"><span data-stu-id="4e684-1442">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e684-1443">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="4e684-1443">-1 Exact.</span></span>       | <span data-ttu-id="4e684-1444">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1444">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4e684-1445">0 自動。</span><span class="sxs-lookup"><span data-stu-id="4e684-1445">0 Auto.</span></span>         | <span data-ttu-id="4e684-1446">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1446">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4e684-1447">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="4e684-1447">1 Column width.</span></span> | <span data-ttu-id="4e684-1448">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="4e684-1448">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="4e684-1449">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1449">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="4e684-1450">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1450">Method widthMode</span></span>

<span data-ttu-id="4e684-1451">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1451">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="4e684-1452">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1452">Parameters - widthMode</span></span>

<span data-ttu-id="4e684-1453">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1453">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="4e684-1454">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1454">Return Value - widthMode</span></span>

<span data-ttu-id="4e684-1455">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1455">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="4e684-1456">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1456">Remarks - widthMode</span></span>

<span data-ttu-id="4e684-1457">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="4e684-1457">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="4e684-1458">モード。</span><span class="sxs-lookup"><span data-stu-id="4e684-1458">Mode.</span></span>         | <span data-ttu-id="4e684-1459">幅計算。</span><span class="sxs-lookup"><span data-stu-id="4e684-1459">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e684-1460">正確。</span><span class="sxs-lookup"><span data-stu-id="4e684-1460">Exact.</span></span>        | <span data-ttu-id="4e684-1461">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1461">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4e684-1462">自動。</span><span class="sxs-lookup"><span data-stu-id="4e684-1462">Auto.</span></span>         | <span data-ttu-id="4e684-1463">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1463">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4e684-1464">列の幅。</span><span class="sxs-lookup"><span data-stu-id="4e684-1464">Column width.</span></span> | <span data-ttu-id="4e684-1465">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="4e684-1465">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="4e684-1466">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="4e684-1466">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="4e684-1467">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1467">Method widthValue</span></span>

<span data-ttu-id="4e684-1468">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1468">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="4e684-1469">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1469">Parameters - widthValue</span></span>

<span data-ttu-id="4e684-1470">値</span><span class="sxs-lookup"><span data-stu-id="4e684-1470">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="4e684-1471">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1471">Return Value - widthValue</span></span>

<span data-ttu-id="4e684-1472">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="4e684-1472">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="4e684-1473">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="4e684-1473">Remarks - widthValue</span></span>

<span data-ttu-id="4e684-1474">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1474">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="4e684-1475">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="4e684-1475">Method dragLeave</span></span>

<span data-ttu-id="4e684-1476">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1476">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-cut"></a><span data-ttu-id="4e684-1477">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="4e684-1477">Method cut</span></span>

<span data-ttu-id="4e684-1478">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="4e684-1478">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="4e684-1479">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="4e684-1479">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="4e684-1480">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="4e684-1480">Parameters - OnLostFocus</span></span>

<span data-ttu-id="4e684-1481">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1481">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1482">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1482">e</span></span>  

## <a name="method-scrollcursor"></a><span data-ttu-id="4e684-1483">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="4e684-1483">Method scrollCursor</span></span>

```xpp
public void scrollCursor()
```

## <a name="method-mouseenter"></a><span data-ttu-id="4e684-1484">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="4e684-1484">Method mouseEnter</span></span>

<span data-ttu-id="4e684-1485">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1485">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="4e684-1486">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="4e684-1486">Parameters - mouseEnter</span></span>

<span data-ttu-id="4e684-1487">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1487">x</span></span>  
<span data-ttu-id="4e684-1488">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1488">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1489">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1489">y</span></span>  
<span data-ttu-id="4e684-1490">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1490">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1491">ボタン</span><span class="sxs-lookup"><span data-stu-id="4e684-1491">button</span></span>  
<span data-ttu-id="4e684-1492">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1492">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1493">Ctrl</span><span class="sxs-lookup"><span data-stu-id="4e684-1493">Ctrl</span></span>  
<span data-ttu-id="4e684-1494">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1494">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="4e684-1495">シフト</span><span class="sxs-lookup"><span data-stu-id="4e684-1495">Shift</span></span>  
<span data-ttu-id="4e684-1496">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1496">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-copy"></a><span data-ttu-id="4e684-1497">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="4e684-1497">Method copy</span></span>

<span data-ttu-id="4e684-1498">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="4e684-1498">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-gotfocus"></a><span data-ttu-id="4e684-1499">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="4e684-1499">Method gotFocus</span></span>

<span data-ttu-id="4e684-1500">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1500">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-onvalidating"></a><span data-ttu-id="4e684-1501">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="4e684-1501">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="4e684-1502">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="4e684-1502">Parameters - OnValidating</span></span>

<span data-ttu-id="4e684-1503">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1503">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1504">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1504">e</span></span>  

## <a name="method-performtypelookup"></a><span data-ttu-id="4e684-1505">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1505">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="4e684-1506">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1506">Parameters - performTypeLookup</span></span>

<span data-ttu-id="4e684-1507">userType</span><span class="sxs-lookup"><span data-stu-id="4e684-1507">userType</span></span>  

<!-- -->

<span data-ttu-id="4e684-1508">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="4e684-1508">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="4e684-1509">会社</span><span class="sxs-lookup"><span data-stu-id="4e684-1509">company</span></span>  

## <a name="method-linescroll"></a><span data-ttu-id="4e684-1510">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="4e684-1510">Method lineScroll</span></span>

```xpp
public void lineScroll(int dx, int dy)
```

### <a name="parameters---linescroll"></a><span data-ttu-id="4e684-1511">パラメーター - lineScroll</span><span class="sxs-lookup"><span data-stu-id="4e684-1511">Parameters - lineScroll</span></span>

<span data-ttu-id="4e684-1512">dx</span><span class="sxs-lookup"><span data-stu-id="4e684-1512">dx</span></span>  

<!-- -->

<span data-ttu-id="4e684-1513">dy</span><span class="sxs-lookup"><span data-stu-id="4e684-1513">dy</span></span>  

## <a name="method-setselection"></a><span data-ttu-id="4e684-1514">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="4e684-1514">Method setSelection</span></span>

```xpp
public void setSelection(int charIndexFrom, int charIndexTo)
```

### <a name="parameters---setselection"></a><span data-ttu-id="4e684-1515">パラメーター - setSelection</span><span class="sxs-lookup"><span data-stu-id="4e684-1515">Parameters - setSelection</span></span>

<span data-ttu-id="4e684-1516">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="4e684-1516">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="4e684-1517">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="4e684-1517">charIndexTo</span></span>  

## <a name="method-textchange"></a><span data-ttu-id="4e684-1518">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="4e684-1518">Method textChange</span></span>

```xpp
public void textChange()
```

## <a name="method-onenter"></a><span data-ttu-id="4e684-1519">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="4e684-1519">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="4e684-1520">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="4e684-1520">Parameters - OnEnter</span></span>

<span data-ttu-id="4e684-1521">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1521">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1522">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1522">e</span></span>  

## <a name="method-pastetext"></a><span data-ttu-id="4e684-1523">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="4e684-1523">Method pasteText</span></span>

```xpp
public void pasteText(str pasteStr, [boolean InsertSel])
```

### <a name="parameters---pastetext"></a><span data-ttu-id="4e684-1524">パラメーター - pasteText</span><span class="sxs-lookup"><span data-stu-id="4e684-1524">Parameters - pasteText</span></span>

<span data-ttu-id="4e684-1525">pasteStr</span><span class="sxs-lookup"><span data-stu-id="4e684-1525">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="4e684-1526">InsertSel</span><span class="sxs-lookup"><span data-stu-id="4e684-1526">InsertSel</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="4e684-1527">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="4e684-1527">Method lostFocus</span></span>

<span data-ttu-id="4e684-1528">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1528">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-jumpref"></a><span data-ttu-id="4e684-1529">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="4e684-1529">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onvalidated"></a><span data-ttu-id="4e684-1530">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="4e684-1530">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="4e684-1531">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="4e684-1531">Parameters - OnValidated</span></span>

<span data-ttu-id="4e684-1532">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1532">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1533">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1533">e</span></span>  

## <a name="method-onlookup"></a><span data-ttu-id="4e684-1534">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1534">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="4e684-1535">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1535">Parameters - OnLookup</span></span>

<span data-ttu-id="4e684-1536">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1536">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1537">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1537">e</span></span>  

## <a name="method-setcursorpos"></a><span data-ttu-id="4e684-1538">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="4e684-1538">Method setCursorPos</span></span>

```xpp
public void setCursorPos(int x, int y)
```

### <a name="parameters---setcursorpos"></a><span data-ttu-id="4e684-1539">パラメーター - setCursorPos</span><span class="sxs-lookup"><span data-stu-id="4e684-1539">Parameters - setCursorPos</span></span>

<span data-ttu-id="4e684-1540">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1540">x</span></span>  

<!-- -->

<span data-ttu-id="4e684-1541">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1541">y</span></span>  

## <a name="method-drop"></a><span data-ttu-id="4e684-1542">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="4e684-1542">Method drop</span></span>

<span data-ttu-id="4e684-1543">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1543">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="4e684-1544">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="4e684-1544">Parameters - drop</span></span>

<span data-ttu-id="4e684-1545">dragSource</span><span class="sxs-lookup"><span data-stu-id="4e684-1545">dragSource</span></span>  
<span data-ttu-id="4e684-1546">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1546">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-1547">dragMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1547">dragMode</span></span>  
<span data-ttu-id="4e684-1548">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1548">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-1549">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1549">x</span></span>  
<span data-ttu-id="4e684-1550">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1550">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-1551">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1551">y</span></span>  
<span data-ttu-id="4e684-1552">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1552">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="4e684-1553">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="4e684-1553">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="4e684-1554">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="4e684-1554">Parameters - OnLeaving</span></span>

<span data-ttu-id="4e684-1555">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1555">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1556">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1556">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="4e684-1557">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="4e684-1557">Method mouseLeave</span></span>

<span data-ttu-id="4e684-1558">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1558">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-performdblookup"></a><span data-ttu-id="4e684-1559">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1559">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="4e684-1560">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1560">Parameters - performDBLookup</span></span>

<span data-ttu-id="4e684-1561">fieldId</span><span class="sxs-lookup"><span data-stu-id="4e684-1561">fieldId</span></span>  

<!-- -->

<span data-ttu-id="4e684-1562">tableId</span><span class="sxs-lookup"><span data-stu-id="4e684-1562">tableId</span></span>  

<!-- -->

<span data-ttu-id="4e684-1563">会社</span><span class="sxs-lookup"><span data-stu-id="4e684-1563">company</span></span>  

## <a name="method-lookup"></a><span data-ttu-id="4e684-1564">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1564">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-enddrag"></a><span data-ttu-id="4e684-1565">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="4e684-1565">Method endDrag</span></span>

<span data-ttu-id="4e684-1566">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1566">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="4e684-1567">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="4e684-1567">Remarks - endDrag</span></span>

<span data-ttu-id="4e684-1568">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="4e684-1568">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="4e684-1569">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1569">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-undo"></a><span data-ttu-id="4e684-1570">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="4e684-1570">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-context"></a><span data-ttu-id="4e684-1571">メソッド context</span><span class="sxs-lookup"><span data-stu-id="4e684-1571">Method context</span></span>

<span data-ttu-id="4e684-1572">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1572">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="4e684-1573">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="4e684-1573">Method resetUserSetting</span></span>

<span data-ttu-id="4e684-1574">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="4e684-1574">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="4e684-1575">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="4e684-1575">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="4e684-1576">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="4e684-1576">Parameters - OnGotFocus</span></span>

<span data-ttu-id="4e684-1577">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1577">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1578">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1578">e</span></span>  

## <a name="method-paste"></a><span data-ttu-id="4e684-1579">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="4e684-1579">Method paste</span></span>

<span data-ttu-id="4e684-1580">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1580">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-onmodified"></a><span data-ttu-id="4e684-1581">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="4e684-1581">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="4e684-1582">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="4e684-1582">Parameters - OnModified</span></span>

<span data-ttu-id="4e684-1583">sender</span><span class="sxs-lookup"><span data-stu-id="4e684-1583">sender</span></span>  

<!-- -->

<span data-ttu-id="4e684-1584">e</span><span class="sxs-lookup"><span data-stu-id="4e684-1584">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="4e684-1585">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="4e684-1585">Method dropEx</span></span>

<span data-ttu-id="4e684-1586">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="4e684-1586">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="4e684-1587">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="4e684-1587">Parameters - dropEx</span></span>

<span data-ttu-id="4e684-1588">dragSource</span><span class="sxs-lookup"><span data-stu-id="4e684-1588">dragSource</span></span>  
<span data-ttu-id="4e684-1589">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1589">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-1590">dragMode</span><span class="sxs-lookup"><span data-stu-id="4e684-1590">dragMode</span></span>  
<span data-ttu-id="4e684-1591">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1591">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-1592">x</span><span class="sxs-lookup"><span data-stu-id="4e684-1592">x</span></span>  
<span data-ttu-id="4e684-1593">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1593">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="4e684-1594">y</span><span class="sxs-lookup"><span data-stu-id="4e684-1594">y</span></span>  
<span data-ttu-id="4e684-1595">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4e684-1595">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="4e684-1596">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="4e684-1596">Method setFocus</span></span>

<span data-ttu-id="4e684-1597">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1597">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="4e684-1598">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="4e684-1598">Method prefColumnSize</span></span>

<span data-ttu-id="4e684-1599">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1599">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="4e684-1600">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="4e684-1600">Parameters - prefColumnSize</span></span>

<span data-ttu-id="4e684-1601">width</span><span class="sxs-lookup"><span data-stu-id="4e684-1601">width</span></span>  
<span data-ttu-id="4e684-1602">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="4e684-1602">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="4e684-1603">height</span><span class="sxs-lookup"><span data-stu-id="4e684-1603">height</span></span>  
<span data-ttu-id="4e684-1604">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="4e684-1604">The preferred height of the control.</span></span>

## <a name="method-enter"></a><span data-ttu-id="4e684-1605">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="4e684-1605">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-filter"></a><span data-ttu-id="4e684-1606">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="4e684-1606">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="4e684-1607">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="4e684-1607">Parameters - filter</span></span>

<span data-ttu-id="4e684-1608">filterStr</span><span class="sxs-lookup"><span data-stu-id="4e684-1608">filterStr</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="4e684-1609">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="4e684-1609">Method inputSearch</span></span>

<span data-ttu-id="4e684-1610">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1610">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="4e684-1611">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="4e684-1611">Parameters - inputSearch</span></span>

<span data-ttu-id="4e684-1612">searchStr</span><span class="sxs-lookup"><span data-stu-id="4e684-1612">searchStr</span></span>  
<span data-ttu-id="4e684-1613">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4e684-1613">The string value to use to filter data; optional.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="4e684-1614">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-1614">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="4e684-1615">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="4e684-1615">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="4e684-1616">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="4e684-1616">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="4e684-1617">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="4e684-1617">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="4e684-1618">overrideObject</span><span class="sxs-lookup"><span data-stu-id="4e684-1618">overrideObject</span></span>  

## <a name="method-performformlookup"></a><span data-ttu-id="4e684-1619">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1619">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="4e684-1620">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="4e684-1620">Parameters - performFormLookup</span></span>

<span data-ttu-id="4e684-1621">フォーム</span><span class="sxs-lookup"><span data-stu-id="4e684-1621">form</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="4e684-1622">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="4e684-1622">Method displayControl</span></span>

<span data-ttu-id="4e684-1623">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="4e684-1623">Displays the control.</span></span>

```xpp
public void displayControl()
```

