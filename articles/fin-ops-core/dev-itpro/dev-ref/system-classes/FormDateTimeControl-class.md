---
title: FormDateTimeControl クラス
description: このトピックでは、FormDateTimeControl クラスについて説明します。
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
ms.openlocfilehash: ed7bf4e2910aac92123f1f51e95d81c8d2e908f0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502630"
---
# <a name="class-formdatetimecontrol"></a><span data-ttu-id="ee3e0-103">クラス FormDateTimeControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-103">Class FormDateTimeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormDateTimeControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="ee3e0-104">備考</span><span class="sxs-lookup"><span data-stu-id="ee3e0-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="ee3e0-105">例</span><span class="sxs-lookup"><span data-stu-id="ee3e0-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ee3e0-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="ee3e0-106">Methods</span></span>

| <span data-ttu-id="ee3e0-107">方法</span><span class="sxs-lookup"><span data-stu-id="ee3e0-107">Method</span></span>                                                                                                      | <span data-ttu-id="ee3e0-108">説明</span><span class="sxs-lookup"><span data-stu-id="ee3e0-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e0-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="ee3e0-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ee3e0-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="ee3e0-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-113">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="ee3e0-114">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-114">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="ee3e0-115">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-115">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="ee3e0-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="ee3e0-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="ee3e0-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="ee3e0-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="ee3e0-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="ee3e0-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="ee3e0-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="ee3e0-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="ee3e0-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="ee3e0-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-126">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="ee3e0-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="ee3e0-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="ee3e0-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="ee3e0-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="ee3e0-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="ee3e0-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-133">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="ee3e0-134">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-134">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="ee3e0-135">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-135">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ee3e0-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="ee3e0-137">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-137">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="ee3e0-138">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-138">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="ee3e0-139">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-139">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="ee3e0-140">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-140">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="ee3e0-141">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-141">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="ee3e0-142">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-142">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-143">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-143">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-144">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-144">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-145">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-145">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="ee3e0-146">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-146">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="ee3e0-147">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-147">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="ee3e0-148">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-148">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="ee3e0-149">public int dateDay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-149">public int dateDay(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-150">public int dateFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-150">public int dateFormat(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-151">public int dateMonth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-151">public int dateMonth(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-152">public int dateSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-152">public int dateSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-153">public DateTime dateTimeValue(\[DateTime value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-153">public DateTime dateTimeValue(\[DateTime value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-154">public int dateYear(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-154">public int dateYear(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-155">public int displayOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-155">public int displayOption(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-156">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-156">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="ee3e0-157">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-157">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="ee3e0-158">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-158">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-159">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-159">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="ee3e0-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="ee3e0-161">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-161">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="ee3e0-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="ee3e0-163">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-163">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="ee3e0-164">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-164">public str dragText()</span></span>                                                                                       | <span data-ttu-id="ee3e0-165">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-165">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="ee3e0-166">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-166">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="ee3e0-167">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-167">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="ee3e0-168">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-168">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-169">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-169">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-170">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-170">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="ee3e0-171">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-171">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="ee3e0-172">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-172">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-173">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-173">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="ee3e0-174">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-174">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="ee3e0-175">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-175">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="ee3e0-176">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-176">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="ee3e0-177">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-177">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="ee3e0-178">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-178">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="ee3e0-179">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-179">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="ee3e0-180">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-180">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="ee3e0-181">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-181">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="ee3e0-182">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-182">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="ee3e0-183">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-183">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="ee3e0-184">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-184">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="ee3e0-185">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-185">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="ee3e0-186">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-186">public str helpField()</span></span>                                                                                      | <span data-ttu-id="ee3e0-187">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-187">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ee3e0-188">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-188">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-189">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-189">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="ee3e0-190">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-190">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="ee3e0-191">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-191">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="ee3e0-192">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-192">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="ee3e0-193">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-193">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ee3e0-194">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-194">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-195">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-195">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="ee3e0-196">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-196">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="ee3e0-197">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-197">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="ee3e0-198">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-198">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="ee3e0-199">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-199">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="ee3e0-200">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-200">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="ee3e0-201">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-201">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-202">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-202">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-203">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-203">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="ee3e0-204">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-204">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="ee3e0-205">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-205">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-206">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-206">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-207">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-207">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-208">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-208">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-209">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-209">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-210">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-210">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-211">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-211">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-212">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-212">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-213">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-213">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-214">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-214">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-215">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-215">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-216">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-216">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-217">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-217">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-218">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-218">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-219">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-219">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-220">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-220">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-221">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-221">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-222">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-222">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-223">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-223">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-224">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-224">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-225">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-225">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="ee3e0-226">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-226">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="ee3e0-227">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-227">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-228">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-228">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ee3e0-229">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-229">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="ee3e0-230">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-230">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="ee3e0-231">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-231">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-232">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-232">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-233">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-233">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-234">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-234">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-235">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-235">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-236">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-236">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="ee3e0-237">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-237">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="ee3e0-238">public str maxDateLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-238">public str maxDateLabel(\[str value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-239">public str maxDateLabelText()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-239">public str maxDateLabelText()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-240">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-240">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-241">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-241">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="ee3e0-242">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-242">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="ee3e0-243">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-243">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="ee3e0-244">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-244">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="ee3e0-245">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-245">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="ee3e0-246">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-246">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="ee3e0-247">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-247">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="ee3e0-248">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-248">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="ee3e0-249">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-249">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="ee3e0-250">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-250">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="ee3e0-251">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-251">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-252">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-252">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-253">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-253">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="ee3e0-254">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-254">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="ee3e0-255">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-255">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-256">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-256">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-257">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-257">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="ee3e0-258">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-258">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="ee3e0-259">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-259">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="ee3e0-260">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-260">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ee3e0-261">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-261">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-262">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-262">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="ee3e0-263">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-263">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="ee3e0-264">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-264">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-265">public int timeFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-265">public int timeFormat(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-266">public int timeHours(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-266">public int timeHours(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-267">public int timeMinute(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-267">public int timeMinute(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-268">public int timeSeconds(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-268">public int timeSeconds(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-269">public int timeSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-269">public int timeSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-270">public Timezone timeZone(\[Timezone timeZone\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-270">public Timezone timeZone(\[Timezone timeZone\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-271">public int timeZoneIndicator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-271">public int timeZoneIndicator(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-272">public int timezonePreference(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-272">public int timezonePreference(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-273">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-273">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="ee3e0-274">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-274">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="ee3e0-275">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-275">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="ee3e0-276">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-276">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="ee3e0-277">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-277">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="ee3e0-278">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-278">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="ee3e0-279">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-279">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-280">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-280">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="ee3e0-281">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-281">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-282">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-282">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-283">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-283">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-284">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-284">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-285">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-285">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="ee3e0-286">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-286">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="ee3e0-287">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-287">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="ee3e0-288">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-288">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="ee3e0-289">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-289">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="ee3e0-290">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-290">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="ee3e0-291">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-291">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="ee3e0-292">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-292">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-293">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-293">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="ee3e0-294">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-294">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="ee3e0-295">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-295">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-296">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-296">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="ee3e0-297">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-297">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="ee3e0-298">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-298">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="ee3e0-299">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-299">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="ee3e0-300">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-300">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ee3e0-301">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-301">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="ee3e0-302">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-302">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="ee3e0-303">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-303">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="ee3e0-304">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-304">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="ee3e0-305">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-305">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="ee3e0-306">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-306">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="ee3e0-307">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-307">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="ee3e0-308">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-308">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="ee3e0-309">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-309">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-310">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-310">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="ee3e0-311">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-311">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ee3e0-312">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-312">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="ee3e0-313">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-313">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="ee3e0-314">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-314">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="ee3e0-315">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-315">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="ee3e0-316">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-316">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-317">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-317">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="ee3e0-318">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-318">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="ee3e0-319">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-319">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="ee3e0-320">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-320">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="ee3e0-321">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-321">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="ee3e0-322">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-322">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="ee3e0-323">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-323">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="ee3e0-324">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-324">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="ee3e0-325">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-325">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="ee3e0-326">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-326">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="ee3e0-327">public void paste()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-327">public void paste()</span></span>                                                                                         | <span data-ttu-id="ee3e0-328">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-328">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ee3e0-329">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-329">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-330">public void copy()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-330">public void copy()</span></span>                                                                                          | <span data-ttu-id="ee3e0-331">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-331">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="ee3e0-332">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-332">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="ee3e0-333">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-333">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="ee3e0-334">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-334">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-335">public void cut()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-335">public void cut()</span></span>                                                                                           | <span data-ttu-id="ee3e0-336">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-336">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="ee3e0-337">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-337">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="ee3e0-338">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-338">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="ee3e0-339">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-339">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="ee3e0-340">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-340">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="ee3e0-341">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-341">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-342">public void timeTextChange()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-342">public void timeTextChange()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-343">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-343">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-344">public void dateTextChange()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-344">public void dateTextChange()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-345">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-345">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-346">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-346">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="ee3e0-347">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-347">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="ee3e0-348">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-348">public void displayControl()</span></span>                                                                                | <span data-ttu-id="ee3e0-349">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-349">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="ee3e0-350">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-350">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-351">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-351">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="ee3e0-352">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-352">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="ee3e0-353">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-353">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="ee3e0-354">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-354">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="ee3e0-355">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-355">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="ee3e0-356">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-356">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="ee3e0-357">public void enter()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-357">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-358">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-358">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="ee3e0-359">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-359">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="ee3e0-360">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-360">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="ee3e0-361">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-361">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="ee3e0-362">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-362">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-363">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-363">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-364">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-364">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-365">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-365">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-366">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-366">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-367">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-367">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-368">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-368">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="ee3e0-369">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-369">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="ee3e0-370">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-370">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="ee3e0-371">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-371">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="ee3e0-372">public void context()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-372">public void context()</span></span>                                                                                       | <span data-ttu-id="ee3e0-373">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-373">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="ee3e0-374">public void undo()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-374">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-375">public void setUTCString(str UTC\_Formatted String)</span><span class="sxs-lookup"><span data-stu-id="ee3e0-375">public void setUTCString(str UTC\_Formatted String)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-376">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-376">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-377">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="ee3e0-377">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="ee3e0-378">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="ee3e0-378">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="ee3e0-379">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-379">Method alignControl</span></span>

<span data-ttu-id="ee3e0-380">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-380">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="ee3e0-381">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-381">Parameters - alignControl</span></span>

<span data-ttu-id="ee3e0-382">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-382">value</span></span>  
<span data-ttu-id="ee3e0-383">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-383">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="ee3e0-384">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-384">Return Value - alignControl</span></span>

<span data-ttu-id="ee3e0-385">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-385">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="ee3e0-386">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-386">Remarks - alignControl</span></span>

<span data-ttu-id="ee3e0-387">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-387">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="ee3e0-388">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="ee3e0-388">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="ee3e0-389">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="ee3e0-389">Parameters - alignment</span></span>

<span data-ttu-id="ee3e0-390">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-390">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="ee3e0-391">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="ee3e0-391">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="ee3e0-392">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee3e0-392">Method allowEdit</span></span>

<span data-ttu-id="ee3e0-393">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-393">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="ee3e0-394">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee3e0-394">Parameters - allowEdit</span></span>

<span data-ttu-id="ee3e0-395">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-395">value</span></span>  
<span data-ttu-id="ee3e0-396">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-396">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="ee3e0-397">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee3e0-397">Return Value - allowEdit</span></span>

<span data-ttu-id="ee3e0-398">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-398">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="ee3e0-399">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ee3e0-399">Remarks - allowEdit</span></span>

<span data-ttu-id="ee3e0-400">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-400">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="ee3e0-401">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-401">Method allowSysSetup</span></span>

<span data-ttu-id="ee3e0-402">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-402">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="ee3e0-403">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-403">Return Value - allowSysSetup</span></span>

<span data-ttu-id="ee3e0-404">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-404">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="ee3e0-405">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ee3e0-405">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="ee3e0-406">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ee3e0-406">Parameters - arrayIndex</span></span>

<span data-ttu-id="ee3e0-407">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-407">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="ee3e0-408">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ee3e0-408">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="ee3e0-409">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee3e0-409">Method autoDeclaration</span></span>

<span data-ttu-id="ee3e0-410">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-410">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="ee3e0-411">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee3e0-411">Parameters - autoDeclaration</span></span>

<span data-ttu-id="ee3e0-412">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-412">value</span></span>  
<span data-ttu-id="ee3e0-413">プロパティはこの値に設定されます (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-413">The property is set to this value; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="ee3e0-414">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee3e0-414">Return Value - autoDeclaration</span></span>

<span data-ttu-id="ee3e0-415">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-415">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="ee3e0-416">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="ee3e0-416">Remarks - autoDeclaration</span></span>

<span data-ttu-id="ee3e0-417">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-417">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="ee3e0-418">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-418">Method backgroundColor</span></span>

<span data-ttu-id="ee3e0-419">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-419">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="ee3e0-420">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-420">Parameters - backgroundColor</span></span>

<span data-ttu-id="ee3e0-421">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-421">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="ee3e0-422">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-422">Return Value - backgroundColor</span></span>

<span data-ttu-id="ee3e0-423">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-423">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="ee3e0-424">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-424">Remarks - backgroundColor</span></span>

<span data-ttu-id="ee3e0-425">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-425">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="ee3e0-426">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-426">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="ee3e0-427">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-427">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="ee3e0-428">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-428">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="ee3e0-429">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-429">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="ee3e0-430">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-430">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="ee3e0-431">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="ee3e0-431">Method backStyle</span></span>

<span data-ttu-id="ee3e0-432">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-432">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="ee3e0-433">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="ee3e0-433">Parameters - backStyle</span></span>

<span data-ttu-id="ee3e0-434">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-434">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="ee3e0-435">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="ee3e0-435">Return Value - backStyle</span></span>

<span data-ttu-id="ee3e0-436">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-436">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="ee3e0-437">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="ee3e0-437">Method beginDrag</span></span>

<span data-ttu-id="ee3e0-438">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-438">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="ee3e0-439">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ee3e0-439">Parameters - beginDrag</span></span>

<span data-ttu-id="ee3e0-440">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-440">x</span></span>  
<span data-ttu-id="ee3e0-441">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-441">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="ee3e0-442">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-442">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-443">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-443">y</span></span>  
<span data-ttu-id="ee3e0-444">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-444">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="ee3e0-445">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-445">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="ee3e0-446">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ee3e0-446">Return Value - beginDrag</span></span>

<span data-ttu-id="ee3e0-447">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-447">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="ee3e0-448">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="ee3e0-448">Remarks - beginDrag</span></span>

<span data-ttu-id="ee3e0-449">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-449">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="ee3e0-450">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-450">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="ee3e0-451">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="ee3e0-451">Method bold</span></span>

<span data-ttu-id="ee3e0-452">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-452">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="ee3e0-453">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="ee3e0-453">Parameters - bold</span></span>

<span data-ttu-id="ee3e0-454">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-454">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="ee3e0-455">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="ee3e0-455">Return Value - bold</span></span>

<span data-ttu-id="ee3e0-456">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-456">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="ee3e0-457">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="ee3e0-457">Remarks - bold</span></span>

<span data-ttu-id="ee3e0-458">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-458">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="ee3e0-459">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-459">0 Use the default font weight.</span></span>
-   <span data-ttu-id="ee3e0-460">1 シン。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-460">1 Thin.</span></span>
-   <span data-ttu-id="ee3e0-461">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-461">2 Extra-light.</span></span>
-   <span data-ttu-id="ee3e0-462">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-462">3 Light.</span></span>
-   <span data-ttu-id="ee3e0-463">4 標準。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-463">4 Normal.</span></span>
-   <span data-ttu-id="ee3e0-464">5 中。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-464">5 Medium.</span></span>
-   <span data-ttu-id="ee3e0-465">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-465">6 Semibold.</span></span>
-   <span data-ttu-id="ee3e0-466">7 太字。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-466">7 Bold.</span></span>
-   <span data-ttu-id="ee3e0-467">8 極太。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-467">8 Extra-bold.</span></span>
-   <span data-ttu-id="ee3e0-468">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-468">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="ee3e0-469">メソッド border</span><span class="sxs-lookup"><span data-stu-id="ee3e0-469">Method border</span></span>

<span data-ttu-id="ee3e0-470">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-470">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="ee3e0-471">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="ee3e0-471">Parameters - border</span></span>

<span data-ttu-id="ee3e0-472">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-472">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="ee3e0-473">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="ee3e0-473">Return Value - border</span></span>

<span data-ttu-id="ee3e0-474">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-474">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="ee3e0-475">備考 - border</span><span class="sxs-lookup"><span data-stu-id="ee3e0-475">Remarks - border</span></span>

<span data-ttu-id="ee3e0-476">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-476">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="ee3e0-477">値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-477">Value.</span></span> | <span data-ttu-id="ee3e0-478">説明。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-478">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="ee3e0-479">0</span><span class="sxs-lookup"><span data-stu-id="ee3e0-479">0</span></span>      | <span data-ttu-id="ee3e0-480">自動。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-480">Auto.</span></span>        |
| <span data-ttu-id="ee3e0-481">1</span><span class="sxs-lookup"><span data-stu-id="ee3e0-481">1</span></span>      | <span data-ttu-id="ee3e0-482">3D。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-482">3D.</span></span>          |
| <span data-ttu-id="ee3e0-483">2</span><span class="sxs-lookup"><span data-stu-id="ee3e0-483">2</span></span>      | <span data-ttu-id="ee3e0-484">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-484">Single line.</span></span> |
| <span data-ttu-id="ee3e0-485">3</span><span class="sxs-lookup"><span data-stu-id="ee3e0-485">3</span></span>      | <span data-ttu-id="ee3e0-486">均一。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-486">Flat.</span></span>        |
| <span data-ttu-id="ee3e0-487">4</span><span class="sxs-lookup"><span data-stu-id="ee3e0-487">4</span></span>      | <span data-ttu-id="ee3e0-488">なし。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-488">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="ee3e0-489">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-489">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="ee3e0-490">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-490">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="ee3e0-491">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-491">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="ee3e0-492">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-492">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="ee3e0-493">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-493">Method calcControlSize</span></span>

<span data-ttu-id="ee3e0-494">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-494">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="ee3e0-495">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-495">Parameters - calcControlSize</span></span>

<span data-ttu-id="ee3e0-496">chars</span><span class="sxs-lookup"><span data-stu-id="ee3e0-496">chars</span></span>  
<span data-ttu-id="ee3e0-497">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-497">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-498">明細行</span><span class="sxs-lookup"><span data-stu-id="ee3e0-498">lines</span></span>  
<span data-ttu-id="ee3e0-499">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-499">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="ee3e0-500">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-500">Return Value - calcControlSize</span></span>

<span data-ttu-id="ee3e0-501">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-501">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="ee3e0-502">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="ee3e0-502">Method characterSet</span></span>

<span data-ttu-id="ee3e0-503">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-503">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="ee3e0-504">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="ee3e0-504">Parameters - characterSet</span></span>

<span data-ttu-id="ee3e0-505">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-505">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="ee3e0-506">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="ee3e0-506">Return Value - characterSet</span></span>

<span data-ttu-id="ee3e0-507">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-507">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="ee3e0-508">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="ee3e0-508">Remarks - characterSet</span></span>

<span data-ttu-id="ee3e0-509">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-509">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="ee3e0-510">値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-510">Value.</span></span> | <span data-ttu-id="ee3e0-511">説明。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-511">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="ee3e0-512">0</span><span class="sxs-lookup"><span data-stu-id="ee3e0-512">0</span></span>      | <span data-ttu-id="ee3e0-513">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-513">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="ee3e0-514">1</span><span class="sxs-lookup"><span data-stu-id="ee3e0-514">1</span></span>      | <span data-ttu-id="ee3e0-515">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-515">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="ee3e0-516">2</span><span class="sxs-lookup"><span data-stu-id="ee3e0-516">2</span></span>      | <span data-ttu-id="ee3e0-517">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-517">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="ee3e0-518">77</span><span class="sxs-lookup"><span data-stu-id="ee3e0-518">77</span></span>     | <span data-ttu-id="ee3e0-519">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-519">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="ee3e0-520">128</span><span class="sxs-lookup"><span data-stu-id="ee3e0-520">128</span></span>    | <span data-ttu-id="ee3e0-521">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-521">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="ee3e0-522">129</span><span class="sxs-lookup"><span data-stu-id="ee3e0-522">129</span></span>    | <span data-ttu-id="ee3e0-523">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-523">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="ee3e0-524">134</span><span class="sxs-lookup"><span data-stu-id="ee3e0-524">134</span></span>    | <span data-ttu-id="ee3e0-525">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-525">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="ee3e0-526">136</span><span class="sxs-lookup"><span data-stu-id="ee3e0-526">136</span></span>    | <span data-ttu-id="ee3e0-527">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-527">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="ee3e0-528">161</span><span class="sxs-lookup"><span data-stu-id="ee3e0-528">161</span></span>    | <span data-ttu-id="ee3e0-529">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-529">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="ee3e0-530">162</span><span class="sxs-lookup"><span data-stu-id="ee3e0-530">162</span></span>    | <span data-ttu-id="ee3e0-531">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-531">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="ee3e0-532">163</span><span class="sxs-lookup"><span data-stu-id="ee3e0-532">163</span></span>    | <span data-ttu-id="ee3e0-533">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-533">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="ee3e0-534">186</span><span class="sxs-lookup"><span data-stu-id="ee3e0-534">186</span></span>    | <span data-ttu-id="ee3e0-535">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-535">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="ee3e0-536">204</span><span class="sxs-lookup"><span data-stu-id="ee3e0-536">204</span></span>    | <span data-ttu-id="ee3e0-537">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-537">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="ee3e0-538">238</span><span class="sxs-lookup"><span data-stu-id="ee3e0-538">238</span></span>    | <span data-ttu-id="ee3e0-539">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-539">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="ee3e0-540">255</span><span class="sxs-lookup"><span data-stu-id="ee3e0-540">255</span></span>    | <span data-ttu-id="ee3e0-541">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-541">OEM\_CHARSET</span></span>         |

<span data-ttu-id="ee3e0-542">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-542">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="ee3e0-543">値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-543">Value.</span></span> | <span data-ttu-id="ee3e0-544">説明。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-544">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="ee3e0-545">130</span><span class="sxs-lookup"><span data-stu-id="ee3e0-545">130</span></span>    | <span data-ttu-id="ee3e0-546">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-546">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="ee3e0-547">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-547">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="ee3e0-548">値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-548">Value.</span></span> | <span data-ttu-id="ee3e0-549">説明。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-549">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="ee3e0-550">177</span><span class="sxs-lookup"><span data-stu-id="ee3e0-550">177</span></span>    | <span data-ttu-id="ee3e0-551">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-551">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="ee3e0-552">178</span><span class="sxs-lookup"><span data-stu-id="ee3e0-552">178</span></span>    | <span data-ttu-id="ee3e0-553">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-553">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="ee3e0-554">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-554">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="ee3e0-555">値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-555">Value.</span></span> | <span data-ttu-id="ee3e0-556">説明。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-556">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="ee3e0-557">222</span><span class="sxs-lookup"><span data-stu-id="ee3e0-557">222</span></span>    | <span data-ttu-id="ee3e0-558">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="ee3e0-558">THAI\_CHARSET</span></span> |

<span data-ttu-id="ee3e0-559">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-559">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="ee3e0-560">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-560">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="ee3e0-561">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-561">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="ee3e0-562">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="ee3e0-562">Method colorScheme</span></span>

<span data-ttu-id="ee3e0-563">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-563">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="ee3e0-564">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ee3e0-564">Parameters - colorScheme</span></span>

<span data-ttu-id="ee3e0-565">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-565">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="ee3e0-566">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ee3e0-566">Return Value - colorScheme</span></span>

<span data-ttu-id="ee3e0-567">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-567">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="ee3e0-568">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="ee3e0-568">Remarks - colorScheme</span></span>

<span data-ttu-id="ee3e0-569">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-569">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="ee3e0-570">値です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-570">Value.</span></span> | <span data-ttu-id="ee3e0-571">スタイル。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-571">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="ee3e0-572">0</span><span class="sxs-lookup"><span data-stu-id="ee3e0-572">0</span></span>      | <span data-ttu-id="ee3e0-573">既定。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-573">Default.</span></span>                       |
| <span data-ttu-id="ee3e0-574">1</span><span class="sxs-lookup"><span data-stu-id="ee3e0-574">1</span></span>      | <span data-ttu-id="ee3e0-575">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-575">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="ee3e0-576">2</span><span class="sxs-lookup"><span data-stu-id="ee3e0-576">2</span></span>      | <span data-ttu-id="ee3e0-577">真の配色。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-577">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="ee3e0-578">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee3e0-578">Method configurationKey</span></span>

<span data-ttu-id="ee3e0-579">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-579">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="ee3e0-580">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee3e0-580">Parameters - configurationKey</span></span>

<span data-ttu-id="ee3e0-581">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-581">value</span></span>  
<span data-ttu-id="ee3e0-582">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-582">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="ee3e0-583">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee3e0-583">Return Value - configurationKey</span></span>

<span data-ttu-id="ee3e0-584">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-584">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="ee3e0-585">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="ee3e0-585">Remarks - configurationKey</span></span>

<span data-ttu-id="ee3e0-586">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-586">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="ee3e0-587">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-587">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="ee3e0-588">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-588">Method configurationKeyEx</span></span>

<span data-ttu-id="ee3e0-589">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-589">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="ee3e0-590">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-590">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="ee3e0-591">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-591">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="ee3e0-592">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-592">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="ee3e0-593">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-593">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="ee3e0-594">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-594">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="ee3e0-595">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-595">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="ee3e0-596">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ee3e0-596">Method countryRegionCodes</span></span>

<span data-ttu-id="ee3e0-597">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-597">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="ee3e0-598">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ee3e0-598">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="ee3e0-599">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-599">value</span></span>  
<span data-ttu-id="ee3e0-600">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-600">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="ee3e0-601">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="ee3e0-601">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="ee3e0-602">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-602">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="ee3e0-603">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-603">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="ee3e0-604">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-604">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="ee3e0-605">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-605">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="ee3e0-606">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-606">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="ee3e0-607">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-607">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="ee3e0-608">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-608">Parameters - dataField</span></span>

<span data-ttu-id="ee3e0-609">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-609">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="ee3e0-610">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-610">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="ee3e0-611">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-611">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="ee3e0-612">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-612">Parameters - dataMethod</span></span>

<span data-ttu-id="ee3e0-613">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-613">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="ee3e0-614">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-614">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="ee3e0-615">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ee3e0-615">Method dataRelationPath</span></span>

<span data-ttu-id="ee3e0-616">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-616">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="ee3e0-617">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ee3e0-617">Parameters - dataRelationPath</span></span>

<span data-ttu-id="ee3e0-618">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-618">value</span></span>  
<span data-ttu-id="ee3e0-619">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-619">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="ee3e0-620">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ee3e0-620">Return Value - dataRelationPath</span></span>

<span data-ttu-id="ee3e0-621">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-621">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="ee3e0-622">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="ee3e0-622">Remarks - dataRelationPath</span></span>

<span data-ttu-id="ee3e0-623">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-623">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="ee3e0-624">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-624">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="ee3e0-625">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="ee3e0-625">Method dataSource</span></span>

<span data-ttu-id="ee3e0-626">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-626">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="ee3e0-627">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="ee3e0-627">Parameters - dataSource</span></span>

<span data-ttu-id="ee3e0-628">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-628">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="ee3e0-629">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="ee3e0-629">Return Value - dataSource</span></span>

<span data-ttu-id="ee3e0-630">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-630">The identifier of the data source to be used.</span></span>

## <a name="method-dateday"></a><span data-ttu-id="ee3e0-631">メソッド dateDay</span><span class="sxs-lookup"><span data-stu-id="ee3e0-631">Method dateDay</span></span>

```xpp
public int dateDay([int value])
```

### <a name="parameters---dateday"></a><span data-ttu-id="ee3e0-632">パラメーター - dateDay</span><span class="sxs-lookup"><span data-stu-id="ee3e0-632">Parameters - dateDay</span></span>

<span data-ttu-id="ee3e0-633">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-633">value</span></span>  

### <a name="return-value---dateday"></a><span data-ttu-id="ee3e0-634">戻り値 - dateDay</span><span class="sxs-lookup"><span data-stu-id="ee3e0-634">Return Value - dateDay</span></span>

## <a name="method-dateformat"></a><span data-ttu-id="ee3e0-635">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="ee3e0-635">Method dateFormat</span></span>

```xpp
public int dateFormat([int value])
```

### <a name="parameters---dateformat"></a><span data-ttu-id="ee3e0-636">パラメーター - dateFormat</span><span class="sxs-lookup"><span data-stu-id="ee3e0-636">Parameters - dateFormat</span></span>

<span data-ttu-id="ee3e0-637">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-637">value</span></span>  

### <a name="return-value---dateformat"></a><span data-ttu-id="ee3e0-638">戻り値 - dateFormat</span><span class="sxs-lookup"><span data-stu-id="ee3e0-638">Return Value - dateFormat</span></span>

## <a name="method-datemonth"></a><span data-ttu-id="ee3e0-639">メソッド dateMonth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-639">Method dateMonth</span></span>

```xpp
public int dateMonth([int value])
```

### <a name="parameters---datemonth"></a><span data-ttu-id="ee3e0-640">パラメーター - dateMonth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-640">Parameters - dateMonth</span></span>

<span data-ttu-id="ee3e0-641">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-641">value</span></span>  

### <a name="return-value---datemonth"></a><span data-ttu-id="ee3e0-642">戻り値 - dateMonth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-642">Return Value - dateMonth</span></span>

## <a name="method-dateseparator"></a><span data-ttu-id="ee3e0-643">メソッド dateSeparator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-643">Method dateSeparator</span></span>

```xpp
public int dateSeparator([int value])
```

### <a name="parameters---dateseparator"></a><span data-ttu-id="ee3e0-644">パラメーター - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-644">Parameters - dateSeparator</span></span>

<span data-ttu-id="ee3e0-645">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-645">value</span></span>  

### <a name="return-value---dateseparator"></a><span data-ttu-id="ee3e0-646">戻り値 - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-646">Return Value - dateSeparator</span></span>

## <a name="method-datetimevalue"></a><span data-ttu-id="ee3e0-647">メソッド dateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-647">Method dateTimeValue</span></span>

```xpp
public DateTime dateTimeValue([DateTime value])
```

### <a name="parameters---datetimevalue"></a><span data-ttu-id="ee3e0-648">パラメーター - dateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-648">Parameters - dateTimeValue</span></span>

<span data-ttu-id="ee3e0-649">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-649">value</span></span>  

### <a name="return-value---datetimevalue"></a><span data-ttu-id="ee3e0-650">戻り値 - dateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-650">Return Value - dateTimeValue</span></span>

## <a name="method-dateyear"></a><span data-ttu-id="ee3e0-651">メソッド dateYear</span><span class="sxs-lookup"><span data-stu-id="ee3e0-651">Method dateYear</span></span>

```xpp
public int dateYear([int value])
```

### <a name="parameters---dateyear"></a><span data-ttu-id="ee3e0-652">パラメーター - dateYear</span><span class="sxs-lookup"><span data-stu-id="ee3e0-652">Parameters - dateYear</span></span>

<span data-ttu-id="ee3e0-653">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-653">value</span></span>  

### <a name="return-value---dateyear"></a><span data-ttu-id="ee3e0-654">戻り値 - dateYear</span><span class="sxs-lookup"><span data-stu-id="ee3e0-654">Return Value - dateYear</span></span>

## <a name="method-displayoption"></a><span data-ttu-id="ee3e0-655">メソッド displayOption</span><span class="sxs-lookup"><span data-stu-id="ee3e0-655">Method displayOption</span></span>

```xpp
public int displayOption([int value])
```

### <a name="parameters---displayoption"></a><span data-ttu-id="ee3e0-656">パラメーター - displayOption</span><span class="sxs-lookup"><span data-stu-id="ee3e0-656">Parameters - displayOption</span></span>

<span data-ttu-id="ee3e0-657">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-657">value</span></span>  

### <a name="return-value---displayoption"></a><span data-ttu-id="ee3e0-658">戻り値 - displayOption</span><span class="sxs-lookup"><span data-stu-id="ee3e0-658">Return Value - displayOption</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="ee3e0-659">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="ee3e0-659">Method displayTarget</span></span>

<span data-ttu-id="ee3e0-660">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-660">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="ee3e0-661">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ee3e0-661">Parameters - displayTarget</span></span>

<span data-ttu-id="ee3e0-662">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-662">value</span></span>  
<span data-ttu-id="ee3e0-663">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-663">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="ee3e0-664">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="ee3e0-664">Return Value - displayTarget</span></span>

<span data-ttu-id="ee3e0-665">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-665">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="ee3e0-666">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="ee3e0-666">Method dragDrop</span></span>

<span data-ttu-id="ee3e0-667">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-667">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="ee3e0-668">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ee3e0-668">Parameters - dragDrop</span></span>

<span data-ttu-id="ee3e0-669">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-669">value</span></span>  
<span data-ttu-id="ee3e0-670">ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-670">An Integer data type that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="ee3e0-671">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ee3e0-671">Return Value - dragDrop</span></span>

<span data-ttu-id="ee3e0-672">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-672">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="ee3e0-673">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="ee3e0-673">Remarks - dragDrop</span></span>

<span data-ttu-id="ee3e0-674">FormControl::dragLeave メソッド、FormControl::dragOver メソッド、および FormControl::dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-674">Use the FormControl::dragLeave method, the FormControl::dragOver method, and the FormControl::dragOverEx method to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="ee3e0-675">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="ee3e0-675">Method dragOver</span></span>

<span data-ttu-id="ee3e0-676">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-676">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="ee3e0-677">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="ee3e0-677">Parameters - dragOver</span></span>

<span data-ttu-id="ee3e0-678">dragSource</span><span class="sxs-lookup"><span data-stu-id="ee3e0-678">dragSource</span></span>  
<span data-ttu-id="ee3e0-679">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-679">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-680">dragMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-680">dragMode</span></span>  
<span data-ttu-id="ee3e0-681">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-681">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-682">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-682">x</span></span>  
<span data-ttu-id="ee3e0-683">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-683">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-684">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-684">y</span></span>  
<span data-ttu-id="ee3e0-685">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-685">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="ee3e0-686">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="ee3e0-686">Return Value - dragOver</span></span>

<span data-ttu-id="ee3e0-687">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-687">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="ee3e0-688">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-688">Method dragOverEx</span></span>

<span data-ttu-id="ee3e0-689">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-689">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="ee3e0-690">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-690">Parameters - dragOverEx</span></span>

<span data-ttu-id="ee3e0-691">dragSource</span><span class="sxs-lookup"><span data-stu-id="ee3e0-691">dragSource</span></span>  
<span data-ttu-id="ee3e0-692">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-692">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-693">dragMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-693">dragMode</span></span>  
<span data-ttu-id="ee3e0-694">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-694">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-695">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-695">x</span></span>  
<span data-ttu-id="ee3e0-696">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-696">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-697">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-697">y</span></span>  
<span data-ttu-id="ee3e0-698">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-698">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="ee3e0-699">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-699">Return Value - dragOverEx</span></span>

<span data-ttu-id="ee3e0-700">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-700">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="ee3e0-701">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-701">Method dragText</span></span>

<span data-ttu-id="ee3e0-702">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-702">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="ee3e0-703">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-703">Return Value - dragText</span></span>

<span data-ttu-id="ee3e0-704">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-704">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="ee3e0-705">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-705">Method enabled</span></span>

<span data-ttu-id="ee3e0-706">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-706">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="ee3e0-707">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-707">Parameters - enabled</span></span>

<span data-ttu-id="ee3e0-708">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-708">value</span></span>  
<span data-ttu-id="ee3e0-709">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-709">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="ee3e0-710">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-710">Return Value - enabled</span></span>

<span data-ttu-id="ee3e0-711">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-711">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="ee3e0-712">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-712">Remarks - enabled</span></span>

<span data-ttu-id="ee3e0-713">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-713">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="ee3e0-714">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-714">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="ee3e0-715">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-715">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="ee3e0-716">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="ee3e0-716">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="ee3e0-717">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="ee3e0-717">Parameters - extendedDataType</span></span>

<span data-ttu-id="ee3e0-718">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-718">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="ee3e0-719">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="ee3e0-719">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="ee3e0-720">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ee3e0-720">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="ee3e0-721">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ee3e0-721">Parameters - fastTabSummary</span></span>

<span data-ttu-id="ee3e0-722">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-722">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="ee3e0-723">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ee3e0-723">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="ee3e0-724">メソッド font</span><span class="sxs-lookup"><span data-stu-id="ee3e0-724">Method font</span></span>

<span data-ttu-id="ee3e0-725">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-725">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="ee3e0-726">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="ee3e0-726">Parameters - font</span></span>

<span data-ttu-id="ee3e0-727">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-727">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="ee3e0-728">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="ee3e0-728">Return Value - font</span></span>

<span data-ttu-id="ee3e0-729">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-729">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="ee3e0-730">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-730">Method fontSize</span></span>

<span data-ttu-id="ee3e0-731">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-731">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="ee3e0-732">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-732">Parameters - fontSize</span></span>

<span data-ttu-id="ee3e0-733">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-733">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="ee3e0-734">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-734">Return Value - fontSize</span></span>

<span data-ttu-id="ee3e0-735">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-735">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="ee3e0-736">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-736">Method foregroundColor</span></span>

<span data-ttu-id="ee3e0-737">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-737">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="ee3e0-738">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-738">Parameters - foregroundColor</span></span>

<span data-ttu-id="ee3e0-739">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-739">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="ee3e0-740">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-740">Return Value - foregroundColor</span></span>

<span data-ttu-id="ee3e0-741">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-741">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="ee3e0-742">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-742">Remarks - foregroundColor</span></span>

<span data-ttu-id="ee3e0-743">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-743">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="ee3e0-744">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-744">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="ee3e0-745">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-745">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="ee3e0-746">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-746">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="ee3e0-747">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-747">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="ee3e0-748">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-748">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="ee3e0-749">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="ee3e0-749">Method hasChanged</span></span>

<span data-ttu-id="ee3e0-750">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-750">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="ee3e0-751">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="ee3e0-751">Parameters - hasChanged</span></span>

<span data-ttu-id="ee3e0-752">val</span><span class="sxs-lookup"><span data-stu-id="ee3e0-752">val</span></span>  
<span data-ttu-id="ee3e0-753">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-753">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="ee3e0-754">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="ee3e0-754">Return Value - hasChanged</span></span>

<span data-ttu-id="ee3e0-755">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-755">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="ee3e0-756">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="ee3e0-756">Method hasUserSetting</span></span>

<span data-ttu-id="ee3e0-757">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-757">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="ee3e0-758">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="ee3e0-758">Return Value - hasUserSetting</span></span>

<span data-ttu-id="ee3e0-759">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-759">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="ee3e0-760">メソッド height</span><span class="sxs-lookup"><span data-stu-id="ee3e0-760">Method height</span></span>

<span data-ttu-id="ee3e0-761">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-761">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="ee3e0-762">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="ee3e0-762">Parameters - height</span></span>

<span data-ttu-id="ee3e0-763">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-763">value</span></span>  
<span data-ttu-id="ee3e0-764">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-764">An Integer data type that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-765">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-765">mode</span></span>  
<span data-ttu-id="ee3e0-766">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-766">An Integer data type that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="ee3e0-767">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="ee3e0-767">Return Value - height</span></span>

<span data-ttu-id="ee3e0-768">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-768">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="ee3e0-769">備考 - height</span><span class="sxs-lookup"><span data-stu-id="ee3e0-769">Remarks - height</span></span>

<span data-ttu-id="ee3e0-770">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-770">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ee3e0-771">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ee3e0-771">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ee3e0-772">モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-772">Mode.</span></span>            | <span data-ttu-id="ee3e0-773">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-773">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e0-774">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-774">-1 Exact.</span></span>        | <span data-ttu-id="ee3e0-775">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-775">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee3e0-776">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-776">0 Auto.</span></span>          | <span data-ttu-id="ee3e0-777">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-777">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee3e0-778">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-778">1 Column height.</span></span> | <span data-ttu-id="ee3e0-779">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-779">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ee3e0-780">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-780">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="ee3e0-781">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-781">Method heightMode</span></span>

<span data-ttu-id="ee3e0-782">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-782">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="ee3e0-783">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-783">Parameters - heightMode</span></span>

<span data-ttu-id="ee3e0-784">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-784">value</span></span>  
<span data-ttu-id="ee3e0-785">コントロールの高さの計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-785">An Integer data type value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="ee3e0-786">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-786">Return Value - heightMode</span></span>

<span data-ttu-id="ee3e0-787">計算モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-787">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="ee3e0-788">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-788">Remarks - heightMode</span></span>

<span data-ttu-id="ee3e0-789">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="ee3e0-789">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="ee3e0-790">モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-790">Mode.</span></span>          | <span data-ttu-id="ee3e0-791">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-791">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e0-792">正確。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-792">Exact.</span></span>         | <span data-ttu-id="ee3e0-793">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-793">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee3e0-794">自動。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-794">Auto.</span></span>          | <span data-ttu-id="ee3e0-795">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-795">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee3e0-796">列の高さ</span><span class="sxs-lookup"><span data-stu-id="ee3e0-796">Column height.</span></span> | <span data-ttu-id="ee3e0-797">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-797">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="ee3e0-798">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-798">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="ee3e0-799">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-799">Method heightValue</span></span>

<span data-ttu-id="ee3e0-800">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-800">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="ee3e0-801">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-801">Parameters - heightValue</span></span>

<span data-ttu-id="ee3e0-802">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-802">value</span></span>  
<span data-ttu-id="ee3e0-803">高さをピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-803">An Integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="ee3e0-804">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-804">Return Value - heightValue</span></span>

<span data-ttu-id="ee3e0-805">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-805">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="ee3e0-806">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-806">Remarks - heightValue</span></span>

<span data-ttu-id="ee3e0-807">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-807">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="ee3e0-808">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-808">Method helpField</span></span>

<span data-ttu-id="ee3e0-809">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-809">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="ee3e0-810">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-810">Return Value - helpField</span></span>

<span data-ttu-id="ee3e0-811">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-811">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="ee3e0-812">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="ee3e0-812">Remarks - helpField</span></span>

<span data-ttu-id="ee3e0-813">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-813">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="ee3e0-814">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-814">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="ee3e0-815">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-815">Method helpText</span></span>

<span data-ttu-id="ee3e0-816">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-816">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="ee3e0-817">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-817">Parameters - helpText</span></span>

<span data-ttu-id="ee3e0-818">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-818">value</span></span>  
<span data-ttu-id="ee3e0-819">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-819">The value that is assigned as the help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="ee3e0-820">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-820">Return Value - helpText</span></span>

<span data-ttu-id="ee3e0-821">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-821">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="ee3e0-822">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-822">Remarks - helpText</span></span>

<span data-ttu-id="ee3e0-823">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-823">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="ee3e0-824">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-824">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="ee3e0-825">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ee3e0-825">Method hierarchyParent</span></span>

<span data-ttu-id="ee3e0-826">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-826">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="ee3e0-827">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ee3e0-827">Parameters - hierarchyParent</span></span>

<span data-ttu-id="ee3e0-828">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-828">value</span></span>  
<span data-ttu-id="ee3e0-829">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-829">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="ee3e0-830">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="ee3e0-830">Return Value - hierarchyParent</span></span>

<span data-ttu-id="ee3e0-831">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-831">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="ee3e0-832">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="ee3e0-832">Method hWnd</span></span>

<span data-ttu-id="ee3e0-833">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-833">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="ee3e0-834">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="ee3e0-834">Return Value - hWnd</span></span>

<span data-ttu-id="ee3e0-835">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-835">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="ee3e0-836">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="ee3e0-836">Remarks - hWnd</span></span>

<span data-ttu-id="ee3e0-837">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-837">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="ee3e0-838">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="ee3e0-838">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="ee3e0-839">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="ee3e0-839">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="ee3e0-840">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ee3e0-840">Method isDisplayed</span></span>

<span data-ttu-id="ee3e0-841">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-841">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="ee3e0-842">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ee3e0-842">Return Value - isDisplayed</span></span>

<span data-ttu-id="ee3e0-843">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-843">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="ee3e0-844">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="ee3e0-844">Remarks - isDisplayed</span></span>

<span data-ttu-id="ee3e0-845">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-845">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="ee3e0-846">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="ee3e0-846">Method isRestricted</span></span>

<span data-ttu-id="ee3e0-847">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-847">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="ee3e0-848">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="ee3e0-848">Return Value - isRestricted</span></span>

<span data-ttu-id="ee3e0-849">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-849">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="ee3e0-850">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-850">Method isUserSetupEnabled</span></span>

<span data-ttu-id="ee3e0-851">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-851">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="ee3e0-852">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-852">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="ee3e0-853">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="ee3e0-853">neededSetupRights</span></span>  
<span data-ttu-id="ee3e0-854">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値、オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-854">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control; optional.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="ee3e0-855">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-855">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="ee3e0-856">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-856">true if the control, design, and parent containers allow for the level of customization that specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="ee3e0-857">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="ee3e0-857">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="ee3e0-858">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-858">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e0-859">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="ee3e0-859">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="ee3e0-860">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-860">No changes can be made to the control.</span></span> <span data-ttu-id="ee3e0-861">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-861">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="ee3e0-862">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="ee3e0-862">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="ee3e0-863">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-863">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="ee3e0-864">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-864">The user cannot move the control.</span></span>   |
| <span data-ttu-id="ee3e0-865">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="ee3e0-865">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="ee3e0-866">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-866">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="ee3e0-867">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-867">The user can also move the control.</span></span> |

<span data-ttu-id="ee3e0-868">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-868">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="ee3e0-869">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="ee3e0-869">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="ee3e0-870">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="ee3e0-870">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="ee3e0-871">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="ee3e0-871">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="ee3e0-872">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="ee3e0-872">Parameters - italic</span></span>

<span data-ttu-id="ee3e0-873">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-873">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="ee3e0-874">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="ee3e0-874">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="ee3e0-875">メソッド label</span><span class="sxs-lookup"><span data-stu-id="ee3e0-875">Method label</span></span>

<span data-ttu-id="ee3e0-876">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-876">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="ee3e0-877">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="ee3e0-877">Parameters - label</span></span>

<span data-ttu-id="ee3e0-878">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-878">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="ee3e0-879">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="ee3e0-879">Return Value - label</span></span>

<span data-ttu-id="ee3e0-880">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-880">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="ee3e0-881">備考 - label</span><span class="sxs-lookup"><span data-stu-id="ee3e0-881">Remarks - label</span></span>

<span data-ttu-id="ee3e0-882">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-882">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="ee3e0-883">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-883">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="ee3e0-884">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="ee3e0-884">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="ee3e0-885">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="ee3e0-885">Parameters - labelAlignment</span></span>

<span data-ttu-id="ee3e0-886">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-886">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="ee3e0-887">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="ee3e0-887">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="ee3e0-888">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="ee3e0-888">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="ee3e0-889">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="ee3e0-889">Parameters - labelBold</span></span>

<span data-ttu-id="ee3e0-890">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-890">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="ee3e0-891">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="ee3e0-891">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="ee3e0-892">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="ee3e0-892">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="ee3e0-893">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="ee3e0-893">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="ee3e0-894">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-894">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="ee3e0-895">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="ee3e0-895">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="ee3e0-896">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="ee3e0-896">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="ee3e0-897">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="ee3e0-897">Parameters - labelFont</span></span>

<span data-ttu-id="ee3e0-898">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-898">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="ee3e0-899">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="ee3e0-899">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="ee3e0-900">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-900">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="ee3e0-901">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-901">Parameters - labelFontSize</span></span>

<span data-ttu-id="ee3e0-902">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-902">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="ee3e0-903">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-903">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="ee3e0-904">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-904">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="ee3e0-905">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-905">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="ee3e0-906">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-906">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="ee3e0-907">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="ee3e0-907">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="ee3e0-908">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="ee3e0-908">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="ee3e0-909">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="ee3e0-909">Parameters - labelGuide</span></span>

<span data-ttu-id="ee3e0-910">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-910">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="ee3e0-911">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="ee3e0-911">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="ee3e0-912">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="ee3e0-912">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="ee3e0-913">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="ee3e0-913">Parameters - labelHeight</span></span>

<span data-ttu-id="ee3e0-914">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-914">value</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-915">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-915">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="ee3e0-916">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="ee3e0-916">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="ee3e0-917">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-917">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="ee3e0-918">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-918">Parameters - labelHeightMode</span></span>

<span data-ttu-id="ee3e0-919">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-919">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="ee3e0-920">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-920">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="ee3e0-921">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-921">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="ee3e0-922">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-922">Parameters - labelHeightValue</span></span>

<span data-ttu-id="ee3e0-923">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-923">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="ee3e0-924">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-924">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="ee3e0-925">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="ee3e0-925">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="ee3e0-926">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="ee3e0-926">Parameters - labelItalic</span></span>

<span data-ttu-id="ee3e0-927">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-927">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="ee3e0-928">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="ee3e0-928">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="ee3e0-929">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ee3e0-929">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="ee3e0-930">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ee3e0-930">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="ee3e0-931">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-931">x</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-932">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-932">y</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-933">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-933">button</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-934">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-934">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-935">Shift</span><span class="sxs-lookup"><span data-stu-id="ee3e0-935">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="ee3e0-936">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ee3e0-936">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="ee3e0-937">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="ee3e0-937">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="ee3e0-938">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="ee3e0-938">Parameters - labelMouseDown</span></span>

<span data-ttu-id="ee3e0-939">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-939">x</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-940">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-940">y</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-941">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-941">button</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-942">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-942">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-943">Shift</span><span class="sxs-lookup"><span data-stu-id="ee3e0-943">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="ee3e0-944">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="ee3e0-944">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="ee3e0-945">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="ee3e0-945">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="ee3e0-946">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="ee3e0-946">Parameters - labelMouseUp</span></span>

<span data-ttu-id="ee3e0-947">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-947">x</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-948">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-948">y</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-949">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-949">button</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-950">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-950">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-951">Shift</span><span class="sxs-lookup"><span data-stu-id="ee3e0-951">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="ee3e0-952">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="ee3e0-952">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="ee3e0-953">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="ee3e0-953">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="ee3e0-954">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="ee3e0-954">Parameters - labelPosition</span></span>

<span data-ttu-id="ee3e0-955">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-955">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="ee3e0-956">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="ee3e0-956">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="ee3e0-957">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="ee3e0-957">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="ee3e0-958">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="ee3e0-958">Parameters - labelUnderline</span></span>

<span data-ttu-id="ee3e0-959">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-959">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="ee3e0-960">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="ee3e0-960">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="ee3e0-961">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-961">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="ee3e0-962">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-962">Parameters - labelWidth</span></span>

<span data-ttu-id="ee3e0-963">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-963">value</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-964">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-964">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="ee3e0-965">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-965">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="ee3e0-966">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-966">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="ee3e0-967">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-967">Parameters - labelWidthMode</span></span>

<span data-ttu-id="ee3e0-968">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-968">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="ee3e0-969">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-969">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="ee3e0-970">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-970">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="ee3e0-971">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-971">Parameters - labelWidthValue</span></span>

<span data-ttu-id="ee3e0-972">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-972">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="ee3e0-973">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-973">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="ee3e0-974">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="ee3e0-974">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="ee3e0-975">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="ee3e0-975">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="ee3e0-976">メソッド left</span><span class="sxs-lookup"><span data-stu-id="ee3e0-976">Method left</span></span>

<span data-ttu-id="ee3e0-977">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-977">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="ee3e0-978">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="ee3e0-978">Parameters - left</span></span>

<span data-ttu-id="ee3e0-979">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-979">value</span></span>  
<span data-ttu-id="ee3e0-980">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-980">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-981">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-981">mode</span></span>  
<span data-ttu-id="ee3e0-982">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-982">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="ee3e0-983">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="ee3e0-983">Return Value - left</span></span>

<span data-ttu-id="ee3e0-984">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-984">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="ee3e0-985">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-985">Method leftMode</span></span>

<span data-ttu-id="ee3e0-986">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-986">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="ee3e0-987">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-987">Parameters - leftMode</span></span>

<span data-ttu-id="ee3e0-988">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-988">value</span></span>  
<span data-ttu-id="ee3e0-989">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-989">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="ee3e0-990">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-990">Return Value - leftMode</span></span>

<span data-ttu-id="ee3e0-991">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-991">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="ee3e0-992">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-992">Method leftValue</span></span>

<span data-ttu-id="ee3e0-993">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-993">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="ee3e0-994">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-994">Parameters - leftValue</span></span>

<span data-ttu-id="ee3e0-995">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-995">value</span></span>  
<span data-ttu-id="ee3e0-996">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-996">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="ee3e0-997">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-997">Return Value - leftValue</span></span>

<span data-ttu-id="ee3e0-998">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-998">The horizontal position of the control in the form.</span></span>

## <a name="method-limittext"></a><span data-ttu-id="ee3e0-999">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-999">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="ee3e0-1000">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1000">Parameters - limitText</span></span>

<span data-ttu-id="ee3e0-1001">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1001">value</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1002">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1002">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="ee3e0-1003">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1003">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="ee3e0-1004">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1004">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="ee3e0-1005">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1005">Parameters - limitTextMode</span></span>

<span data-ttu-id="ee3e0-1006">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1006">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="ee3e0-1007">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1007">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="ee3e0-1008">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1008">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="ee3e0-1009">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1009">Parameters - limitTextValue</span></span>

<span data-ttu-id="ee3e0-1010">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1010">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="ee3e0-1011">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1011">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="ee3e0-1012">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1012">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="ee3e0-1013">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1013">Parameters - lookupButton</span></span>

<span data-ttu-id="ee3e0-1014">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1014">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="ee3e0-1015">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1015">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="ee3e0-1016">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1016">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="ee3e0-1017">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1017">Parameters - mandatory</span></span>

<span data-ttu-id="ee3e0-1018">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1018">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="ee3e0-1019">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1019">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="ee3e0-1020">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1020">Method markAsUserAdd</span></span>

<span data-ttu-id="ee3e0-1021">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1021">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="ee3e0-1022">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1022">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="ee3e0-1023">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1023">value</span></span>  
<span data-ttu-id="ee3e0-1024">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1024">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="ee3e0-1025">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1025">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="ee3e0-1026">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1026">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-maxdatelabel"></a><span data-ttu-id="ee3e0-1027">メソッド maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1027">Method maxDateLabel</span></span>

```xpp
public str maxDateLabel([str value])
```

### <a name="parameters---maxdatelabel"></a><span data-ttu-id="ee3e0-1028">パラメーター - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1028">Parameters - maxDateLabel</span></span>

<span data-ttu-id="ee3e0-1029">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1029">value</span></span>  

### <a name="return-value---maxdatelabel"></a><span data-ttu-id="ee3e0-1030">戻り値 - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1030">Return Value - maxDateLabel</span></span>

## <a name="method-maxdatelabeltext"></a><span data-ttu-id="ee3e0-1031">メソッド maxDateLabelText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1031">Method maxDateLabelText</span></span>

```xpp
public str maxDateLabelText()
```

### <a name="return-value---maxdatelabeltext"></a><span data-ttu-id="ee3e0-1032">戻り値 - maxDateLabelText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1032">Return Value - maxDateLabelText</span></span>

## <a name="method-modified"></a><span data-ttu-id="ee3e0-1033">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1033">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="ee3e0-1034">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1034">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="ee3e0-1035">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1035">Method mouseDblClick</span></span>

<span data-ttu-id="ee3e0-1036">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1036">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="ee3e0-1037">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1037">Parameters - mouseDblClick</span></span>

<span data-ttu-id="ee3e0-1038">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1038">x</span></span>  
<span data-ttu-id="ee3e0-1039">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1039">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1040">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1040">y</span></span>  
<span data-ttu-id="ee3e0-1041">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1041">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1042">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1042">button</span></span>  
<span data-ttu-id="ee3e0-1043">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1043">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1044">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1044">Ctrl</span></span>  
<span data-ttu-id="ee3e0-1045">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1045">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1046">シフト</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1046">Shift</span></span>  
<span data-ttu-id="ee3e0-1047">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1047">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="ee3e0-1048">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1048">Return Value - mouseDblClick</span></span>

<span data-ttu-id="ee3e0-1049">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1049">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="ee3e0-1050">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1050">Remarks - mouseDblClick</span></span>

<span data-ttu-id="ee3e0-1051">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1051">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="ee3e0-1052">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1052">Method mouseDown</span></span>

<span data-ttu-id="ee3e0-1053">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1053">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="ee3e0-1054">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1054">Parameters - mouseDown</span></span>

<span data-ttu-id="ee3e0-1055">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1055">x</span></span>  
<span data-ttu-id="ee3e0-1056">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1056">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1057">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1057">y</span></span>  
<span data-ttu-id="ee3e0-1058">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1058">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1059">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1059">button</span></span>  
<span data-ttu-id="ee3e0-1060">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1060">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1061">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1061">Ctrl</span></span>  
<span data-ttu-id="ee3e0-1062">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1062">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1063">シフト</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1063">Shift</span></span>  
<span data-ttu-id="ee3e0-1064">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1064">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="ee3e0-1065">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1065">Return Value - mouseDown</span></span>

<span data-ttu-id="ee3e0-1066">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1066">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="ee3e0-1067">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1067">Remarks - mouseDown</span></span>

<span data-ttu-id="ee3e0-1068">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1068">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="ee3e0-1069">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1069">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="ee3e0-1070">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1070">Method mouseMove</span></span>

<span data-ttu-id="ee3e0-1071">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1071">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="ee3e0-1072">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1072">Parameters - mouseMove</span></span>

<span data-ttu-id="ee3e0-1073">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1073">x</span></span>  
<span data-ttu-id="ee3e0-1074">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1074">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1075">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1075">y</span></span>  
<span data-ttu-id="ee3e0-1076">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1076">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1077">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1077">button</span></span>  
<span data-ttu-id="ee3e0-1078">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1078">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1079">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1079">Ctrl</span></span>  
<span data-ttu-id="ee3e0-1080">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1080">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1081">シフト</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1081">Shift</span></span>  
<span data-ttu-id="ee3e0-1082">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1082">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="ee3e0-1083">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1083">Return Value - mouseMove</span></span>

<span data-ttu-id="ee3e0-1084">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1084">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="ee3e0-1085">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1085">Remarks - mouseMove</span></span>

<span data-ttu-id="ee3e0-1086">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1086">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="ee3e0-1087">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1087">Method mouseUp</span></span>

<span data-ttu-id="ee3e0-1088">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1088">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="ee3e0-1089">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1089">Parameters - mouseUp</span></span>

<span data-ttu-id="ee3e0-1090">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1090">x</span></span>  
<span data-ttu-id="ee3e0-1091">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1091">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1092">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1092">y</span></span>  
<span data-ttu-id="ee3e0-1093">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1093">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1094">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1094">button</span></span>  
<span data-ttu-id="ee3e0-1095">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1095">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1096">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1096">Ctrl</span></span>  
<span data-ttu-id="ee3e0-1097">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1097">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1098">シフト</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1098">Shift</span></span>  
<span data-ttu-id="ee3e0-1099">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1099">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="ee3e0-1100">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1100">Return Value - mouseUp</span></span>

<span data-ttu-id="ee3e0-1101">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1101">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="ee3e0-1102">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1102">Remarks - mouseUp</span></span>

<span data-ttu-id="ee3e0-1103">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1103">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="ee3e0-1104">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1104">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="ee3e0-1105">メソッド名</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1105">Method name</span></span>

<span data-ttu-id="ee3e0-1106">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1106">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="ee3e0-1107">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1107">Parameters - name</span></span>

<span data-ttu-id="ee3e0-1108">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1108">value</span></span>  
<span data-ttu-id="ee3e0-1109">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1109">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="ee3e0-1110">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1110">Return Value - name</span></span>

<span data-ttu-id="ee3e0-1111">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1111">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="ee3e0-1112">備考 - name</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1112">Remarks - name</span></span>

<span data-ttu-id="ee3e0-1113">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1113">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="ee3e0-1114">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1114">It must start with a letter.</span></span>
-   <span data-ttu-id="ee3e0-1115">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1115">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="ee3e0-1116">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1116">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="ee3e0-1117">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1117">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="ee3e0-1118">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1118">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="ee3e0-1119">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1119">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="ee3e0-1120">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1120">Parameters - neededPermission</span></span>

<span data-ttu-id="ee3e0-1121">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1121">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="ee3e0-1122">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1122">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="ee3e0-1123">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1123">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="ee3e0-1124">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1124">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="ee3e0-1125">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1125">Method parentControl</span></span>

<span data-ttu-id="ee3e0-1126">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1126">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="ee3e0-1127">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1127">Return Value - parentControl</span></span>

<span data-ttu-id="ee3e0-1128">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1128">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="ee3e0-1129">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1129">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="ee3e0-1130">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1130">Parameters - previewPartRef</span></span>

<span data-ttu-id="ee3e0-1131">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1131">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="ee3e0-1132">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1132">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="ee3e0-1133">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1133">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="ee3e0-1134">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1134">Parameters - promptrect</span></span>

<span data-ttu-id="ee3e0-1135">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1135">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="ee3e0-1136">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1136">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="ee3e0-1137">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1137">Method securityKey</span></span>

<span data-ttu-id="ee3e0-1138">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1138">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="ee3e0-1139">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1139">Parameters - securityKey</span></span>

<span data-ttu-id="ee3e0-1140">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1140">value</span></span>  
<span data-ttu-id="ee3e0-1141">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1141">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="ee3e0-1142">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1142">Return Value - securityKey</span></span>

<span data-ttu-id="ee3e0-1143">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1143">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="ee3e0-1144">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1144">Method showContextMenu</span></span>

<span data-ttu-id="ee3e0-1145">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1145">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="ee3e0-1146">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1146">Parameters - showContextMenu</span></span>

<span data-ttu-id="ee3e0-1147">menuHandle</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1147">menuHandle</span></span>  
<span data-ttu-id="ee3e0-1148">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1148">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="ee3e0-1149">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1149">Return Value - showContextMenu</span></span>

<span data-ttu-id="ee3e0-1150">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1150">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="ee3e0-1151">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1151">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="ee3e0-1152">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1152">Parameters - showLabel</span></span>

<span data-ttu-id="ee3e0-1153">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1153">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="ee3e0-1154">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1154">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="ee3e0-1155">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1155">Method skip</span></span>

<span data-ttu-id="ee3e0-1156">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1156">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="ee3e0-1157">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1157">Parameters - skip</span></span>

<span data-ttu-id="ee3e0-1158">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1158">value</span></span>  
<span data-ttu-id="ee3e0-1159">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1159">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="ee3e0-1160">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1160">Return Value - skip</span></span>

<span data-ttu-id="ee3e0-1161">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1161">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="ee3e0-1162">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1162">Remarks - skip</span></span>

<span data-ttu-id="ee3e0-1163">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1163">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="ee3e0-1164">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1164">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="ee3e0-1165">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1165">Parameters - sort</span></span>

<span data-ttu-id="ee3e0-1166">sortDirection</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1166">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="ee3e0-1167">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1167">Return Value - sort</span></span>

## <a name="method-timeformat"></a><span data-ttu-id="ee3e0-1168">メソッド timeFormat</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1168">Method timeFormat</span></span>

```xpp
public int timeFormat([int value])
```

### <a name="parameters---timeformat"></a><span data-ttu-id="ee3e0-1169">パラメーター - timeFormat</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1169">Parameters - timeFormat</span></span>

<span data-ttu-id="ee3e0-1170">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1170">value</span></span>  

### <a name="return-value---timeformat"></a><span data-ttu-id="ee3e0-1171">戻り値 - timeFormat</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1171">Return Value - timeFormat</span></span>

## <a name="method-timehours"></a><span data-ttu-id="ee3e0-1172">メソッド timeHours</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1172">Method timeHours</span></span>

```xpp
public int timeHours([int value])
```

### <a name="parameters---timehours"></a><span data-ttu-id="ee3e0-1173">パラメーター - timeHours</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1173">Parameters - timeHours</span></span>

<span data-ttu-id="ee3e0-1174">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1174">value</span></span>  

### <a name="return-value---timehours"></a><span data-ttu-id="ee3e0-1175">戻り値 - timeHours</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1175">Return Value - timeHours</span></span>

## <a name="method-timeminute"></a><span data-ttu-id="ee3e0-1176">メソッド timeMinute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1176">Method timeMinute</span></span>

```xpp
public int timeMinute([int value])
```

### <a name="parameters---timeminute"></a><span data-ttu-id="ee3e0-1177">パラメーター - timeMinute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1177">Parameters - timeMinute</span></span>

<span data-ttu-id="ee3e0-1178">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1178">value</span></span>  

### <a name="return-value---timeminute"></a><span data-ttu-id="ee3e0-1179">戻り値 - timeMinute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1179">Return Value - timeMinute</span></span>

## <a name="method-timeseconds"></a><span data-ttu-id="ee3e0-1180">メソッド timeSeconds</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1180">Method timeSeconds</span></span>

```xpp
public int timeSeconds([int value])
```

### <a name="parameters---timeseconds"></a><span data-ttu-id="ee3e0-1181">パラメーター - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1181">Parameters - timeSeconds</span></span>

<span data-ttu-id="ee3e0-1182">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1182">value</span></span>  

### <a name="return-value---timeseconds"></a><span data-ttu-id="ee3e0-1183">戻り値 - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1183">Return Value - timeSeconds</span></span>

## <a name="method-timeseparator"></a><span data-ttu-id="ee3e0-1184">メソッド timeSeparator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1184">Method timeSeparator</span></span>

```xpp
public int timeSeparator([int value])
```

### <a name="parameters---timeseparator"></a><span data-ttu-id="ee3e0-1185">パラメーター - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1185">Parameters - timeSeparator</span></span>

<span data-ttu-id="ee3e0-1186">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1186">value</span></span>  

### <a name="return-value---timeseparator"></a><span data-ttu-id="ee3e0-1187">戻り値 - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1187">Return Value - timeSeparator</span></span>

## <a name="method-timezone"></a><span data-ttu-id="ee3e0-1188">メソッド timeZone</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1188">Method timeZone</span></span>

```xpp
public Timezone timeZone([Timezone timeZone])
```

### <a name="parameters---timezone"></a><span data-ttu-id="ee3e0-1189">パラメーター - timeZone</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1189">Parameters - timeZone</span></span>

<span data-ttu-id="ee3e0-1190">timeZone</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1190">timeZone</span></span>  

### <a name="return-value---timezone"></a><span data-ttu-id="ee3e0-1191">戻り値 - timeZone</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1191">Return Value - timeZone</span></span>

## <a name="method-timezoneindicator"></a><span data-ttu-id="ee3e0-1192">メソッド timeZoneIndicator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1192">Method timeZoneIndicator</span></span>

```xpp
public int timeZoneIndicator([int value])
```

### <a name="parameters---timezoneindicator"></a><span data-ttu-id="ee3e0-1193">パラメーター - timeZoneIndicator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1193">Parameters - timeZoneIndicator</span></span>

<span data-ttu-id="ee3e0-1194">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1194">value</span></span>  

### <a name="return-value---timezoneindicator"></a><span data-ttu-id="ee3e0-1195">戻り値 - timeZoneIndicator</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1195">Return Value - timeZoneIndicator</span></span>

## <a name="method-timezonepreference"></a><span data-ttu-id="ee3e0-1196">メソッド timezonePreference</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1196">Method timezonePreference</span></span>

```xpp
public int timezonePreference([int value])
```

### <a name="parameters---timezonepreference"></a><span data-ttu-id="ee3e0-1197">パラメーター - timezonePreference</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1197">Parameters - timezonePreference</span></span>

<span data-ttu-id="ee3e0-1198">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1198">value</span></span>  

### <a name="return-value---timezonepreference"></a><span data-ttu-id="ee3e0-1199">戻り値 - timezonePreference</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1199">Return Value - timezonePreference</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="ee3e0-1200">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1200">Method toolTip</span></span>

<span data-ttu-id="ee3e0-1201">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1201">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="ee3e0-1202">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1202">Return Value - toolTip</span></span>

<span data-ttu-id="ee3e0-1203">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1203">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="ee3e0-1204">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1204">Remarks - toolTip</span></span>

<span data-ttu-id="ee3e0-1205">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1205">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="ee3e0-1206">メソッド top</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1206">Method top</span></span>

<span data-ttu-id="ee3e0-1207">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1207">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="ee3e0-1208">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1208">Parameters - top</span></span>

<span data-ttu-id="ee3e0-1209">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1209">value</span></span>  
<span data-ttu-id="ee3e0-1210">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1210">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1211">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1211">mode</span></span>  
<span data-ttu-id="ee3e0-1212">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1212">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="ee3e0-1213">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1213">Return Value - top</span></span>

<span data-ttu-id="ee3e0-1214">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1214">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="ee3e0-1215">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1215">Method topMode</span></span>

<span data-ttu-id="ee3e0-1216">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1216">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="ee3e0-1217">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1217">Parameters - topMode</span></span>

<span data-ttu-id="ee3e0-1218">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1218">value</span></span>  
<span data-ttu-id="ee3e0-1219">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1219">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="ee3e0-1220">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1220">Return Value - topMode</span></span>

<span data-ttu-id="ee3e0-1221">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1221">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="ee3e0-1222">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1222">Method topValue</span></span>

<span data-ttu-id="ee3e0-1223">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1223">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="ee3e0-1224">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1224">Parameters - topValue</span></span>

<span data-ttu-id="ee3e0-1225">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1225">value</span></span>  
<span data-ttu-id="ee3e0-1226">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1226">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="ee3e0-1227">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1227">Return Value - topValue</span></span>

<span data-ttu-id="ee3e0-1228">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1228">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="ee3e0-1229">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1229">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="ee3e0-1230">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1230">Parameters - type</span></span>

<span data-ttu-id="ee3e0-1231">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1231">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="ee3e0-1232">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1232">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="ee3e0-1233">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1233">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="ee3e0-1234">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1234">Parameters - underline</span></span>

<span data-ttu-id="ee3e0-1235">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1235">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="ee3e0-1236">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1236">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="ee3e0-1237">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1237">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="ee3e0-1238">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1238">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="ee3e0-1239">データ</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1239">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="ee3e0-1240">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1240">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="ee3e0-1241">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1241">Method userData</span></span>

<span data-ttu-id="ee3e0-1242">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1242">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="ee3e0-1243">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1243">Parameters - userData</span></span>

<span data-ttu-id="ee3e0-1244">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1244">value</span></span>  
<span data-ttu-id="ee3e0-1245">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1245">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="ee3e0-1246">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1246">Return Value - userData</span></span>

<span data-ttu-id="ee3e0-1247">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1247">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="ee3e0-1248">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1248">Method userDataItem</span></span>

<span data-ttu-id="ee3e0-1249">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1249">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="ee3e0-1250">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1250">Parameters - userDataItem</span></span>

<span data-ttu-id="ee3e0-1251">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1251">value</span></span>  
<span data-ttu-id="ee3e0-1252">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1252">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="ee3e0-1253">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1253">Return Value - userDataItem</span></span>

<span data-ttu-id="ee3e0-1254">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1254">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="ee3e0-1255">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1255">Method userDataItems</span></span>

<span data-ttu-id="ee3e0-1256">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1256">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="ee3e0-1257">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1257">Parameters - userDataItems</span></span>

<span data-ttu-id="ee3e0-1258">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1258">value</span></span>  
<span data-ttu-id="ee3e0-1259">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1259">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="ee3e0-1260">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1260">Return Value - userDataItems</span></span>

<span data-ttu-id="ee3e0-1261">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1261">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="ee3e0-1262">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1262">Method userDisable</span></span>

<span data-ttu-id="ee3e0-1263">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1263">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="ee3e0-1264">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1264">Parameters - userDisable</span></span>

<span data-ttu-id="ee3e0-1265">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1265">value</span></span>  
<span data-ttu-id="ee3e0-1266">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1266">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="ee3e0-1267">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1267">Return Value - userDisable</span></span>

<span data-ttu-id="ee3e0-1268">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1268">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userfasttabsummary"></a><span data-ttu-id="ee3e0-1269">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1269">Method userFastTabSummary</span></span>

```xpp
public int userFastTabSummary([int value])
```

### <a name="parameters---userfasttabsummary"></a><span data-ttu-id="ee3e0-1270">パラメーター - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1270">Parameters - userFastTabSummary</span></span>

<span data-ttu-id="ee3e0-1271">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1271">value</span></span>  

### <a name="return-value---userfasttabsummary"></a><span data-ttu-id="ee3e0-1272">戻り値 - userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1272">Return Value - userFastTabSummary</span></span>

## <a name="method-userheight"></a><span data-ttu-id="ee3e0-1273">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1273">Method userHeight</span></span>

<span data-ttu-id="ee3e0-1274">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1274">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="ee3e0-1275">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1275">Parameters - userHeight</span></span>

<span data-ttu-id="ee3e0-1276">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1276">value</span></span>  
<span data-ttu-id="ee3e0-1277">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1277">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="ee3e0-1278">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1278">Return Value - userHeight</span></span>

<span data-ttu-id="ee3e0-1279">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1279">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="ee3e0-1280">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1280">Method userHide</span></span>

<span data-ttu-id="ee3e0-1281">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1281">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="ee3e0-1282">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1282">Parameters - userHide</span></span>

<span data-ttu-id="ee3e0-1283">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1283">value</span></span>  
<span data-ttu-id="ee3e0-1284">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1284">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="ee3e0-1285">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1285">Return Value - userHide</span></span>

<span data-ttu-id="ee3e0-1286">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1286">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="ee3e0-1287">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1287">Remarks - userHide</span></span>

<span data-ttu-id="ee3e0-1288">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1288">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="ee3e0-1289">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1289">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="ee3e0-1290">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1290">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="ee3e0-1291">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1291">Method userOrgContainer</span></span>

<span data-ttu-id="ee3e0-1292">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1292">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="ee3e0-1293">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1293">Parameters - userOrgContainer</span></span>

<span data-ttu-id="ee3e0-1294">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1294">value</span></span>  
<span data-ttu-id="ee3e0-1295">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1295">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="ee3e0-1296">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1296">Return Value - userOrgContainer</span></span>

<span data-ttu-id="ee3e0-1297">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1297">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="ee3e0-1298">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1298">Method userOrgSibling</span></span>

<span data-ttu-id="ee3e0-1299">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1299">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="ee3e0-1300">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1300">Parameters - userOrgSibling</span></span>

<span data-ttu-id="ee3e0-1301">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1301">value</span></span>  
<span data-ttu-id="ee3e0-1302">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1302">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="ee3e0-1303">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1303">Return Value - userOrgSibling</span></span>

<span data-ttu-id="ee3e0-1304">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1304">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="ee3e0-1305">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1305">Method userPromptText</span></span>

<span data-ttu-id="ee3e0-1306">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1306">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="ee3e0-1307">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1307">Parameters - userPromptText</span></span>

<span data-ttu-id="ee3e0-1308">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1308">value</span></span>  
<span data-ttu-id="ee3e0-1309">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1309">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="ee3e0-1310">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1310">Return Value - userPromptText</span></span>

<span data-ttu-id="ee3e0-1311">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1311">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="ee3e0-1312">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1312">Method userSecurityLevel</span></span>

<span data-ttu-id="ee3e0-1313">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1313">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="ee3e0-1314">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1314">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="ee3e0-1315">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1315">value</span></span>  
<span data-ttu-id="ee3e0-1316">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1316">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="ee3e0-1317">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1317">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="ee3e0-1318">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1318">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="ee3e0-1319">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1319">Method userSkip</span></span>

<span data-ttu-id="ee3e0-1320">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1320">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="ee3e0-1321">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1321">Parameters - userSkip</span></span>

<span data-ttu-id="ee3e0-1322">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1322">value</span></span>  
<span data-ttu-id="ee3e0-1323">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1323">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="ee3e0-1324">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1324">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="ee3e0-1325">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1325">Return Value - userSkip</span></span>

<span data-ttu-id="ee3e0-1326">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1326">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="ee3e0-1327">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1327">Method userWidth</span></span>

<span data-ttu-id="ee3e0-1328">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1328">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="ee3e0-1329">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1329">Parameters - userWidth</span></span>

<span data-ttu-id="ee3e0-1330">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1330">value</span></span>  
<span data-ttu-id="ee3e0-1331">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1331">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="ee3e0-1332">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1332">Return Value - userWidth</span></span>

<span data-ttu-id="ee3e0-1333">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1333">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="ee3e0-1334">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1334">Remarks - userWidth</span></span>

<span data-ttu-id="ee3e0-1335">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1335">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="ee3e0-1336">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1336">For example, if the user has specified 30 characters as the width for the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="ee3e0-1337">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1337">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="ee3e0-1338">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1338">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="ee3e0-1339">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1339">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="ee3e0-1340">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1340">Method verticalSpacing</span></span>

<span data-ttu-id="ee3e0-1341">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1341">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="ee3e0-1342">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1342">Parameters - verticalSpacing</span></span>

<span data-ttu-id="ee3e0-1343">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1343">value</span></span>  
<span data-ttu-id="ee3e0-1344">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1344">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1345">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1345">mode</span></span>  
<span data-ttu-id="ee3e0-1346">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1346">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="ee3e0-1347">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1347">Return Value - verticalSpacing</span></span>

<span data-ttu-id="ee3e0-1348">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1348">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="ee3e0-1349">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1349">Method verticalSpacingMode</span></span>

<span data-ttu-id="ee3e0-1350">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1350">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="ee3e0-1351">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1351">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="ee3e0-1352">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1352">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="ee3e0-1353">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1353">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="ee3e0-1354">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1354">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="ee3e0-1355">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1355">Method verticalSpacingValue</span></span>

<span data-ttu-id="ee3e0-1356">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1356">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="ee3e0-1357">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1357">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="ee3e0-1358">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1358">value</span></span>  
<span data-ttu-id="ee3e0-1359">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1359">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="ee3e0-1360">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1360">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="ee3e0-1361">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1361">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="ee3e0-1362">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1362">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="ee3e0-1363">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1363">Parameters - viewEditMode</span></span>

<span data-ttu-id="ee3e0-1364">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1364">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="ee3e0-1365">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1365">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="ee3e0-1366">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1366">Method visible</span></span>

<span data-ttu-id="ee3e0-1367">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1367">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="ee3e0-1368">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1368">Parameters - visible</span></span>

<span data-ttu-id="ee3e0-1369">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1369">value</span></span>  
<span data-ttu-id="ee3e0-1370">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1370">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="ee3e0-1371">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1371">Return Value - visible</span></span>

<span data-ttu-id="ee3e0-1372">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1372">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="ee3e0-1373">メソッド width</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1373">Method width</span></span>

<span data-ttu-id="ee3e0-1374">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1374">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="ee3e0-1375">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1375">Parameters - width</span></span>

<span data-ttu-id="ee3e0-1376">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1376">value</span></span>  
<span data-ttu-id="ee3e0-1377">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1377">An Integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1378">モード</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1378">mode</span></span>  
<span data-ttu-id="ee3e0-1379">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1379">An Integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="ee3e0-1380">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1380">Return Value - width</span></span>

<span data-ttu-id="ee3e0-1381">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1381">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="ee3e0-1382">備考 - width</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1382">Remarks - width</span></span>

<span data-ttu-id="ee3e0-1383">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1383">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="ee3e0-1384">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1384">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ee3e0-1385">モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1385">Mode.</span></span>           | <span data-ttu-id="ee3e0-1386">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1386">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e0-1387">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1387">-1 Exact.</span></span>       | <span data-ttu-id="ee3e0-1388">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1388">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee3e0-1389">0 自動。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1389">0 Auto.</span></span>         | <span data-ttu-id="ee3e0-1390">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1390">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee3e0-1391">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1391">1 Column width.</span></span> | <span data-ttu-id="ee3e0-1392">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1392">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ee3e0-1393">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1393">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="ee3e0-1394">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1394">Method widthMode</span></span>

<span data-ttu-id="ee3e0-1395">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1395">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="ee3e0-1396">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1396">Parameters - widthMode</span></span>

<span data-ttu-id="ee3e0-1397">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1397">value</span></span>  
<span data-ttu-id="ee3e0-1398">コントロールの幅の計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1398">An Integer data type value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="ee3e0-1399">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1399">Return Value - widthMode</span></span>

<span data-ttu-id="ee3e0-1400">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1400">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="ee3e0-1401">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1401">Remarks - widthMode</span></span>

<span data-ttu-id="ee3e0-1402">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1402">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="ee3e0-1403">モード。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1403">Mode.</span></span>         | <span data-ttu-id="ee3e0-1404">幅計算。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1404">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3e0-1405">正確。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1405">Exact.</span></span>        | <span data-ttu-id="ee3e0-1406">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1406">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="ee3e0-1407">自動。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1407">Auto.</span></span>         | <span data-ttu-id="ee3e0-1408">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1408">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="ee3e0-1409">列の幅。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1409">Column width.</span></span> | <span data-ttu-id="ee3e0-1410">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1410">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="ee3e0-1411">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1411">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="ee3e0-1412">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1412">Method widthValue</span></span>

<span data-ttu-id="ee3e0-1413">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1413">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="ee3e0-1414">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1414">Parameters - widthValue</span></span>

<span data-ttu-id="ee3e0-1415">値</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1415">value</span></span>  
<span data-ttu-id="ee3e0-1416">幅をピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1416">An Integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="ee3e0-1417">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1417">Return Value - widthValue</span></span>

<span data-ttu-id="ee3e0-1418">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1418">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="ee3e0-1419">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1419">Remarks - widthValue</span></span>

<span data-ttu-id="ee3e0-1420">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1420">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-gotfocus"></a><span data-ttu-id="ee3e0-1421">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1421">Method gotFocus</span></span>

<span data-ttu-id="ee3e0-1422">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1422">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-paste"></a><span data-ttu-id="ee3e0-1423">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1423">Method paste</span></span>

<span data-ttu-id="ee3e0-1424">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1424">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-performtypelookup"></a><span data-ttu-id="ee3e0-1425">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1425">Method performTypeLookup</span></span>

```xpp
public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])
```

### <a name="parameters---performtypelookup"></a><span data-ttu-id="ee3e0-1426">パラメーター - performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1426">Parameters - performTypeLookup</span></span>

<span data-ttu-id="ee3e0-1427">userType</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1427">userType</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1428">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1428">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1429">会社</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1429">company</span></span>  

## <a name="method-copy"></a><span data-ttu-id="ee3e0-1430">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1430">Method copy</span></span>

<span data-ttu-id="ee3e0-1431">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1431">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-drop"></a><span data-ttu-id="ee3e0-1432">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1432">Method drop</span></span>

<span data-ttu-id="ee3e0-1433">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1433">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="ee3e0-1434">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1434">Parameters - drop</span></span>

<span data-ttu-id="ee3e0-1435">dragSource</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1435">dragSource</span></span>  
<span data-ttu-id="ee3e0-1436">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1436">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1437">dragMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1437">dragMode</span></span>  
<span data-ttu-id="ee3e0-1438">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1438">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1439">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1439">x</span></span>  
<span data-ttu-id="ee3e0-1440">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1440">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1441">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1441">y</span></span>  
<span data-ttu-id="ee3e0-1442">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1442">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onvalidating"></a><span data-ttu-id="ee3e0-1443">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1443">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="ee3e0-1444">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1444">Parameters - OnValidating</span></span>

<span data-ttu-id="ee3e0-1445">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1445">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1446">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1446">e</span></span>  

## <a name="method-cut"></a><span data-ttu-id="ee3e0-1447">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1447">Method cut</span></span>

<span data-ttu-id="ee3e0-1448">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1448">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-enddrag"></a><span data-ttu-id="ee3e0-1449">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1449">Method endDrag</span></span>

<span data-ttu-id="ee3e0-1450">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1450">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="ee3e0-1451">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1451">Remarks - endDrag</span></span>

<span data-ttu-id="ee3e0-1452">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1452">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="ee3e0-1453">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1453">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="ee3e0-1454">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1454">Method mouseEnter</span></span>

<span data-ttu-id="ee3e0-1455">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1455">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="ee3e0-1456">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1456">Parameters - mouseEnter</span></span>

<span data-ttu-id="ee3e0-1457">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1457">x</span></span>  
<span data-ttu-id="ee3e0-1458">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1458">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1459">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1459">y</span></span>  
<span data-ttu-id="ee3e0-1460">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1460">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1461">ボタン</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1461">button</span></span>  
<span data-ttu-id="ee3e0-1462">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1462">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1463">Ctrl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1463">Ctrl</span></span>  
<span data-ttu-id="ee3e0-1464">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1464">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1465">シフト</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1465">Shift</span></span>  
<span data-ttu-id="ee3e0-1466">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1466">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="ee3e0-1467">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1467">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="ee3e0-1468">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1468">Parameters - OnEnter</span></span>

<span data-ttu-id="ee3e0-1469">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1469">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1470">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1470">e</span></span>  

## <a name="method-timetextchange"></a><span data-ttu-id="ee3e0-1471">メソッド timeTextChange</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1471">Method timeTextChange</span></span>

```xpp
public void timeTextChange()
```

## <a name="method-performdblookup"></a><span data-ttu-id="ee3e0-1472">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1472">Method performDBLookup</span></span>

```xpp
public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])
```

### <a name="parameters---performdblookup"></a><span data-ttu-id="ee3e0-1473">パラメーター - performDBLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1473">Parameters - performDBLookup</span></span>

<span data-ttu-id="ee3e0-1474">fieldId</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1474">fieldId</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1475">tableId</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1475">tableId</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1476">会社</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1476">company</span></span>  

## <a name="method-datetextchange"></a><span data-ttu-id="ee3e0-1477">メソッド dateTextChange</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1477">Method dateTextChange</span></span>

```xpp
public void dateTextChange()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="ee3e0-1478">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1478">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="ee3e0-1479">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1479">Parameters - OnLostFocus</span></span>

<span data-ttu-id="ee3e0-1480">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1480">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1481">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1481">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="ee3e0-1482">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1482">Method prefColumnSize</span></span>

<span data-ttu-id="ee3e0-1483">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1483">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="ee3e0-1484">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1484">Parameters - prefColumnSize</span></span>

<span data-ttu-id="ee3e0-1485">width</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1485">width</span></span>  
<span data-ttu-id="ee3e0-1486">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1486">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1487">height</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1487">height</span></span>  
<span data-ttu-id="ee3e0-1488">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1488">The preferred height of the control.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="ee3e0-1489">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1489">Method displayControl</span></span>

<span data-ttu-id="ee3e0-1490">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1490">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="ee3e0-1491">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1491">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="ee3e0-1492">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1492">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="ee3e0-1493">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1493">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1494">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1494">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1495">overrideObject</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1495">overrideObject</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="ee3e0-1496">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1496">Method lostFocus</span></span>

<span data-ttu-id="ee3e0-1497">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1497">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-inputsearch"></a><span data-ttu-id="ee3e0-1498">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1498">Method inputSearch</span></span>

<span data-ttu-id="ee3e0-1499">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1499">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="ee3e0-1500">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1500">Parameters - inputSearch</span></span>

<span data-ttu-id="ee3e0-1501">searchStr</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1501">searchStr</span></span>  
<span data-ttu-id="ee3e0-1502">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1502">The string value to use to filter data; optional.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="ee3e0-1503">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1503">Method mouseLeave</span></span>

<span data-ttu-id="ee3e0-1504">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1504">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-enter"></a><span data-ttu-id="ee3e0-1505">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1505">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-setfocus"></a><span data-ttu-id="ee3e0-1506">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1506">Method setFocus</span></span>

<span data-ttu-id="ee3e0-1507">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1507">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-dropex"></a><span data-ttu-id="ee3e0-1508">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1508">Method dropEx</span></span>

<span data-ttu-id="ee3e0-1509">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1509">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="ee3e0-1510">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1510">Parameters - dropEx</span></span>

<span data-ttu-id="ee3e0-1511">dragSource</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1511">dragSource</span></span>  
<span data-ttu-id="ee3e0-1512">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1512">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1513">dragMode</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1513">dragMode</span></span>  
<span data-ttu-id="ee3e0-1514">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1514">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1515">x</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1515">x</span></span>  
<span data-ttu-id="ee3e0-1516">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1516">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="ee3e0-1517">y</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1517">y</span></span>  
<span data-ttu-id="ee3e0-1518">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1518">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-filter"></a><span data-ttu-id="ee3e0-1519">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1519">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="ee3e0-1520">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1520">Parameters - filter</span></span>

<span data-ttu-id="ee3e0-1521">filterStr</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1521">filterStr</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="ee3e0-1522">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1522">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="ee3e0-1523">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1523">Parameters - OnValidated</span></span>

<span data-ttu-id="ee3e0-1524">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1524">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1525">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1525">e</span></span>  

## <a name="method-performformlookup"></a><span data-ttu-id="ee3e0-1526">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1526">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="ee3e0-1527">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1527">Parameters - performFormLookup</span></span>

<span data-ttu-id="ee3e0-1528">フォーム</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1528">form</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="ee3e0-1529">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1529">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="ee3e0-1530">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1530">Parameters - OnLeaving</span></span>

<span data-ttu-id="ee3e0-1531">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1531">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1532">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1532">e</span></span>  

## <a name="method-lookup"></a><span data-ttu-id="ee3e0-1533">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1533">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-onlookup"></a><span data-ttu-id="ee3e0-1534">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1534">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="ee3e0-1535">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1535">Parameters - OnLookup</span></span>

<span data-ttu-id="ee3e0-1536">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1536">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1537">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1537">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="ee3e0-1538">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1538">Method dragLeave</span></span>

<span data-ttu-id="ee3e0-1539">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1539">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="ee3e0-1540">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1540">Method resetUserSetting</span></span>

<span data-ttu-id="ee3e0-1541">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1541">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-context"></a><span data-ttu-id="ee3e0-1542">メソッド context</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1542">Method context</span></span>

<span data-ttu-id="ee3e0-1543">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1543">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-undo"></a><span data-ttu-id="ee3e0-1544">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1544">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-setutcstring"></a><span data-ttu-id="ee3e0-1545">メソッド setUTCString</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1545">Method setUTCString</span></span>

```xpp
public void setUTCString(str UTC_Formatted String)
```

### <a name="parameters---setutcstring"></a><span data-ttu-id="ee3e0-1546">パラメーター - setUTCString</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1546">Parameters - setUTCString</span></span>

<span data-ttu-id="ee3e0-1547">UTC\_書式設定された文字列</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1547">UTC\_Formatted String</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="ee3e0-1548">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1548">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="ee3e0-1549">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1549">Parameters - OnModified</span></span>

<span data-ttu-id="ee3e0-1550">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1550">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1551">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1551">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="ee3e0-1552">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1552">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="ee3e0-1553">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1553">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="ee3e0-1554">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1554">Parameters - OnGotFocus</span></span>

<span data-ttu-id="ee3e0-1555">sender</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1555">sender</span></span>  

<!-- -->

<span data-ttu-id="ee3e0-1556">e</span><span class="sxs-lookup"><span data-stu-id="ee3e0-1556">e</span></span>  

