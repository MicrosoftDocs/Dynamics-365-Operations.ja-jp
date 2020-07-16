---
title: FormListBoxControl クラス
description: このトピックでは、FormListBoxControl クラスについて説明します。
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
ms.openlocfilehash: b6bec3aa8fda36b35bc7b94d064f16d68cc651cc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502932"
---
# <a name="class-formlistboxcontrol"></a><span data-ttu-id="3928b-103">クラス FormListBoxControl</span><span class="sxs-lookup"><span data-stu-id="3928b-103">Class FormListBoxControl</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormListBoxControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="3928b-104">備考</span><span class="sxs-lookup"><span data-stu-id="3928b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3928b-105">例</span><span class="sxs-lookup"><span data-stu-id="3928b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3928b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3928b-106">Methods</span></span>

| <span data-ttu-id="3928b-107">方法</span><span class="sxs-lookup"><span data-stu-id="3928b-107">Method</span></span>                                                                                                      | <span data-ttu-id="3928b-108">説明</span><span class="sxs-lookup"><span data-stu-id="3928b-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3928b-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="3928b-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3928b-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="3928b-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-112">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="3928b-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="3928b-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="3928b-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="3928b-115">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-115">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="3928b-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="3928b-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="3928b-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-119">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="3928b-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="3928b-121">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-121">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="3928b-122">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3928b-122">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="3928b-123">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-123">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="3928b-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-124">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="3928b-125">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-125">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="3928b-126">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-126">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="3928b-127">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-127">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="3928b-128">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-128">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-129">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="3928b-129">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="3928b-130">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-130">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="3928b-131">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-131">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="3928b-132">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-132">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="3928b-133">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-133">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="3928b-134">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-134">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="3928b-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-135">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="3928b-136">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-136">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="3928b-137">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="3928b-137">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="3928b-138">コントロールでチェックされているコンフィギュレーション キーの名前を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-138">Retrieves a list that contains the names of configuration keys that are checked for the control.</span></span>                                                                        |
| <span data-ttu-id="3928b-139">public int count()</span><span class="sxs-lookup"><span data-stu-id="3928b-139">public int count()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="3928b-140">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-140">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="3928b-141">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-141">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="3928b-142">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-142">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-143">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-143">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-144">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-144">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-145">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-145">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="3928b-146">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-146">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="3928b-147">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-147">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="3928b-148">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-148">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="3928b-149">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-149">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="3928b-150">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-150">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-151">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-151">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="3928b-152">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-152">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="3928b-153">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-153">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="3928b-154">public int doubleClick()</span><span class="sxs-lookup"><span data-stu-id="3928b-154">public int doubleClick()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-155">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-155">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="3928b-156">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-156">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="3928b-157">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3928b-157">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="3928b-158">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-158">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="3928b-159">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3928b-159">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="3928b-160">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-160">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="3928b-161">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="3928b-161">public str dragText()</span></span>                                                                                       | <span data-ttu-id="3928b-162">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-162">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="3928b-163">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-163">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="3928b-164">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-164">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="3928b-165">public EnumId enumType(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-165">public EnumId enumType(\[EnumId value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-166">public EnumId enumTypeValue()</span><span class="sxs-lookup"><span data-stu-id="3928b-166">public EnumId enumTypeValue()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="3928b-167">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-167">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="3928b-168">public int find(str string)</span><span class="sxs-lookup"><span data-stu-id="3928b-168">public int find(str string)</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-169">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-169">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="3928b-170">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-170">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="3928b-171">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-171">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="3928b-172">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-172">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="3928b-173">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-173">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="3928b-174">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-174">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="3928b-175">public str getText(int index)</span><span class="sxs-lookup"><span data-stu-id="3928b-175">public str getText(int index)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="3928b-176">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="3928b-176">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="3928b-177">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-177">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="3928b-178">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="3928b-178">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="3928b-179">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-179">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="3928b-180">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-180">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="3928b-181">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-181">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="3928b-182">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-182">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="3928b-183">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-183">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="3928b-184">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-184">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="3928b-185">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-185">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="3928b-186">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="3928b-186">public str helpField()</span></span>                                                                                      | <span data-ttu-id="3928b-187">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-187">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3928b-188">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-188">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="3928b-189">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-189">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="3928b-190">public boolean hideFirstEntry(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-190">public boolean hideFirstEntry(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="3928b-191">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-191">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="3928b-192">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-192">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="3928b-193">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="3928b-193">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="3928b-194">コントロールの Windows ハンドル (hWnd) を返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-194">Returns the Windows handle (hWnd) of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="3928b-195">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="3928b-195">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="3928b-196">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="3928b-196">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="3928b-197">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-197">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="3928b-198">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="3928b-198">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="3928b-199">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-199">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="3928b-200">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="3928b-200">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="3928b-201">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-201">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="3928b-202">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="3928b-202">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-203">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-203">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-204">public int item(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-204">public int item(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3928b-205">public int items(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-205">public int items(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="3928b-206">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-206">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="3928b-207">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-207">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="3928b-208">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-208">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-209">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-209">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3928b-210">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-210">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-211">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-211">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3928b-212">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-212">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="3928b-213">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-213">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3928b-214">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-214">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-215">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-215">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="3928b-216">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-216">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-217">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-217">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="3928b-218">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-218">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="3928b-219">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-219">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-220">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-220">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="3928b-221">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-221">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="3928b-222">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-222">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="3928b-223">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-223">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="3928b-224">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-224">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3928b-225">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-225">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-226">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-226">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-227">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="3928b-227">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="3928b-228">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-228">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="3928b-229">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-229">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="3928b-230">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-230">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="3928b-231">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-231">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="3928b-232">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-232">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="3928b-233">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-233">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="3928b-234">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-234">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="3928b-235">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="3928b-235">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="3928b-236">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="3928b-236">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-237">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-237">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="3928b-238">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-238">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="3928b-239">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-239">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="3928b-240">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-240">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="3928b-241">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-241">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="3928b-242">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-242">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="3928b-243">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-243">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="3928b-244">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-244">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="3928b-245">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-245">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="3928b-246">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-246">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="3928b-247">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-247">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="3928b-248">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="3928b-248">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="3928b-249">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="3928b-249">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="3928b-250">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-250">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="3928b-251">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-251">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-252">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-252">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-253">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-253">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="3928b-254">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-254">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="3928b-255">public int selection(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-255">public int selection(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3928b-256">public int selectionChange()</span><span class="sxs-lookup"><span data-stu-id="3928b-256">public int selectionChange()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="3928b-257">public int selectText(str string)</span><span class="sxs-lookup"><span data-stu-id="3928b-257">public int selectText(str string)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="3928b-258">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="3928b-258">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="3928b-259">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-259">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3928b-260">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-260">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-261">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-261">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="3928b-262">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-262">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="3928b-263">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="3928b-263">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="3928b-264">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-264">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3928b-265">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="3928b-265">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="3928b-266">コントロールのツールヒントを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-266">Retrieves a tooltip for the control.</span></span>                                                                                                                                    |
| <span data-ttu-id="3928b-267">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-267">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="3928b-268">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-268">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="3928b-269">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-269">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="3928b-270">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-270">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="3928b-271">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-271">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="3928b-272">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-272">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="3928b-273">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-273">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3928b-274">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-274">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="3928b-275">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-275">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="3928b-276">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="3928b-276">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3928b-277">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-277">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="3928b-278">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-278">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="3928b-279">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-279">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="3928b-280">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-280">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="3928b-281">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-281">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="3928b-282">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-282">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="3928b-283">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-283">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="3928b-284">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-284">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="3928b-285">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-285">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="3928b-286">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-286">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="3928b-287">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-287">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="3928b-288">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-288">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="3928b-289">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-289">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="3928b-290">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-290">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="3928b-291">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-291">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="3928b-292">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-292">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="3928b-293">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-293">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="3928b-294">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-294">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="3928b-295">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-295">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="3928b-296">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-296">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="3928b-297">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-297">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="3928b-298">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-298">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="3928b-299">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-299">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="3928b-300">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-300">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="3928b-301">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="3928b-301">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-302">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-302">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="3928b-303">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-303">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="3928b-304">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-304">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="3928b-305">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-305">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="3928b-306">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-306">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="3928b-307">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-307">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="3928b-308">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-308">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="3928b-309">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-309">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="3928b-310">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-310">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="3928b-311">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3928b-311">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="3928b-312">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-312">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="3928b-313">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-313">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="3928b-314">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-314">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="3928b-315">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3928b-315">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="3928b-316">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-316">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="3928b-317">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="3928b-317">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="3928b-318">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-318">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="3928b-319">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="3928b-319">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="3928b-320">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-320">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="3928b-321">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="3928b-321">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="3928b-322">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-322">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="3928b-323">public void copy()</span><span class="sxs-lookup"><span data-stu-id="3928b-323">public void copy()</span></span>                                                                                          | <span data-ttu-id="3928b-324">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="3928b-324">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="3928b-325">public void cut()</span><span class="sxs-lookup"><span data-stu-id="3928b-325">public void cut()</span></span>                                                                                           | <span data-ttu-id="3928b-326">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="3928b-326">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="3928b-327">public void insert(str string, int index)</span><span class="sxs-lookup"><span data-stu-id="3928b-327">public void insert(str string, int index)</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-328">public void delete(str string)</span><span class="sxs-lookup"><span data-stu-id="3928b-328">public void delete(str string)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3928b-329">public void context()</span><span class="sxs-lookup"><span data-stu-id="3928b-329">public void context()</span></span>                                                                                       | <span data-ttu-id="3928b-330">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-330">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3928b-331">public void enter()</span><span class="sxs-lookup"><span data-stu-id="3928b-331">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3928b-332">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="3928b-332">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="3928b-333">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-333">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="3928b-334">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="3928b-334">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="3928b-335">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="3928b-335">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="3928b-336">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="3928b-336">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="3928b-337">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-337">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="3928b-338">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3928b-338">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="3928b-339">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-339">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="3928b-340">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3928b-340">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="3928b-341">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-341">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="3928b-342">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="3928b-342">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="3928b-343">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-343">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="3928b-344">public void paste()</span><span class="sxs-lookup"><span data-stu-id="3928b-344">public void paste()</span></span>                                                                                         | <span data-ttu-id="3928b-345">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="3928b-345">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="3928b-346">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="3928b-346">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="3928b-347">public void add(str string)</span><span class="sxs-lookup"><span data-stu-id="3928b-347">public void add(str string)</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-348">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-348">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="3928b-349">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-349">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-350">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3928b-350">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="3928b-351">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-351">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="3928b-352">public void undo()</span><span class="sxs-lookup"><span data-stu-id="3928b-352">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="3928b-353">public void endUpdate()</span><span class="sxs-lookup"><span data-stu-id="3928b-353">public void endUpdate()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="3928b-354">public void clear()</span><span class="sxs-lookup"><span data-stu-id="3928b-354">public void clear()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3928b-355">public void beginUpdate()</span><span class="sxs-lookup"><span data-stu-id="3928b-355">public void beginUpdate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-356">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="3928b-356">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="3928b-357">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-357">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="3928b-358">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-358">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="3928b-359">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="3928b-359">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="3928b-360">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="3928b-360">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="3928b-361">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-361">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-362">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="3928b-362">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3928b-363">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="3928b-363">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="3928b-364">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-364">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="3928b-365">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="3928b-365">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="3928b-366">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-366">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="3928b-367">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="3928b-367">public void displayControl()</span></span>                                                                                | <span data-ttu-id="3928b-368">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-368">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="3928b-369">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-369">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="3928b-370">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-370">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="3928b-371">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-371">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                         |                                                                                                                                                                         |
| <span data-ttu-id="3928b-372">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3928b-372">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="3928b-373">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="3928b-373">Method alignControl</span></span>

<span data-ttu-id="3928b-374">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-374">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="3928b-375">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="3928b-375">Parameters - alignControl</span></span>

<span data-ttu-id="3928b-376">値</span><span class="sxs-lookup"><span data-stu-id="3928b-376">value</span></span>  
<span data-ttu-id="3928b-377">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-377">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="3928b-378">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="3928b-378">Return Value - alignControl</span></span>

<span data-ttu-id="3928b-379">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3928b-379">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="3928b-380">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="3928b-380">Remarks - alignControl</span></span>

<span data-ttu-id="3928b-381">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-381">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="3928b-382">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="3928b-382">Method allowEdit</span></span>

<span data-ttu-id="3928b-383">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-383">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="3928b-384">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3928b-384">Parameters - allowEdit</span></span>

<span data-ttu-id="3928b-385">値</span><span class="sxs-lookup"><span data-stu-id="3928b-385">value</span></span>  
<span data-ttu-id="3928b-386">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="3928b-386">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="3928b-387">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3928b-387">Return Value - allowEdit</span></span>

<span data-ttu-id="3928b-388">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3928b-388">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="3928b-389">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3928b-389">Remarks - allowEdit</span></span>

<span data-ttu-id="3928b-390">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="3928b-390">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="3928b-391">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="3928b-391">Method allowSysSetup</span></span>

<span data-ttu-id="3928b-392">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-392">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="3928b-393">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="3928b-393">Return Value - allowSysSetup</span></span>

<span data-ttu-id="3928b-394">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3928b-394">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="3928b-395">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="3928b-395">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="3928b-396">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="3928b-396">Parameters - arrayIndex</span></span>

<span data-ttu-id="3928b-397">値</span><span class="sxs-lookup"><span data-stu-id="3928b-397">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="3928b-398">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="3928b-398">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="3928b-399">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3928b-399">Method autoDeclaration</span></span>

<span data-ttu-id="3928b-400">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-400">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="3928b-401">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3928b-401">Parameters - autoDeclaration</span></span>

<span data-ttu-id="3928b-402">値</span><span class="sxs-lookup"><span data-stu-id="3928b-402">value</span></span>  
<span data-ttu-id="3928b-403">プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-403">The value to assign to the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="3928b-404">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3928b-404">Return Value - autoDeclaration</span></span>

<span data-ttu-id="3928b-405">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3928b-405">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="3928b-406">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3928b-406">Remarks - autoDeclaration</span></span>

<span data-ttu-id="3928b-407">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="3928b-407">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="3928b-408">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-408">Method backgroundColor</span></span>

<span data-ttu-id="3928b-409">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-409">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="3928b-410">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-410">Parameters - backgroundColor</span></span>

<span data-ttu-id="3928b-411">値</span><span class="sxs-lookup"><span data-stu-id="3928b-411">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="3928b-412">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-412">Return Value - backgroundColor</span></span>

<span data-ttu-id="3928b-413">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="3928b-413">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="3928b-414">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-414">Remarks - backgroundColor</span></span>

<span data-ttu-id="3928b-415">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3928b-415">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="3928b-416">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3928b-416">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="3928b-417">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3928b-417">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="3928b-418">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3928b-418">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="3928b-419">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3928b-419">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="3928b-420">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="3928b-420">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="3928b-421">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="3928b-421">Method backStyle</span></span>

<span data-ttu-id="3928b-422">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-422">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="3928b-423">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="3928b-423">Parameters - backStyle</span></span>

<span data-ttu-id="3928b-424">値</span><span class="sxs-lookup"><span data-stu-id="3928b-424">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="3928b-425">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="3928b-425">Return Value - backStyle</span></span>

<span data-ttu-id="3928b-426">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="3928b-426">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="3928b-427">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="3928b-427">Method beginDrag</span></span>

<span data-ttu-id="3928b-428">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-428">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="3928b-429">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="3928b-429">Parameters - beginDrag</span></span>

<span data-ttu-id="3928b-430">x</span><span class="sxs-lookup"><span data-stu-id="3928b-430">x</span></span>  
<span data-ttu-id="3928b-431">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-431">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="3928b-432">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="3928b-432">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="3928b-433">y</span><span class="sxs-lookup"><span data-stu-id="3928b-433">y</span></span>  
<span data-ttu-id="3928b-434">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-434">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="3928b-435">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="3928b-435">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="3928b-436">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="3928b-436">Return Value - beginDrag</span></span>

<span data-ttu-id="3928b-437">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3928b-437">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="3928b-438">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="3928b-438">Remarks - beginDrag</span></span>

<span data-ttu-id="3928b-439">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="3928b-439">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="3928b-440">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="3928b-440">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="3928b-441">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="3928b-441">Method bold</span></span>

<span data-ttu-id="3928b-442">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-442">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="3928b-443">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="3928b-443">Parameters - bold</span></span>

<span data-ttu-id="3928b-444">値</span><span class="sxs-lookup"><span data-stu-id="3928b-444">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="3928b-445">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="3928b-445">Return Value - bold</span></span>

<span data-ttu-id="3928b-446">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-446">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="3928b-447">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="3928b-447">Remarks - bold</span></span>

<span data-ttu-id="3928b-448">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3928b-448">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="3928b-449">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="3928b-449">0 Use the default font weight.</span></span>
-   <span data-ttu-id="3928b-450">1 シン。</span><span class="sxs-lookup"><span data-stu-id="3928b-450">1 Thin.</span></span>
-   <span data-ttu-id="3928b-451">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="3928b-451">2 Extra-light.</span></span>
-   <span data-ttu-id="3928b-452">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="3928b-452">3 Light.</span></span>
-   <span data-ttu-id="3928b-453">4 標準。</span><span class="sxs-lookup"><span data-stu-id="3928b-453">4 Normal.</span></span>
-   <span data-ttu-id="3928b-454">5 中。</span><span class="sxs-lookup"><span data-stu-id="3928b-454">5 Medium.</span></span>
-   <span data-ttu-id="3928b-455">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="3928b-455">6 Semibold.</span></span>
-   <span data-ttu-id="3928b-456">7 太字。</span><span class="sxs-lookup"><span data-stu-id="3928b-456">7 Bold.</span></span>
-   <span data-ttu-id="3928b-457">8 極太。</span><span class="sxs-lookup"><span data-stu-id="3928b-457">8 Extra-bold.</span></span>
-   <span data-ttu-id="3928b-458">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="3928b-458">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="3928b-459">メソッド border</span><span class="sxs-lookup"><span data-stu-id="3928b-459">Method border</span></span>

<span data-ttu-id="3928b-460">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-460">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="3928b-461">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="3928b-461">Parameters - border</span></span>

<span data-ttu-id="3928b-462">値</span><span class="sxs-lookup"><span data-stu-id="3928b-462">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="3928b-463">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="3928b-463">Return Value - border</span></span>

<span data-ttu-id="3928b-464">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="3928b-464">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="3928b-465">備考 - border</span><span class="sxs-lookup"><span data-stu-id="3928b-465">Remarks - border</span></span>

<span data-ttu-id="3928b-466">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3928b-466">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="3928b-467">値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-467">Value.</span></span> | <span data-ttu-id="3928b-468">説明。</span><span class="sxs-lookup"><span data-stu-id="3928b-468">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="3928b-469">0</span><span class="sxs-lookup"><span data-stu-id="3928b-469">0</span></span>      | <span data-ttu-id="3928b-470">自動。</span><span class="sxs-lookup"><span data-stu-id="3928b-470">Auto.</span></span>        |
| <span data-ttu-id="3928b-471">1</span><span class="sxs-lookup"><span data-stu-id="3928b-471">1</span></span>      | <span data-ttu-id="3928b-472">3D。</span><span class="sxs-lookup"><span data-stu-id="3928b-472">3D.</span></span>          |
| <span data-ttu-id="3928b-473">2</span><span class="sxs-lookup"><span data-stu-id="3928b-473">2</span></span>      | <span data-ttu-id="3928b-474">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="3928b-474">Single line.</span></span> |
| <span data-ttu-id="3928b-475">3</span><span class="sxs-lookup"><span data-stu-id="3928b-475">3</span></span>      | <span data-ttu-id="3928b-476">均一。</span><span class="sxs-lookup"><span data-stu-id="3928b-476">Flat.</span></span>        |
| <span data-ttu-id="3928b-477">4</span><span class="sxs-lookup"><span data-stu-id="3928b-477">4</span></span>      | <span data-ttu-id="3928b-478">なし。</span><span class="sxs-lookup"><span data-stu-id="3928b-478">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="3928b-479">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-479">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="3928b-480">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-480">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="3928b-481">値</span><span class="sxs-lookup"><span data-stu-id="3928b-481">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="3928b-482">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-482">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="3928b-483">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="3928b-483">Method calcControlSize</span></span>

<span data-ttu-id="3928b-484">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-484">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="3928b-485">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="3928b-485">Parameters - calcControlSize</span></span>

<span data-ttu-id="3928b-486">chars</span><span class="sxs-lookup"><span data-stu-id="3928b-486">chars</span></span>  
<span data-ttu-id="3928b-487">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="3928b-487">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="3928b-488">明細行</span><span class="sxs-lookup"><span data-stu-id="3928b-488">lines</span></span>  
<span data-ttu-id="3928b-489">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="3928b-489">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="3928b-490">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="3928b-490">Return Value - calcControlSize</span></span>

<span data-ttu-id="3928b-491">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="3928b-491">The container that holds the width and height.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="3928b-492">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="3928b-492">Method characterSet</span></span>

<span data-ttu-id="3928b-493">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-493">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="3928b-494">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="3928b-494">Parameters - characterSet</span></span>

<span data-ttu-id="3928b-495">値</span><span class="sxs-lookup"><span data-stu-id="3928b-495">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="3928b-496">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="3928b-496">Return Value - characterSet</span></span>

<span data-ttu-id="3928b-497">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-497">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="3928b-498">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="3928b-498">Remarks - characterSet</span></span>

<span data-ttu-id="3928b-499">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-499">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="3928b-500">値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-500">Value.</span></span> | <span data-ttu-id="3928b-501">説明。</span><span class="sxs-lookup"><span data-stu-id="3928b-501">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="3928b-502">0</span><span class="sxs-lookup"><span data-stu-id="3928b-502">0</span></span>      | <span data-ttu-id="3928b-503">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-503">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="3928b-504">1</span><span class="sxs-lookup"><span data-stu-id="3928b-504">1</span></span>      | <span data-ttu-id="3928b-505">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-505">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="3928b-506">2</span><span class="sxs-lookup"><span data-stu-id="3928b-506">2</span></span>      | <span data-ttu-id="3928b-507">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-507">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="3928b-508">77</span><span class="sxs-lookup"><span data-stu-id="3928b-508">77</span></span>     | <span data-ttu-id="3928b-509">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-509">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="3928b-510">128</span><span class="sxs-lookup"><span data-stu-id="3928b-510">128</span></span>    | <span data-ttu-id="3928b-511">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-511">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="3928b-512">129</span><span class="sxs-lookup"><span data-stu-id="3928b-512">129</span></span>    | <span data-ttu-id="3928b-513">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-513">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="3928b-514">134</span><span class="sxs-lookup"><span data-stu-id="3928b-514">134</span></span>    | <span data-ttu-id="3928b-515">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-515">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="3928b-516">136</span><span class="sxs-lookup"><span data-stu-id="3928b-516">136</span></span>    | <span data-ttu-id="3928b-517">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-517">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="3928b-518">161</span><span class="sxs-lookup"><span data-stu-id="3928b-518">161</span></span>    | <span data-ttu-id="3928b-519">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-519">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="3928b-520">162</span><span class="sxs-lookup"><span data-stu-id="3928b-520">162</span></span>    | <span data-ttu-id="3928b-521">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-521">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="3928b-522">163</span><span class="sxs-lookup"><span data-stu-id="3928b-522">163</span></span>    | <span data-ttu-id="3928b-523">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-523">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="3928b-524">186</span><span class="sxs-lookup"><span data-stu-id="3928b-524">186</span></span>    | <span data-ttu-id="3928b-525">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-525">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="3928b-526">204</span><span class="sxs-lookup"><span data-stu-id="3928b-526">204</span></span>    | <span data-ttu-id="3928b-527">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-527">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="3928b-528">238</span><span class="sxs-lookup"><span data-stu-id="3928b-528">238</span></span>    | <span data-ttu-id="3928b-529">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-529">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="3928b-530">255</span><span class="sxs-lookup"><span data-stu-id="3928b-530">255</span></span>    | <span data-ttu-id="3928b-531">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-531">OEM\_CHARSET</span></span>         |

<span data-ttu-id="3928b-532">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-532">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="3928b-533">値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-533">Value.</span></span> | <span data-ttu-id="3928b-534">説明。</span><span class="sxs-lookup"><span data-stu-id="3928b-534">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="3928b-535">130</span><span class="sxs-lookup"><span data-stu-id="3928b-535">130</span></span>    | <span data-ttu-id="3928b-536">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-536">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="3928b-537">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-537">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="3928b-538">値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-538">Value.</span></span> | <span data-ttu-id="3928b-539">説明。</span><span class="sxs-lookup"><span data-stu-id="3928b-539">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="3928b-540">177</span><span class="sxs-lookup"><span data-stu-id="3928b-540">177</span></span>    | <span data-ttu-id="3928b-541">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-541">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="3928b-542">178</span><span class="sxs-lookup"><span data-stu-id="3928b-542">178</span></span>    | <span data-ttu-id="3928b-543">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-543">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="3928b-544">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-544">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="3928b-545">値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-545">Value.</span></span> | <span data-ttu-id="3928b-546">説明。</span><span class="sxs-lookup"><span data-stu-id="3928b-546">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="3928b-547">222</span><span class="sxs-lookup"><span data-stu-id="3928b-547">222</span></span>    | <span data-ttu-id="3928b-548">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3928b-548">THAI\_CHARSET</span></span> |

<span data-ttu-id="3928b-549">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-549">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="3928b-550">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-550">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="3928b-551">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3928b-551">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="3928b-552">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="3928b-552">Method colorScheme</span></span>

<span data-ttu-id="3928b-553">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-553">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="3928b-554">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3928b-554">Parameters - colorScheme</span></span>

<span data-ttu-id="3928b-555">値</span><span class="sxs-lookup"><span data-stu-id="3928b-555">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="3928b-556">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3928b-556">Return Value - colorScheme</span></span>

<span data-ttu-id="3928b-557">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="3928b-557">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="3928b-558">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3928b-558">Remarks - colorScheme</span></span>

<span data-ttu-id="3928b-559">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-559">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="3928b-560">値です。</span><span class="sxs-lookup"><span data-stu-id="3928b-560">Value.</span></span> | <span data-ttu-id="3928b-561">スタイル。</span><span class="sxs-lookup"><span data-stu-id="3928b-561">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="3928b-562">0</span><span class="sxs-lookup"><span data-stu-id="3928b-562">0</span></span>      | <span data-ttu-id="3928b-563">既定。</span><span class="sxs-lookup"><span data-stu-id="3928b-563">Default.</span></span>               |
| <span data-ttu-id="3928b-564">1</span><span class="sxs-lookup"><span data-stu-id="3928b-564">1</span></span>      | <span data-ttu-id="3928b-565">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="3928b-565">The Windows palette.</span></span>   |
| <span data-ttu-id="3928b-566">2</span><span class="sxs-lookup"><span data-stu-id="3928b-566">2</span></span>      | <span data-ttu-id="3928b-567">真の配色。</span><span class="sxs-lookup"><span data-stu-id="3928b-567">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="3928b-568">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="3928b-568">Method configurationKey</span></span>

<span data-ttu-id="3928b-569">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-569">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="3928b-570">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3928b-570">Parameters - configurationKey</span></span>

<span data-ttu-id="3928b-571">値</span><span class="sxs-lookup"><span data-stu-id="3928b-571">value</span></span>  
<span data-ttu-id="3928b-572">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-572">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="3928b-573">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3928b-573">Return Value - configurationKey</span></span>

<span data-ttu-id="3928b-574">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="3928b-574">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="3928b-575">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3928b-575">Remarks - configurationKey</span></span>

<span data-ttu-id="3928b-576">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-576">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="3928b-577">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="3928b-577">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="3928b-578">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="3928b-578">Method configurationKeyEx</span></span>

<span data-ttu-id="3928b-579">コントロールでチェックされているコンフィギュレーション キーの名前を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-579">Retrieves a list that contains the names of configuration keys that are checked for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="3928b-580">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="3928b-580">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="3928b-581">コンフィギュレーション キー名を持つ文字列の一覧。</span><span class="sxs-lookup"><span data-stu-id="3928b-581">A list of strings that contain the configuration key names.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="3928b-582">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="3928b-582">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="3928b-583">取得されたリストに重複が含まれていません。</span><span class="sxs-lookup"><span data-stu-id="3928b-583">The list that is retrieved does not contain duplicates.</span></span> <span data-ttu-id="3928b-584">すべてのフォーム コントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-584">It applies to all form controls.</span></span> <span data-ttu-id="3928b-585">コントロールがデータ バインドの場合は、一覧には、テーブルとフィールドのコンフィギュレーション キーも含まれます。</span><span class="sxs-lookup"><span data-stu-id="3928b-585">If the control is data-bound, the list also contains the configuration key of the table and field.</span></span> <span data-ttu-id="3928b-586">コントロールがプロパティ、拡張データ型、または Enumtype メソッドに空でない値を持っている場合は、これらの要素のコンフィギュレーション キーもリストに追加されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-586">The configuration keys on these elements are also added to the list if the control has non-empty values in the properties, extended data type, or Enumtype methods.</span></span> <span data-ttu-id="3928b-587">FormBuildMenuButtonControl クラスの実装の詳細のため、指定されたメニュー項目にある構成キーはリストに含まれません。</span><span class="sxs-lookup"><span data-stu-id="3928b-587">Because of implementation details for the FormBuildMenuButtonControl class, the list does not contain the configuration keys that found on the specified menu item.</span></span> <span data-ttu-id="3928b-588">ただし、FormMenuButtonControl クラスでメソッドが呼び出される場合、一覧にはこれらが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3928b-588">However, the list does include these if the method is invoked on the FormMenuButtonControl class.</span></span>

## <a name="method-count"></a><span data-ttu-id="3928b-589">メソッド count</span><span class="sxs-lookup"><span data-stu-id="3928b-589">Method count</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="3928b-590">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="3928b-590">Return Value - count</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="3928b-591">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3928b-591">Method countryRegionCodes</span></span>

<span data-ttu-id="3928b-592">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-592">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="3928b-593">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3928b-593">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="3928b-594">値</span><span class="sxs-lookup"><span data-stu-id="3928b-594">value</span></span>  
<span data-ttu-id="3928b-595">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-595">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="3928b-596">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3928b-596">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="3928b-597">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="3928b-597">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="3928b-598">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="3928b-598">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="3928b-599">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="3928b-599">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="3928b-600">値</span><span class="sxs-lookup"><span data-stu-id="3928b-600">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="3928b-601">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="3928b-601">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="3928b-602">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="3928b-602">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="3928b-603">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="3928b-603">Parameters - dataField</span></span>

<span data-ttu-id="3928b-604">値</span><span class="sxs-lookup"><span data-stu-id="3928b-604">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="3928b-605">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="3928b-605">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="3928b-606">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-606">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="3928b-607">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-607">Parameters - dataMethod</span></span>

<span data-ttu-id="3928b-608">値</span><span class="sxs-lookup"><span data-stu-id="3928b-608">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="3928b-609">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-609">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="3928b-610">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3928b-610">Method dataRelationPath</span></span>

<span data-ttu-id="3928b-611">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-611">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="3928b-612">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3928b-612">Parameters - dataRelationPath</span></span>

<span data-ttu-id="3928b-613">値</span><span class="sxs-lookup"><span data-stu-id="3928b-613">value</span></span>  
<span data-ttu-id="3928b-614">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-614">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="3928b-615">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3928b-615">Return Value - dataRelationPath</span></span>

<span data-ttu-id="3928b-616">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="3928b-616">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="3928b-617">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3928b-617">Remarks - dataRelationPath</span></span>

<span data-ttu-id="3928b-618">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="3928b-618">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="3928b-619">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="3928b-619">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="3928b-620">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="3928b-620">Method dataSource</span></span>

<span data-ttu-id="3928b-621">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-621">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="3928b-622">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="3928b-622">Parameters - dataSource</span></span>

<span data-ttu-id="3928b-623">値</span><span class="sxs-lookup"><span data-stu-id="3928b-623">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="3928b-624">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="3928b-624">Return Value - dataSource</span></span>

<span data-ttu-id="3928b-625">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="3928b-625">The identifier of the data source to be used.</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="3928b-626">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="3928b-626">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="3928b-627">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="3928b-627">Parameters - displayLength</span></span>

<span data-ttu-id="3928b-628">値</span><span class="sxs-lookup"><span data-stu-id="3928b-628">value</span></span>  

<!-- -->

<span data-ttu-id="3928b-629">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-629">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="3928b-630">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="3928b-630">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="3928b-631">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-631">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="3928b-632">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-632">Parameters - displayLengthMode</span></span>

<span data-ttu-id="3928b-633">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-633">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="3928b-634">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-634">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="3928b-635">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-635">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="3928b-636">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-636">Parameters - displayLengthValue</span></span>

<span data-ttu-id="3928b-637">値</span><span class="sxs-lookup"><span data-stu-id="3928b-637">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="3928b-638">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-638">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="3928b-639">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="3928b-639">Method displayTarget</span></span>

<span data-ttu-id="3928b-640">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-640">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="3928b-641">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="3928b-641">Parameters - displayTarget</span></span>

<span data-ttu-id="3928b-642">値</span><span class="sxs-lookup"><span data-stu-id="3928b-642">value</span></span>  
<span data-ttu-id="3928b-643">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-643">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="3928b-644">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="3928b-644">Return Value - displayTarget</span></span>

<span data-ttu-id="3928b-645">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="3928b-645">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-doubleclick"></a><span data-ttu-id="3928b-646">メソッド doubleClick</span><span class="sxs-lookup"><span data-stu-id="3928b-646">Method doubleClick</span></span>

```xpp
public int doubleClick()
```

### <a name="return-value---doubleclick"></a><span data-ttu-id="3928b-647">戻り値 - doubleClick</span><span class="sxs-lookup"><span data-stu-id="3928b-647">Return Value - doubleClick</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="3928b-648">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="3928b-648">Method dragDrop</span></span>

<span data-ttu-id="3928b-649">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-649">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="3928b-650">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3928b-650">Parameters - dragDrop</span></span>

<span data-ttu-id="3928b-651">値</span><span class="sxs-lookup"><span data-stu-id="3928b-651">value</span></span>  
<span data-ttu-id="3928b-652">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-652">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="3928b-653">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3928b-653">Return Value - dragDrop</span></span>

<span data-ttu-id="3928b-654">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="3928b-654">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="3928b-655">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3928b-655">Remarks - dragDrop</span></span>

<span data-ttu-id="3928b-656">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-656">Use the dragLeave, the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="3928b-657">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="3928b-657">Method dragOver</span></span>

<span data-ttu-id="3928b-658">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-658">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="3928b-659">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="3928b-659">Parameters - dragOver</span></span>

<span data-ttu-id="3928b-660">dragSource</span><span class="sxs-lookup"><span data-stu-id="3928b-660">dragSource</span></span>  
<span data-ttu-id="3928b-661">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-661">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-662">dragMode</span><span class="sxs-lookup"><span data-stu-id="3928b-662">dragMode</span></span>  
<span data-ttu-id="3928b-663">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-663">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-664">x</span><span class="sxs-lookup"><span data-stu-id="3928b-664">x</span></span>  
<span data-ttu-id="3928b-665">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-665">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-666">y</span><span class="sxs-lookup"><span data-stu-id="3928b-666">y</span></span>  
<span data-ttu-id="3928b-667">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-667">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="3928b-668">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="3928b-668">Return Value - dragOver</span></span>

<span data-ttu-id="3928b-669">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="3928b-669">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="3928b-670">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="3928b-670">Method dragOverEx</span></span>

<span data-ttu-id="3928b-671">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-671">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="3928b-672">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="3928b-672">Parameters - dragOverEx</span></span>

<span data-ttu-id="3928b-673">dragSource</span><span class="sxs-lookup"><span data-stu-id="3928b-673">dragSource</span></span>  
<span data-ttu-id="3928b-674">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-674">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-675">dragMode</span><span class="sxs-lookup"><span data-stu-id="3928b-675">dragMode</span></span>  
<span data-ttu-id="3928b-676">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-676">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-677">x</span><span class="sxs-lookup"><span data-stu-id="3928b-677">x</span></span>  
<span data-ttu-id="3928b-678">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-678">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-679">y</span><span class="sxs-lookup"><span data-stu-id="3928b-679">y</span></span>  
<span data-ttu-id="3928b-680">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-680">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="3928b-681">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="3928b-681">Return Value - dragOverEx</span></span>

<span data-ttu-id="3928b-682">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="3928b-682">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="3928b-683">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="3928b-683">Method dragText</span></span>

<span data-ttu-id="3928b-684">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-684">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="3928b-685">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="3928b-685">Return Value - dragText</span></span>

<span data-ttu-id="3928b-686">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3928b-686">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="3928b-687">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="3928b-687">Method enabled</span></span>

<span data-ttu-id="3928b-688">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-688">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="3928b-689">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="3928b-689">Parameters - enabled</span></span>

<span data-ttu-id="3928b-690">値</span><span class="sxs-lookup"><span data-stu-id="3928b-690">value</span></span>  
<span data-ttu-id="3928b-691">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-691">A Boolean value that indicates whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="3928b-692">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="3928b-692">Return Value - enabled</span></span>

<span data-ttu-id="3928b-693">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3928b-693">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="3928b-694">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="3928b-694">Remarks - enabled</span></span>

<span data-ttu-id="3928b-695">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="3928b-695">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="3928b-696">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3928b-696">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="3928b-697">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3928b-697">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-enumtype"></a><span data-ttu-id="3928b-698">メソッド enumType</span><span class="sxs-lookup"><span data-stu-id="3928b-698">Method enumType</span></span>

```xpp
public EnumId enumType([EnumId value])
```

### <a name="parameters---enumtype"></a><span data-ttu-id="3928b-699">パラメーター - enumType</span><span class="sxs-lookup"><span data-stu-id="3928b-699">Parameters - enumType</span></span>

<span data-ttu-id="3928b-700">値</span><span class="sxs-lookup"><span data-stu-id="3928b-700">value</span></span>  

### <a name="return-value---enumtype"></a><span data-ttu-id="3928b-701">戻り値 - enumType</span><span class="sxs-lookup"><span data-stu-id="3928b-701">Return Value - enumType</span></span>

## <a name="method-enumtypevalue"></a><span data-ttu-id="3928b-702">メソッド enumTypeValue</span><span class="sxs-lookup"><span data-stu-id="3928b-702">Method enumTypeValue</span></span>

```xpp
public EnumId enumTypeValue()
```

### <a name="return-value---enumtypevalue"></a><span data-ttu-id="3928b-703">戻り値 - enumTypeValue</span><span class="sxs-lookup"><span data-stu-id="3928b-703">Return Value - enumTypeValue</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="3928b-704">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="3928b-704">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="3928b-705">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="3928b-705">Parameters - extendedDataType</span></span>

<span data-ttu-id="3928b-706">値</span><span class="sxs-lookup"><span data-stu-id="3928b-706">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="3928b-707">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="3928b-707">Return Value - extendedDataType</span></span>

## <a name="method-find"></a><span data-ttu-id="3928b-708">メソッド find</span><span class="sxs-lookup"><span data-stu-id="3928b-708">Method find</span></span>

```xpp
public int find(str string)
```

### <a name="parameters---find"></a><span data-ttu-id="3928b-709">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="3928b-709">Parameters - find</span></span>

<span data-ttu-id="3928b-710">文字列</span><span class="sxs-lookup"><span data-stu-id="3928b-710">string</span></span>  

### <a name="return-value---find"></a><span data-ttu-id="3928b-711">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="3928b-711">Return Value - find</span></span>

## <a name="method-font"></a><span data-ttu-id="3928b-712">メソッド font</span><span class="sxs-lookup"><span data-stu-id="3928b-712">Method font</span></span>

<span data-ttu-id="3928b-713">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-713">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="3928b-714">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="3928b-714">Parameters - font</span></span>

<span data-ttu-id="3928b-715">値</span><span class="sxs-lookup"><span data-stu-id="3928b-715">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="3928b-716">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="3928b-716">Return Value - font</span></span>

<span data-ttu-id="3928b-717">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="3928b-717">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="3928b-718">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="3928b-718">Method fontSize</span></span>

<span data-ttu-id="3928b-719">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-719">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="3928b-720">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="3928b-720">Parameters - fontSize</span></span>

<span data-ttu-id="3928b-721">値</span><span class="sxs-lookup"><span data-stu-id="3928b-721">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="3928b-722">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="3928b-722">Return Value - fontSize</span></span>

<span data-ttu-id="3928b-723">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="3928b-723">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="3928b-724">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-724">Method foregroundColor</span></span>

<span data-ttu-id="3928b-725">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-725">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="3928b-726">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-726">Parameters - foregroundColor</span></span>

<span data-ttu-id="3928b-727">値</span><span class="sxs-lookup"><span data-stu-id="3928b-727">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="3928b-728">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-728">Return Value - foregroundColor</span></span>

<span data-ttu-id="3928b-729">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="3928b-729">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="3928b-730">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-730">Remarks - foregroundColor</span></span>

<span data-ttu-id="3928b-731">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3928b-731">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="3928b-732">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3928b-732">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="3928b-733">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3928b-733">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="3928b-734">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3928b-734">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="3928b-735">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3928b-735">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="3928b-736">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="3928b-736">The maximum value for a single byte is 255.</span></span>

## <a name="method-gettext"></a><span data-ttu-id="3928b-737">メソッド getText</span><span class="sxs-lookup"><span data-stu-id="3928b-737">Method getText</span></span>

```xpp
public str getText(int index)
```

### <a name="parameters---gettext"></a><span data-ttu-id="3928b-738">パラメーター - getText</span><span class="sxs-lookup"><span data-stu-id="3928b-738">Parameters - getText</span></span>

<span data-ttu-id="3928b-739">指数</span><span class="sxs-lookup"><span data-stu-id="3928b-739">index</span></span>  

### <a name="return-value---gettext"></a><span data-ttu-id="3928b-740">戻り値 - getText</span><span class="sxs-lookup"><span data-stu-id="3928b-740">Return Value - getText</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="3928b-741">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="3928b-741">Method hasChanged</span></span>

<span data-ttu-id="3928b-742">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-742">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="3928b-743">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="3928b-743">Parameters - hasChanged</span></span>

<span data-ttu-id="3928b-744">val</span><span class="sxs-lookup"><span data-stu-id="3928b-744">val</span></span>  
<span data-ttu-id="3928b-745">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-745">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="3928b-746">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="3928b-746">Return Value - hasChanged</span></span>

<span data-ttu-id="3928b-747">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3928b-747">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="3928b-748">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="3928b-748">Method hasUserSetting</span></span>

<span data-ttu-id="3928b-749">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-749">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="3928b-750">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="3928b-750">Return Value - hasUserSetting</span></span>

<span data-ttu-id="3928b-751">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3928b-751">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="3928b-752">メソッド height</span><span class="sxs-lookup"><span data-stu-id="3928b-752">Method height</span></span>

<span data-ttu-id="3928b-753">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-753">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="3928b-754">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="3928b-754">Parameters - height</span></span>

<span data-ttu-id="3928b-755">値</span><span class="sxs-lookup"><span data-stu-id="3928b-755">value</span></span>  
<span data-ttu-id="3928b-756">高さの計算方法を指定する整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-756">An integer data type that specifies how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="3928b-757">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-757">mode</span></span>  
<span data-ttu-id="3928b-758">高さの計算方法を指定する整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-758">An integer data type that specifies how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="3928b-759">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="3928b-759">Return Value - height</span></span>

<span data-ttu-id="3928b-760">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="3928b-760">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="3928b-761">備考 - height</span><span class="sxs-lookup"><span data-stu-id="3928b-761">Remarks - height</span></span>

<span data-ttu-id="3928b-762">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-762">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="3928b-763">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="3928b-763">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="3928b-764">モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-764">Mode.</span></span>            | <span data-ttu-id="3928b-765">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="3928b-765">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3928b-766">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="3928b-766">-1 Exact.</span></span>        | <span data-ttu-id="3928b-767">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-767">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3928b-768">0 自動。</span><span class="sxs-lookup"><span data-stu-id="3928b-768">0 Auto.</span></span>          | <span data-ttu-id="3928b-769">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-769">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3928b-770">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="3928b-770">1 Column height.</span></span> | <span data-ttu-id="3928b-771">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="3928b-771">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="3928b-772">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3928b-772">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="3928b-773">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="3928b-773">Method heightMode</span></span>

<span data-ttu-id="3928b-774">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-774">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="3928b-775">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="3928b-775">Parameters - heightMode</span></span>

<span data-ttu-id="3928b-776">値</span><span class="sxs-lookup"><span data-stu-id="3928b-776">value</span></span>  
<span data-ttu-id="3928b-777">コントロールの高さの計算方法を指定する整数データ型値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-777">An integer data type value that specifies how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="3928b-778">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="3928b-778">Return Value - heightMode</span></span>

<span data-ttu-id="3928b-779">計算モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-779">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="3928b-780">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="3928b-780">Remarks - heightMode</span></span>

<span data-ttu-id="3928b-781">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="3928b-781">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="3928b-782">モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-782">Mode.</span></span>          | <span data-ttu-id="3928b-783">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="3928b-783">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3928b-784">正確。</span><span class="sxs-lookup"><span data-stu-id="3928b-784">Exact.</span></span>         | <span data-ttu-id="3928b-785">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-785">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3928b-786">自動。</span><span class="sxs-lookup"><span data-stu-id="3928b-786">Auto.</span></span>          | <span data-ttu-id="3928b-787">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-787">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3928b-788">列の高さ</span><span class="sxs-lookup"><span data-stu-id="3928b-788">Column height.</span></span> | <span data-ttu-id="3928b-789">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="3928b-789">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="3928b-790">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="3928b-790">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="3928b-791">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="3928b-791">Method heightValue</span></span>

<span data-ttu-id="3928b-792">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-792">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="3928b-793">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="3928b-793">Parameters - heightValue</span></span>

<span data-ttu-id="3928b-794">値</span><span class="sxs-lookup"><span data-stu-id="3928b-794">value</span></span>  
<span data-ttu-id="3928b-795">高さをピクセル単位で指定する整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-795">An integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="3928b-796">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="3928b-796">Return Value - heightValue</span></span>

<span data-ttu-id="3928b-797">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="3928b-797">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="3928b-798">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="3928b-798">Remarks - heightValue</span></span>

<span data-ttu-id="3928b-799">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="3928b-799">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="3928b-800">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="3928b-800">Method helpField</span></span>

<span data-ttu-id="3928b-801">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-801">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="3928b-802">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="3928b-802">Return Value - helpField</span></span>

<span data-ttu-id="3928b-803">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3928b-803">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="3928b-804">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="3928b-804">Remarks - helpField</span></span>

<span data-ttu-id="3928b-805">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3928b-805">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="3928b-806">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3928b-806">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="3928b-807">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="3928b-807">Method helpText</span></span>

<span data-ttu-id="3928b-808">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-808">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="3928b-809">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="3928b-809">Parameters - helpText</span></span>

<span data-ttu-id="3928b-810">値</span><span class="sxs-lookup"><span data-stu-id="3928b-810">value</span></span>  
<span data-ttu-id="3928b-811">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="3928b-811">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="3928b-812">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="3928b-812">Return Value - helpText</span></span>

<span data-ttu-id="3928b-813">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="3928b-813">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="3928b-814">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="3928b-814">Remarks - helpText</span></span>

<span data-ttu-id="3928b-815">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-815">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="3928b-816">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="3928b-816">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hidefirstentry"></a><span data-ttu-id="3928b-817">メソッド hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="3928b-817">Method hideFirstEntry</span></span>

```xpp
public boolean hideFirstEntry([boolean value])
```

### <a name="parameters---hidefirstentry"></a><span data-ttu-id="3928b-818">パラメーター - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="3928b-818">Parameters - hideFirstEntry</span></span>

<span data-ttu-id="3928b-819">値</span><span class="sxs-lookup"><span data-stu-id="3928b-819">value</span></span>  

### <a name="return-value---hidefirstentry"></a><span data-ttu-id="3928b-820">戻り値 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="3928b-820">Return Value - hideFirstEntry</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="3928b-821">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3928b-821">Method hierarchyParent</span></span>

<span data-ttu-id="3928b-822">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-822">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="3928b-823">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3928b-823">Parameters - hierarchyParent</span></span>

<span data-ttu-id="3928b-824">値</span><span class="sxs-lookup"><span data-stu-id="3928b-824">value</span></span>  
<span data-ttu-id="3928b-825">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="3928b-825">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="3928b-826">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3928b-826">Return Value - hierarchyParent</span></span>

<span data-ttu-id="3928b-827">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="3928b-827">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="3928b-828">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="3928b-828">Method hWnd</span></span>

<span data-ttu-id="3928b-829">コントロールの Windows ハンドル (hWnd) を返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-829">Returns the Windows handle (hWnd) of the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="3928b-830">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="3928b-830">Return Value - hWnd</span></span>

<span data-ttu-id="3928b-831">32 ビット ハンドル (hWnd)。</span><span class="sxs-lookup"><span data-stu-id="3928b-831">A 32-bit handle (hWnd).</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="3928b-832">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="3928b-832">Remarks - hWnd</span></span>

<span data-ttu-id="3928b-833">この処理は、すべてのコントロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-833">This handle applies to all controls.</span></span> <span data-ttu-id="3928b-834">これは、Windows API を使用する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="3928b-834">This is useful when you work with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="3928b-835">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="3928b-835">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="3928b-836">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="3928b-836">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="3928b-837">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="3928b-837">Method isDisplayed</span></span>

<span data-ttu-id="3928b-838">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-838">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="3928b-839">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="3928b-839">Return Value - isDisplayed</span></span>

<span data-ttu-id="3928b-840">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3928b-840">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="3928b-841">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="3928b-841">Remarks - isDisplayed</span></span>

<span data-ttu-id="3928b-842">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3928b-842">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="3928b-843">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="3928b-843">Method isRestricted</span></span>

<span data-ttu-id="3928b-844">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-844">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="3928b-845">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="3928b-845">Return Value - isRestricted</span></span>

<span data-ttu-id="3928b-846">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3928b-846">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="3928b-847">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3928b-847">Method isUserSetupEnabled</span></span>

<span data-ttu-id="3928b-848">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-848">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="3928b-849">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3928b-849">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="3928b-850">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="3928b-850">neededSetupRights</span></span>  
<span data-ttu-id="3928b-851">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="3928b-851">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="3928b-852">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3928b-852">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="3928b-853">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3928b-853">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise false.</span></span> <span data-ttu-id="3928b-854">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="3928b-854">For this method to return true, the AllowUserSetup property of the design and all parent containers must permit the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="3928b-855">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3928b-855">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="3928b-856">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="3928b-856">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3928b-857">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="3928b-857">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="3928b-858">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="3928b-858">No changes can be made to the control.</span></span> <span data-ttu-id="3928b-859">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-859">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="3928b-860">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="3928b-860">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="3928b-861">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3928b-861">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="3928b-862">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="3928b-862">The user cannot move the control.</span></span>   |
| <span data-ttu-id="3928b-863">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="3928b-863">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="3928b-864">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3928b-864">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="3928b-865">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="3928b-865">The user can also move the control.</span></span> |

## <a name="method-isvalid"></a><span data-ttu-id="3928b-866">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="3928b-866">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="3928b-867">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="3928b-867">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="3928b-868">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="3928b-868">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="3928b-869">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="3928b-869">Parameters - italic</span></span>

<span data-ttu-id="3928b-870">値</span><span class="sxs-lookup"><span data-stu-id="3928b-870">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="3928b-871">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="3928b-871">Return Value - italic</span></span>

## <a name="method-item"></a><span data-ttu-id="3928b-872">メソッド item</span><span class="sxs-lookup"><span data-stu-id="3928b-872">Method item</span></span>

```xpp
public int item([int value])
```

### <a name="parameters---item"></a><span data-ttu-id="3928b-873">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="3928b-873">Parameters - item</span></span>

<span data-ttu-id="3928b-874">値</span><span class="sxs-lookup"><span data-stu-id="3928b-874">value</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="3928b-875">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="3928b-875">Return Value - item</span></span>

## <a name="method-items"></a><span data-ttu-id="3928b-876">メソッド items</span><span class="sxs-lookup"><span data-stu-id="3928b-876">Method items</span></span>

```xpp
public int items([int value])
```

### <a name="parameters---items"></a><span data-ttu-id="3928b-877">パラメーター - items</span><span class="sxs-lookup"><span data-stu-id="3928b-877">Parameters - items</span></span>

<span data-ttu-id="3928b-878">値</span><span class="sxs-lookup"><span data-stu-id="3928b-878">value</span></span>  

### <a name="return-value---items"></a><span data-ttu-id="3928b-879">戻り値 - items</span><span class="sxs-lookup"><span data-stu-id="3928b-879">Return Value - items</span></span>

## <a name="method-label"></a><span data-ttu-id="3928b-880">メソッド label</span><span class="sxs-lookup"><span data-stu-id="3928b-880">Method label</span></span>

<span data-ttu-id="3928b-881">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-881">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="3928b-882">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="3928b-882">Parameters - label</span></span>

<span data-ttu-id="3928b-883">値</span><span class="sxs-lookup"><span data-stu-id="3928b-883">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="3928b-884">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="3928b-884">Return Value - label</span></span>

<span data-ttu-id="3928b-885">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="3928b-885">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="3928b-886">備考 - label</span><span class="sxs-lookup"><span data-stu-id="3928b-886">Remarks - label</span></span>

<span data-ttu-id="3928b-887">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-887">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="3928b-888">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="3928b-888">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="3928b-889">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="3928b-889">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="3928b-890">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="3928b-890">Parameters - labelAlignment</span></span>

<span data-ttu-id="3928b-891">値</span><span class="sxs-lookup"><span data-stu-id="3928b-891">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="3928b-892">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="3928b-892">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="3928b-893">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="3928b-893">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="3928b-894">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="3928b-894">Parameters - labelBold</span></span>

<span data-ttu-id="3928b-895">値</span><span class="sxs-lookup"><span data-stu-id="3928b-895">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="3928b-896">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="3928b-896">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="3928b-897">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="3928b-897">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="3928b-898">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="3928b-898">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="3928b-899">値</span><span class="sxs-lookup"><span data-stu-id="3928b-899">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="3928b-900">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="3928b-900">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="3928b-901">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="3928b-901">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="3928b-902">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="3928b-902">Parameters - labelFont</span></span>

<span data-ttu-id="3928b-903">値</span><span class="sxs-lookup"><span data-stu-id="3928b-903">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="3928b-904">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="3928b-904">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="3928b-905">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="3928b-905">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="3928b-906">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="3928b-906">Parameters - labelFontSize</span></span>

<span data-ttu-id="3928b-907">値</span><span class="sxs-lookup"><span data-stu-id="3928b-907">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="3928b-908">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="3928b-908">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="3928b-909">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-909">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="3928b-910">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-910">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="3928b-911">値</span><span class="sxs-lookup"><span data-stu-id="3928b-911">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="3928b-912">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="3928b-912">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="3928b-913">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="3928b-913">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="3928b-914">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="3928b-914">Parameters - labelGuide</span></span>

<span data-ttu-id="3928b-915">値</span><span class="sxs-lookup"><span data-stu-id="3928b-915">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="3928b-916">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="3928b-916">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="3928b-917">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="3928b-917">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="3928b-918">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="3928b-918">Parameters - labelHeight</span></span>

<span data-ttu-id="3928b-919">値</span><span class="sxs-lookup"><span data-stu-id="3928b-919">value</span></span>  

<!-- -->

<span data-ttu-id="3928b-920">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-920">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="3928b-921">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="3928b-921">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="3928b-922">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="3928b-922">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="3928b-923">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="3928b-923">Parameters - labelHeightMode</span></span>

<span data-ttu-id="3928b-924">値</span><span class="sxs-lookup"><span data-stu-id="3928b-924">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="3928b-925">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="3928b-925">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="3928b-926">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="3928b-926">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="3928b-927">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="3928b-927">Parameters - labelHeightValue</span></span>

<span data-ttu-id="3928b-928">値</span><span class="sxs-lookup"><span data-stu-id="3928b-928">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="3928b-929">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="3928b-929">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="3928b-930">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="3928b-930">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="3928b-931">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="3928b-931">Parameters - labelItalic</span></span>

<span data-ttu-id="3928b-932">値</span><span class="sxs-lookup"><span data-stu-id="3928b-932">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="3928b-933">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="3928b-933">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="3928b-934">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3928b-934">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="3928b-935">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3928b-935">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="3928b-936">x</span><span class="sxs-lookup"><span data-stu-id="3928b-936">x</span></span>  

<!-- -->

<span data-ttu-id="3928b-937">y</span><span class="sxs-lookup"><span data-stu-id="3928b-937">y</span></span>  

<!-- -->

<span data-ttu-id="3928b-938">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-938">button</span></span>  

<!-- -->

<span data-ttu-id="3928b-939">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-939">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="3928b-940">Shift</span><span class="sxs-lookup"><span data-stu-id="3928b-940">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="3928b-941">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3928b-941">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="3928b-942">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="3928b-942">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="3928b-943">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="3928b-943">Parameters - labelMouseDown</span></span>

<span data-ttu-id="3928b-944">x</span><span class="sxs-lookup"><span data-stu-id="3928b-944">x</span></span>  

<!-- -->

<span data-ttu-id="3928b-945">y</span><span class="sxs-lookup"><span data-stu-id="3928b-945">y</span></span>  

<!-- -->

<span data-ttu-id="3928b-946">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-946">button</span></span>  

<!-- -->

<span data-ttu-id="3928b-947">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-947">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="3928b-948">Shift</span><span class="sxs-lookup"><span data-stu-id="3928b-948">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="3928b-949">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="3928b-949">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="3928b-950">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="3928b-950">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="3928b-951">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="3928b-951">Parameters - labelMouseUp</span></span>

<span data-ttu-id="3928b-952">x</span><span class="sxs-lookup"><span data-stu-id="3928b-952">x</span></span>  

<!-- -->

<span data-ttu-id="3928b-953">y</span><span class="sxs-lookup"><span data-stu-id="3928b-953">y</span></span>  

<!-- -->

<span data-ttu-id="3928b-954">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-954">button</span></span>  

<!-- -->

<span data-ttu-id="3928b-955">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-955">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="3928b-956">Shift</span><span class="sxs-lookup"><span data-stu-id="3928b-956">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="3928b-957">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="3928b-957">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="3928b-958">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="3928b-958">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="3928b-959">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="3928b-959">Parameters - labelPosition</span></span>

<span data-ttu-id="3928b-960">値</span><span class="sxs-lookup"><span data-stu-id="3928b-960">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="3928b-961">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="3928b-961">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="3928b-962">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="3928b-962">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="3928b-963">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="3928b-963">Parameters - labelUnderline</span></span>

<span data-ttu-id="3928b-964">値</span><span class="sxs-lookup"><span data-stu-id="3928b-964">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="3928b-965">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="3928b-965">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="3928b-966">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="3928b-966">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="3928b-967">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="3928b-967">Parameters - labelWidth</span></span>

<span data-ttu-id="3928b-968">値</span><span class="sxs-lookup"><span data-stu-id="3928b-968">value</span></span>  

<!-- -->

<span data-ttu-id="3928b-969">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-969">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="3928b-970">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="3928b-970">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="3928b-971">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-971">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="3928b-972">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-972">Parameters - labelWidthMode</span></span>

<span data-ttu-id="3928b-973">値</span><span class="sxs-lookup"><span data-stu-id="3928b-973">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="3928b-974">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-974">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="3928b-975">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-975">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="3928b-976">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-976">Parameters - labelWidthValue</span></span>

<span data-ttu-id="3928b-977">値</span><span class="sxs-lookup"><span data-stu-id="3928b-977">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="3928b-978">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-978">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="3928b-979">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="3928b-979">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="3928b-980">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="3928b-980">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="3928b-981">メソッド left</span><span class="sxs-lookup"><span data-stu-id="3928b-981">Method left</span></span>

<span data-ttu-id="3928b-982">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-982">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="3928b-983">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="3928b-983">Parameters - left</span></span>

<span data-ttu-id="3928b-984">値</span><span class="sxs-lookup"><span data-stu-id="3928b-984">value</span></span>  
<span data-ttu-id="3928b-985">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-985">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="3928b-986">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-986">mode</span></span>  
<span data-ttu-id="3928b-987">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-987">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="3928b-988">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="3928b-988">Return Value - left</span></span>

<span data-ttu-id="3928b-989">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="3928b-989">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="3928b-990">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="3928b-990">Method leftMode</span></span>

<span data-ttu-id="3928b-991">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-991">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="3928b-992">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="3928b-992">Parameters - leftMode</span></span>

<span data-ttu-id="3928b-993">値</span><span class="sxs-lookup"><span data-stu-id="3928b-993">value</span></span>  
<span data-ttu-id="3928b-994">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-994">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="3928b-995">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="3928b-995">Return Value - leftMode</span></span>

<span data-ttu-id="3928b-996">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-996">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="3928b-997">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="3928b-997">Method leftValue</span></span>

<span data-ttu-id="3928b-998">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-998">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="3928b-999">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="3928b-999">Parameters - leftValue</span></span>

<span data-ttu-id="3928b-1000">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1000">value</span></span>  
<span data-ttu-id="3928b-1001">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1001">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="3928b-1002">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1002">Return Value - leftValue</span></span>

<span data-ttu-id="3928b-1003">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="3928b-1003">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="3928b-1004">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="3928b-1004">Method markAsUserAdd</span></span>

<span data-ttu-id="3928b-1005">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="3928b-1005">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="3928b-1006">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="3928b-1006">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="3928b-1007">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1007">value</span></span>  
<span data-ttu-id="3928b-1008">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1008">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="3928b-1009">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="3928b-1009">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="3928b-1010">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3928b-1010">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="3928b-1011">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="3928b-1011">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="3928b-1012">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="3928b-1012">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="3928b-1013">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3928b-1013">Method mouseDblClick</span></span>

<span data-ttu-id="3928b-1014">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1014">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="3928b-1015">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3928b-1015">Parameters - mouseDblClick</span></span>

<span data-ttu-id="3928b-1016">x</span><span class="sxs-lookup"><span data-stu-id="3928b-1016">x</span></span>  
<span data-ttu-id="3928b-1017">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1017">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1018">y</span><span class="sxs-lookup"><span data-stu-id="3928b-1018">y</span></span>  
<span data-ttu-id="3928b-1019">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1019">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1020">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-1020">button</span></span>  
<span data-ttu-id="3928b-1021">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1021">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1022">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-1022">Ctrl</span></span>  
<span data-ttu-id="3928b-1023">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1023">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1024">シフト</span><span class="sxs-lookup"><span data-stu-id="3928b-1024">Shift</span></span>  
<span data-ttu-id="3928b-1025">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1025">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="3928b-1026">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3928b-1026">Return Value - mouseDblClick</span></span>

<span data-ttu-id="3928b-1027">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1027">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="3928b-1028">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3928b-1028">Remarks - mouseDblClick</span></span>

<span data-ttu-id="3928b-1029">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1029">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="3928b-1030">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="3928b-1030">Method mouseDown</span></span>

<span data-ttu-id="3928b-1031">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1031">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="3928b-1032">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="3928b-1032">Parameters - mouseDown</span></span>

<span data-ttu-id="3928b-1033">x</span><span class="sxs-lookup"><span data-stu-id="3928b-1033">x</span></span>  
<span data-ttu-id="3928b-1034">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1034">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1035">y</span><span class="sxs-lookup"><span data-stu-id="3928b-1035">y</span></span>  
<span data-ttu-id="3928b-1036">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1036">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1037">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-1037">button</span></span>  
<span data-ttu-id="3928b-1038">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1038">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1039">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-1039">Ctrl</span></span>  
<span data-ttu-id="3928b-1040">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1040">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1041">シフト</span><span class="sxs-lookup"><span data-stu-id="3928b-1041">Shift</span></span>  
<span data-ttu-id="3928b-1042">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1042">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="3928b-1043">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="3928b-1043">Return Value - mouseDown</span></span>

<span data-ttu-id="3928b-1044">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1044">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="3928b-1045">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="3928b-1045">Remarks - mouseDown</span></span>

<span data-ttu-id="3928b-1046">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1046">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="3928b-1047">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1047">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="3928b-1048">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="3928b-1048">Method mouseMove</span></span>

<span data-ttu-id="3928b-1049">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1049">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="3928b-1050">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="3928b-1050">Parameters - mouseMove</span></span>

<span data-ttu-id="3928b-1051">x</span><span class="sxs-lookup"><span data-stu-id="3928b-1051">x</span></span>  
<span data-ttu-id="3928b-1052">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1052">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1053">y</span><span class="sxs-lookup"><span data-stu-id="3928b-1053">y</span></span>  
<span data-ttu-id="3928b-1054">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1054">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1055">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-1055">button</span></span>  
<span data-ttu-id="3928b-1056">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1056">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1057">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-1057">Ctrl</span></span>  
<span data-ttu-id="3928b-1058">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1058">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1059">シフト</span><span class="sxs-lookup"><span data-stu-id="3928b-1059">Shift</span></span>  
<span data-ttu-id="3928b-1060">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1060">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="3928b-1061">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="3928b-1061">Return Value - mouseMove</span></span>

<span data-ttu-id="3928b-1062">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1062">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="3928b-1063">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="3928b-1063">Remarks - mouseMove</span></span>

<span data-ttu-id="3928b-1064">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1064">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="3928b-1065">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="3928b-1065">Method mouseUp</span></span>

<span data-ttu-id="3928b-1066">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1066">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="3928b-1067">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="3928b-1067">Parameters - mouseUp</span></span>

<span data-ttu-id="3928b-1068">x</span><span class="sxs-lookup"><span data-stu-id="3928b-1068">x</span></span>  
<span data-ttu-id="3928b-1069">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1069">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1070">y</span><span class="sxs-lookup"><span data-stu-id="3928b-1070">y</span></span>  
<span data-ttu-id="3928b-1071">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1071">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1072">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-1072">button</span></span>  
<span data-ttu-id="3928b-1073">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1073">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1074">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-1074">Ctrl</span></span>  
<span data-ttu-id="3928b-1075">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1075">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1076">シフト</span><span class="sxs-lookup"><span data-stu-id="3928b-1076">Shift</span></span>  
<span data-ttu-id="3928b-1077">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1077">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="3928b-1078">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="3928b-1078">Return Value - mouseUp</span></span>

<span data-ttu-id="3928b-1079">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1079">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="3928b-1080">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="3928b-1080">Remarks - mouseUp</span></span>

<span data-ttu-id="3928b-1081">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1081">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="3928b-1082">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1082">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="3928b-1083">メソッド名</span><span class="sxs-lookup"><span data-stu-id="3928b-1083">Method name</span></span>

<span data-ttu-id="3928b-1084">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1084">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="3928b-1085">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="3928b-1085">Parameters - name</span></span>

<span data-ttu-id="3928b-1086">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1086">value</span></span>  
<span data-ttu-id="3928b-1087">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1087">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="3928b-1088">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="3928b-1088">Return Value - name</span></span>

<span data-ttu-id="3928b-1089">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="3928b-1089">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="3928b-1090">備考 - name</span><span class="sxs-lookup"><span data-stu-id="3928b-1090">Remarks - name</span></span>

<span data-ttu-id="3928b-1091">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3928b-1091">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="3928b-1092">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3928b-1092">It must start with a letter.</span></span>
-   <span data-ttu-id="3928b-1093">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="3928b-1093">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="3928b-1094">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1094">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="3928b-1095">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="3928b-1095">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="3928b-1096">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="3928b-1096">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="3928b-1097">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="3928b-1097">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="3928b-1098">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="3928b-1098">Parameters - neededPermission</span></span>

<span data-ttu-id="3928b-1099">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1099">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="3928b-1100">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="3928b-1100">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="3928b-1101">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3928b-1101">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="3928b-1102">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3928b-1102">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="3928b-1103">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="3928b-1103">Method parentControl</span></span>

<span data-ttu-id="3928b-1104">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1104">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="3928b-1105">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="3928b-1105">Return Value - parentControl</span></span>

<span data-ttu-id="3928b-1106">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="3928b-1106">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="3928b-1107">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="3928b-1107">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="3928b-1108">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="3928b-1108">Parameters - previewPartRef</span></span>

<span data-ttu-id="3928b-1109">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1109">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="3928b-1110">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="3928b-1110">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="3928b-1111">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="3928b-1111">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="3928b-1112">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="3928b-1112">Parameters - promptrect</span></span>

<span data-ttu-id="3928b-1113">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1113">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="3928b-1114">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="3928b-1114">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="3928b-1115">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="3928b-1115">Method securityKey</span></span>

<span data-ttu-id="3928b-1116">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1116">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="3928b-1117">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="3928b-1117">Parameters - securityKey</span></span>

<span data-ttu-id="3928b-1118">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1118">value</span></span>  
<span data-ttu-id="3928b-1119">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1119">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="3928b-1120">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="3928b-1120">Return Value - securityKey</span></span>

<span data-ttu-id="3928b-1121">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1121">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-selection"></a><span data-ttu-id="3928b-1122">メソッド selection</span><span class="sxs-lookup"><span data-stu-id="3928b-1122">Method selection</span></span>

```xpp
public int selection([int value])
```

### <a name="parameters---selection"></a><span data-ttu-id="3928b-1123">パラメーター - selection</span><span class="sxs-lookup"><span data-stu-id="3928b-1123">Parameters - selection</span></span>

<span data-ttu-id="3928b-1124">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1124">value</span></span>  

### <a name="return-value---selection"></a><span data-ttu-id="3928b-1125">戻り値 - selection</span><span class="sxs-lookup"><span data-stu-id="3928b-1125">Return Value - selection</span></span>

## <a name="method-selectionchange"></a><span data-ttu-id="3928b-1126">メソッド selectionChange</span><span class="sxs-lookup"><span data-stu-id="3928b-1126">Method selectionChange</span></span>

```xpp
public int selectionChange()
```

### <a name="return-value---selectionchange"></a><span data-ttu-id="3928b-1127">戻り値 - selectionChange</span><span class="sxs-lookup"><span data-stu-id="3928b-1127">Return Value - selectionChange</span></span>

## <a name="method-selecttext"></a><span data-ttu-id="3928b-1128">メソッド selectText</span><span class="sxs-lookup"><span data-stu-id="3928b-1128">Method selectText</span></span>

```xpp
public int selectText(str string)
```

### <a name="parameters---selecttext"></a><span data-ttu-id="3928b-1129">パラメーター - selectText</span><span class="sxs-lookup"><span data-stu-id="3928b-1129">Parameters - selectText</span></span>

<span data-ttu-id="3928b-1130">文字列</span><span class="sxs-lookup"><span data-stu-id="3928b-1130">string</span></span>  

### <a name="return-value---selecttext"></a><span data-ttu-id="3928b-1131">戻り値 - selectText</span><span class="sxs-lookup"><span data-stu-id="3928b-1131">Return Value - selectText</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="3928b-1132">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="3928b-1132">Method showContextMenu</span></span>

<span data-ttu-id="3928b-1133">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1133">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="3928b-1134">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="3928b-1134">Parameters - showContextMenu</span></span>

<span data-ttu-id="3928b-1135">menuHandle</span><span class="sxs-lookup"><span data-stu-id="3928b-1135">menuHandle</span></span>  
<span data-ttu-id="3928b-1136">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="3928b-1136">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="3928b-1137">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="3928b-1137">Return Value - showContextMenu</span></span>

<span data-ttu-id="3928b-1138">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1138">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="3928b-1139">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="3928b-1139">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="3928b-1140">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="3928b-1140">Parameters - showLabel</span></span>

<span data-ttu-id="3928b-1141">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1141">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="3928b-1142">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="3928b-1142">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="3928b-1143">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="3928b-1143">Method skip</span></span>

<span data-ttu-id="3928b-1144">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1144">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="3928b-1145">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="3928b-1145">Parameters - skip</span></span>

<span data-ttu-id="3928b-1146">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1146">value</span></span>  
<span data-ttu-id="3928b-1147">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1147">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="3928b-1148">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="3928b-1148">Return Value - skip</span></span>

<span data-ttu-id="3928b-1149">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3928b-1149">true if the control is skipped when the user presses the TAB key to move to the control; otherwise false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="3928b-1150">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="3928b-1150">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="3928b-1151">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="3928b-1151">Parameters - sort</span></span>

<span data-ttu-id="3928b-1152">sortDirection</span><span class="sxs-lookup"><span data-stu-id="3928b-1152">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="3928b-1153">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="3928b-1153">Return Value - sort</span></span>

## <a name="method-text"></a><span data-ttu-id="3928b-1154">メソッド text</span><span class="sxs-lookup"><span data-stu-id="3928b-1154">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="3928b-1155">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="3928b-1155">Parameters - text</span></span>

<span data-ttu-id="3928b-1156">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1156">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="3928b-1157">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="3928b-1157">Return Value - text</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="3928b-1158">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="3928b-1158">Method toolTip</span></span>

<span data-ttu-id="3928b-1159">コントロールのツールヒントを取得します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1159">Retrieves a tooltip for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="3928b-1160">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="3928b-1160">Return Value - toolTip</span></span>

<span data-ttu-id="3928b-1161">ツールヒントに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="3928b-1161">The text to show in the tooltip.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="3928b-1162">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="3928b-1162">Remarks - toolTip</span></span>

<span data-ttu-id="3928b-1163">ポインターをコントロール上に移動するときはいつでも、ツールヒントがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1163">Whenever the pointer hovers over the control, the tooltip is displayed to the user.</span></span> <span data-ttu-id="3928b-1164">このメソッドをオーバーライドして、コントロールに入力された値についてユーザーに指示テキストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1164">This method can be overridden to present instructive text to the user about the values that are entered in the control.</span></span>

### <a name="examples---tooltip"></a><span data-ttu-id="3928b-1165">例 - toolTip</span><span class="sxs-lookup"><span data-stu-id="3928b-1165">Examples - toolTip</span></span>

```xpp
str tooltip() 
{ 
    return "Account numbers of customers eligible for discount"; 
}
```

## <a name="method-top"></a><span data-ttu-id="3928b-1166">メソッド top</span><span class="sxs-lookup"><span data-stu-id="3928b-1166">Method top</span></span>

<span data-ttu-id="3928b-1167">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1167">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="3928b-1168">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="3928b-1168">Parameters - top</span></span>

<span data-ttu-id="3928b-1169">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1169">value</span></span>  
<span data-ttu-id="3928b-1170">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1170">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="3928b-1171">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-1171">mode</span></span>  
<span data-ttu-id="3928b-1172">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1172">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="3928b-1173">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="3928b-1173">Return Value - top</span></span>

<span data-ttu-id="3928b-1174">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="3928b-1174">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="3928b-1175">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1175">Method topMode</span></span>

<span data-ttu-id="3928b-1176">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1176">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="3928b-1177">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1177">Parameters - topMode</span></span>

<span data-ttu-id="3928b-1178">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1178">value</span></span>  
<span data-ttu-id="3928b-1179">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1179">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="3928b-1180">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1180">Return Value - topMode</span></span>

<span data-ttu-id="3928b-1181">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-1181">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="3928b-1182">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1182">Method topValue</span></span>

<span data-ttu-id="3928b-1183">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1183">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="3928b-1184">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1184">Parameters - topValue</span></span>

<span data-ttu-id="3928b-1185">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1185">value</span></span>  
<span data-ttu-id="3928b-1186">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1186">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="3928b-1187">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1187">Return Value - topValue</span></span>

<span data-ttu-id="3928b-1188">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="3928b-1188">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="3928b-1189">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="3928b-1189">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="3928b-1190">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="3928b-1190">Parameters - type</span></span>

<span data-ttu-id="3928b-1191">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1191">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="3928b-1192">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="3928b-1192">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="3928b-1193">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="3928b-1193">Method underline</span></span>

<span data-ttu-id="3928b-1194">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1194">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="3928b-1195">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="3928b-1195">Parameters - underline</span></span>

<span data-ttu-id="3928b-1196">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1196">value</span></span>  
<span data-ttu-id="3928b-1197">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1197">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="3928b-1198">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="3928b-1198">Return Value - underline</span></span>

<span data-ttu-id="3928b-1199">コントロール内のテキストが下線付きである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3928b-1199">true if the text in the control is underlined; otherwise false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="3928b-1200">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3928b-1200">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="3928b-1201">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3928b-1201">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="3928b-1202">データ</span><span class="sxs-lookup"><span data-stu-id="3928b-1202">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="3928b-1203">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3928b-1203">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="3928b-1204">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="3928b-1204">Method userData</span></span>

<span data-ttu-id="3928b-1205">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1205">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="3928b-1206">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="3928b-1206">Parameters - userData</span></span>

<span data-ttu-id="3928b-1207">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1207">value</span></span>  
<span data-ttu-id="3928b-1208">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1208">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="3928b-1209">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="3928b-1209">Return Value - userData</span></span>

<span data-ttu-id="3928b-1210">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="3928b-1210">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="3928b-1211">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="3928b-1211">Method userDataItem</span></span>

<span data-ttu-id="3928b-1212">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1212">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="3928b-1213">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="3928b-1213">Parameters - userDataItem</span></span>

<span data-ttu-id="3928b-1214">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1214">value</span></span>  
<span data-ttu-id="3928b-1215">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1215">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="3928b-1216">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="3928b-1216">Return Value - userDataItem</span></span>

<span data-ttu-id="3928b-1217">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="3928b-1217">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="3928b-1218">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="3928b-1218">Method userDataItems</span></span>

<span data-ttu-id="3928b-1219">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1219">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="3928b-1220">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="3928b-1220">Parameters - userDataItems</span></span>

<span data-ttu-id="3928b-1221">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1221">value</span></span>  
<span data-ttu-id="3928b-1222">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1222">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="3928b-1223">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="3928b-1223">Return Value - userDataItems</span></span>

<span data-ttu-id="3928b-1224">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="3928b-1224">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="3928b-1225">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="3928b-1225">Method userDisable</span></span>

<span data-ttu-id="3928b-1226">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1226">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="3928b-1227">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="3928b-1227">Parameters - userDisable</span></span>

<span data-ttu-id="3928b-1228">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1228">value</span></span>  
<span data-ttu-id="3928b-1229">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1229">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="3928b-1230">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="3928b-1230">Return Value - userDisable</span></span>

<span data-ttu-id="3928b-1231">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1231">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="3928b-1232">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="3928b-1232">Method userHeight</span></span>

<span data-ttu-id="3928b-1233">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1233">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="3928b-1234">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="3928b-1234">Parameters - userHeight</span></span>

<span data-ttu-id="3928b-1235">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1235">value</span></span>  
<span data-ttu-id="3928b-1236">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1236">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="3928b-1237">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="3928b-1237">Return Value - userHeight</span></span>

<span data-ttu-id="3928b-1238">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="3928b-1238">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="3928b-1239">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="3928b-1239">Method userHide</span></span>

<span data-ttu-id="3928b-1240">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1240">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="3928b-1241">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="3928b-1241">Parameters - userHide</span></span>

<span data-ttu-id="3928b-1242">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1242">value</span></span>  
<span data-ttu-id="3928b-1243">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1243">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="3928b-1244">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="3928b-1244">Return Value - userHide</span></span>

<span data-ttu-id="3928b-1245">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1245">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="3928b-1246">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="3928b-1246">Remarks - userHide</span></span>

<span data-ttu-id="3928b-1247">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1247">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="3928b-1248">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1248">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="3928b-1249">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1249">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="3928b-1250">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="3928b-1250">Method userOrgContainer</span></span>

<span data-ttu-id="3928b-1251">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1251">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="3928b-1252">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="3928b-1252">Parameters - userOrgContainer</span></span>

<span data-ttu-id="3928b-1253">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1253">value</span></span>  
<span data-ttu-id="3928b-1254">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1254">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="3928b-1255">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="3928b-1255">Return Value - userOrgContainer</span></span>

<span data-ttu-id="3928b-1256">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="3928b-1256">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="3928b-1257">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="3928b-1257">Method userOrgSibling</span></span>

<span data-ttu-id="3928b-1258">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1258">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="3928b-1259">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="3928b-1259">Parameters - userOrgSibling</span></span>

<span data-ttu-id="3928b-1260">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1260">value</span></span>  
<span data-ttu-id="3928b-1261">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1261">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="3928b-1262">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="3928b-1262">Return Value - userOrgSibling</span></span>

<span data-ttu-id="3928b-1263">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="3928b-1263">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="3928b-1264">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="3928b-1264">Method userPromptText</span></span>

<span data-ttu-id="3928b-1265">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1265">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="3928b-1266">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="3928b-1266">Parameters - userPromptText</span></span>

<span data-ttu-id="3928b-1267">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1267">value</span></span>  
<span data-ttu-id="3928b-1268">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1268">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="3928b-1269">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="3928b-1269">Return Value - userPromptText</span></span>

<span data-ttu-id="3928b-1270">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="3928b-1270">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="3928b-1271">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="3928b-1271">Method userSecurityLevel</span></span>

<span data-ttu-id="3928b-1272">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1272">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="3928b-1273">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="3928b-1273">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="3928b-1274">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1274">value</span></span>  
<span data-ttu-id="3928b-1275">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1275">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="3928b-1276">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="3928b-1276">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="3928b-1277">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="3928b-1277">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="3928b-1278">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="3928b-1278">Method userSkip</span></span>

<span data-ttu-id="3928b-1279">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1279">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="3928b-1280">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="3928b-1280">Parameters - userSkip</span></span>

<span data-ttu-id="3928b-1281">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1281">value</span></span>  
<span data-ttu-id="3928b-1282">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1282">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="3928b-1283">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1283">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="3928b-1284">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="3928b-1284">Return Value - userSkip</span></span>

<span data-ttu-id="3928b-1285">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="3928b-1285">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="3928b-1286">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="3928b-1286">Method userWidth</span></span>

<span data-ttu-id="3928b-1287">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1287">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="3928b-1288">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="3928b-1288">Parameters - userWidth</span></span>

<span data-ttu-id="3928b-1289">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1289">value</span></span>  
<span data-ttu-id="3928b-1290">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1290">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="3928b-1291">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="3928b-1291">Return Value - userWidth</span></span>

<span data-ttu-id="3928b-1292">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1292">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="3928b-1293">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="3928b-1293">Remarks - userWidth</span></span>

<span data-ttu-id="3928b-1294">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1294">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="3928b-1295">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="3928b-1295">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="3928b-1296">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1296">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="3928b-1297">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="3928b-1297">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="3928b-1298">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="3928b-1298">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="3928b-1299">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3928b-1299">Method verticalSpacing</span></span>

<span data-ttu-id="3928b-1300">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1300">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="3928b-1301">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3928b-1301">Parameters - verticalSpacing</span></span>

<span data-ttu-id="3928b-1302">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1302">value</span></span>  
<span data-ttu-id="3928b-1303">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1303">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="3928b-1304">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-1304">mode</span></span>  
<span data-ttu-id="3928b-1305">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1305">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="3928b-1306">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3928b-1306">Return Value - verticalSpacing</span></span>

<span data-ttu-id="3928b-1307">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="3928b-1307">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="3928b-1308">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1308">Method verticalSpacingMode</span></span>

<span data-ttu-id="3928b-1309">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1309">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="3928b-1310">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1310">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="3928b-1311">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-1311">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="3928b-1312">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1312">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="3928b-1313">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-1313">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="3928b-1314">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1314">Method verticalSpacingValue</span></span>

<span data-ttu-id="3928b-1315">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1315">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="3928b-1316">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1316">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="3928b-1317">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1317">value</span></span>  
<span data-ttu-id="3928b-1318">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1318">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="3928b-1319">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1319">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="3928b-1320">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="3928b-1320">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="3928b-1321">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1321">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="3928b-1322">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1322">Parameters - viewEditMode</span></span>

<span data-ttu-id="3928b-1323">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1323">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="3928b-1324">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1324">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="3928b-1325">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="3928b-1325">Method visible</span></span>

<span data-ttu-id="3928b-1326">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1326">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="3928b-1327">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="3928b-1327">Parameters - visible</span></span>

<span data-ttu-id="3928b-1328">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1328">value</span></span>  
<span data-ttu-id="3928b-1329">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1329">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="3928b-1330">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="3928b-1330">Return Value - visible</span></span>

<span data-ttu-id="3928b-1331">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3928b-1331">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="3928b-1332">メソッド width</span><span class="sxs-lookup"><span data-stu-id="3928b-1332">Method width</span></span>

<span data-ttu-id="3928b-1333">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1333">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="3928b-1334">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="3928b-1334">Parameters - width</span></span>

<span data-ttu-id="3928b-1335">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1335">value</span></span>  
<span data-ttu-id="3928b-1336">幅の計算方法を示す整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1336">An integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="3928b-1337">モード</span><span class="sxs-lookup"><span data-stu-id="3928b-1337">mode</span></span>  
<span data-ttu-id="3928b-1338">幅の計算方法を示す整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1338">An integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="3928b-1339">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="3928b-1339">Return Value - width</span></span>

<span data-ttu-id="3928b-1340">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="3928b-1340">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="3928b-1341">備考 - width</span><span class="sxs-lookup"><span data-stu-id="3928b-1341">Remarks - width</span></span>

<span data-ttu-id="3928b-1342">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1342">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="3928b-1343">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="3928b-1343">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="3928b-1344">モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-1344">Mode.</span></span>           | <span data-ttu-id="3928b-1345">幅計算。</span><span class="sxs-lookup"><span data-stu-id="3928b-1345">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3928b-1346">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="3928b-1346">-1 Exact.</span></span>       | <span data-ttu-id="3928b-1347">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1347">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3928b-1348">0 自動。</span><span class="sxs-lookup"><span data-stu-id="3928b-1348">0 Auto.</span></span>         | <span data-ttu-id="3928b-1349">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1349">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3928b-1350">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="3928b-1350">1 Column width.</span></span> | <span data-ttu-id="3928b-1351">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="3928b-1351">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="3928b-1352">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1352">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="3928b-1353">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1353">Method widthMode</span></span>

<span data-ttu-id="3928b-1354">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1354">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="3928b-1355">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1355">Parameters - widthMode</span></span>

<span data-ttu-id="3928b-1356">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1356">value</span></span>  
<span data-ttu-id="3928b-1357">コントロールの幅の計算方法を示す整数データ型値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1357">An integer data type value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="3928b-1358">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1358">Return Value - widthMode</span></span>

<span data-ttu-id="3928b-1359">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1359">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="3928b-1360">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1360">Remarks - widthMode</span></span>

<span data-ttu-id="3928b-1361">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="3928b-1361">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="3928b-1362">モード。</span><span class="sxs-lookup"><span data-stu-id="3928b-1362">Mode.</span></span>         | <span data-ttu-id="3928b-1363">幅計算。</span><span class="sxs-lookup"><span data-stu-id="3928b-1363">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3928b-1364">正確。</span><span class="sxs-lookup"><span data-stu-id="3928b-1364">Exact.</span></span>        | <span data-ttu-id="3928b-1365">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1365">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3928b-1366">自動。</span><span class="sxs-lookup"><span data-stu-id="3928b-1366">Auto.</span></span>         | <span data-ttu-id="3928b-1367">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1367">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3928b-1368">列の幅。</span><span class="sxs-lookup"><span data-stu-id="3928b-1368">Column width.</span></span> | <span data-ttu-id="3928b-1369">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="3928b-1369">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="3928b-1370">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="3928b-1370">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="3928b-1371">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1371">Method widthValue</span></span>

<span data-ttu-id="3928b-1372">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1372">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="3928b-1373">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1373">Parameters - widthValue</span></span>

<span data-ttu-id="3928b-1374">値</span><span class="sxs-lookup"><span data-stu-id="3928b-1374">value</span></span>  
<span data-ttu-id="3928b-1375">幅をピクセル単位で指定する整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3928b-1375">An integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="3928b-1376">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1376">Return Value - widthValue</span></span>

<span data-ttu-id="3928b-1377">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="3928b-1377">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="3928b-1378">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="3928b-1378">Remarks - widthValue</span></span>

<span data-ttu-id="3928b-1379">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1379">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="3928b-1380">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="3928b-1380">Method dragLeave</span></span>

<span data-ttu-id="3928b-1381">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1381">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-filter"></a><span data-ttu-id="3928b-1382">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="3928b-1382">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="3928b-1383">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="3928b-1383">Parameters - filter</span></span>

<span data-ttu-id="3928b-1384">filterStr</span><span class="sxs-lookup"><span data-stu-id="3928b-1384">filterStr</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="3928b-1385">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="3928b-1385">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="3928b-1386">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="3928b-1386">Parameters - OnLeaving</span></span>

<span data-ttu-id="3928b-1387">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1387">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1388">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1388">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="3928b-1389">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="3928b-1389">Method lostFocus</span></span>

<span data-ttu-id="3928b-1390">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1390">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-copy"></a><span data-ttu-id="3928b-1391">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="3928b-1391">Method copy</span></span>

<span data-ttu-id="3928b-1392">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="3928b-1392">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-cut"></a><span data-ttu-id="3928b-1393">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="3928b-1393">Method cut</span></span>

<span data-ttu-id="3928b-1394">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="3928b-1394">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-insert"></a><span data-ttu-id="3928b-1395">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="3928b-1395">Method insert</span></span>

```xpp
public void insert(str string, int index)
```

### <a name="parameters---insert"></a><span data-ttu-id="3928b-1396">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="3928b-1396">Parameters - insert</span></span>

<span data-ttu-id="3928b-1397">文字列</span><span class="sxs-lookup"><span data-stu-id="3928b-1397">string</span></span>  

<!-- -->

<span data-ttu-id="3928b-1398">指数</span><span class="sxs-lookup"><span data-stu-id="3928b-1398">index</span></span>  

## <a name="method-delete"></a><span data-ttu-id="3928b-1399">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="3928b-1399">Method delete</span></span>

```xpp
public void delete(str string)
```

### <a name="parameters---delete"></a><span data-ttu-id="3928b-1400">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="3928b-1400">Parameters - delete</span></span>

<span data-ttu-id="3928b-1401">文字列</span><span class="sxs-lookup"><span data-stu-id="3928b-1401">string</span></span>  

## <a name="method-context"></a><span data-ttu-id="3928b-1402">メソッド context</span><span class="sxs-lookup"><span data-stu-id="3928b-1402">Method context</span></span>

<span data-ttu-id="3928b-1403">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1403">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enter"></a><span data-ttu-id="3928b-1404">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="3928b-1404">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-enddrag"></a><span data-ttu-id="3928b-1405">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="3928b-1405">Method endDrag</span></span>

<span data-ttu-id="3928b-1406">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1406">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="3928b-1407">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="3928b-1407">Remarks - endDrag</span></span>

<span data-ttu-id="3928b-1408">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="3928b-1408">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="3928b-1409">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1409">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="3928b-1410">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="3928b-1410">Method resetUserSetting</span></span>

<span data-ttu-id="3928b-1411">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="3928b-1411">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="3928b-1412">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="3928b-1412">Method prefColumnSize</span></span>

<span data-ttu-id="3928b-1413">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1413">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="3928b-1414">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="3928b-1414">Parameters - prefColumnSize</span></span>

<span data-ttu-id="3928b-1415">width</span><span class="sxs-lookup"><span data-stu-id="3928b-1415">width</span></span>  
<span data-ttu-id="3928b-1416">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="3928b-1416">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="3928b-1417">height</span><span class="sxs-lookup"><span data-stu-id="3928b-1417">height</span></span>  
<span data-ttu-id="3928b-1418">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="3928b-1418">The preferred height of the control.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="3928b-1419">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="3928b-1419">Method mouseEnter</span></span>

<span data-ttu-id="3928b-1420">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1420">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="3928b-1421">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="3928b-1421">Parameters - mouseEnter</span></span>

<span data-ttu-id="3928b-1422">x</span><span class="sxs-lookup"><span data-stu-id="3928b-1422">x</span></span>  
<span data-ttu-id="3928b-1423">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1423">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1424">y</span><span class="sxs-lookup"><span data-stu-id="3928b-1424">y</span></span>  
<span data-ttu-id="3928b-1425">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1425">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1426">ボタン</span><span class="sxs-lookup"><span data-stu-id="3928b-1426">button</span></span>  
<span data-ttu-id="3928b-1427">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1427">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1428">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3928b-1428">Ctrl</span></span>  
<span data-ttu-id="3928b-1429">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1429">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3928b-1430">シフト</span><span class="sxs-lookup"><span data-stu-id="3928b-1430">Shift</span></span>  
<span data-ttu-id="3928b-1431">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1431">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-drop"></a><span data-ttu-id="3928b-1432">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="3928b-1432">Method drop</span></span>

<span data-ttu-id="3928b-1433">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1433">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="3928b-1434">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="3928b-1434">Parameters - drop</span></span>

<span data-ttu-id="3928b-1435">dragSource</span><span class="sxs-lookup"><span data-stu-id="3928b-1435">dragSource</span></span>  
<span data-ttu-id="3928b-1436">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1436">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-1437">dragMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1437">dragMode</span></span>  
<span data-ttu-id="3928b-1438">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1438">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-1439">x</span><span class="sxs-lookup"><span data-stu-id="3928b-1439">x</span></span>  
<span data-ttu-id="3928b-1440">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1440">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-1441">y</span><span class="sxs-lookup"><span data-stu-id="3928b-1441">y</span></span>  
<span data-ttu-id="3928b-1442">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1442">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="3928b-1443">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="3928b-1443">Method setFocus</span></span>

<span data-ttu-id="3928b-1444">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1444">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-paste"></a><span data-ttu-id="3928b-1445">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="3928b-1445">Method paste</span></span>

<span data-ttu-id="3928b-1446">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1446">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="3928b-1447">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-1447">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="3928b-1448">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="3928b-1448">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="3928b-1449">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="3928b-1449">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="3928b-1450">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="3928b-1450">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="3928b-1451">overrideObject</span><span class="sxs-lookup"><span data-stu-id="3928b-1451">overrideObject</span></span>  

## <a name="method-add"></a><span data-ttu-id="3928b-1452">メソッド add</span><span class="sxs-lookup"><span data-stu-id="3928b-1452">Method add</span></span>

```xpp
public void add(str string)
```

### <a name="parameters---add"></a><span data-ttu-id="3928b-1453">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="3928b-1453">Parameters - add</span></span>

<span data-ttu-id="3928b-1454">文字列</span><span class="sxs-lookup"><span data-stu-id="3928b-1454">string</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="3928b-1455">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="3928b-1455">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="3928b-1456">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="3928b-1456">Parameters - OnValidated</span></span>

<span data-ttu-id="3928b-1457">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1457">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1458">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1458">e</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="3928b-1459">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="3928b-1459">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="3928b-1460">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="3928b-1460">Parameters - OnModified</span></span>

<span data-ttu-id="3928b-1461">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1461">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1462">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1462">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="3928b-1463">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="3928b-1463">Method dropEx</span></span>

<span data-ttu-id="3928b-1464">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3928b-1464">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="3928b-1465">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="3928b-1465">Parameters - dropEx</span></span>

<span data-ttu-id="3928b-1466">dragSource</span><span class="sxs-lookup"><span data-stu-id="3928b-1466">dragSource</span></span>  
<span data-ttu-id="3928b-1467">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1467">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-1468">dragMode</span><span class="sxs-lookup"><span data-stu-id="3928b-1468">dragMode</span></span>  
<span data-ttu-id="3928b-1469">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1469">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-1470">x</span><span class="sxs-lookup"><span data-stu-id="3928b-1470">x</span></span>  
<span data-ttu-id="3928b-1471">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1471">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3928b-1472">y</span><span class="sxs-lookup"><span data-stu-id="3928b-1472">y</span></span>  
<span data-ttu-id="3928b-1473">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3928b-1473">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-undo"></a><span data-ttu-id="3928b-1474">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="3928b-1474">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-endupdate"></a><span data-ttu-id="3928b-1475">メソッド endUpdate</span><span class="sxs-lookup"><span data-stu-id="3928b-1475">Method endUpdate</span></span>

```xpp
public void endUpdate()
```

## <a name="method-clear"></a><span data-ttu-id="3928b-1476">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="3928b-1476">Method clear</span></span>

```xpp
public void clear()
```

## <a name="method-beginupdate"></a><span data-ttu-id="3928b-1477">メソッド beginUpdate</span><span class="sxs-lookup"><span data-stu-id="3928b-1477">Method beginUpdate</span></span>

```xpp
public void beginUpdate()
```

## <a name="method-jumpref"></a><span data-ttu-id="3928b-1478">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="3928b-1478">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onlookup"></a><span data-ttu-id="3928b-1479">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="3928b-1479">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="3928b-1480">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="3928b-1480">Parameters - OnLookup</span></span>

<span data-ttu-id="3928b-1481">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1481">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1482">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1482">e</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="3928b-1483">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="3928b-1483">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="3928b-1484">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="3928b-1484">Parameters - OnLostFocus</span></span>

<span data-ttu-id="3928b-1485">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1485">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1486">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1486">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="3928b-1487">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="3928b-1487">Method inputSearch</span></span>

<span data-ttu-id="3928b-1488">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1488">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="3928b-1489">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="3928b-1489">Parameters - inputSearch</span></span>

<span data-ttu-id="3928b-1490">searchStr</span><span class="sxs-lookup"><span data-stu-id="3928b-1490">searchStr</span></span>  
<span data-ttu-id="3928b-1491">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3928b-1491">The string value to use to filter data; optional.</span></span>

## <a name="method-onselectionchanging"></a><span data-ttu-id="3928b-1492">メソッド OnSelectionChanging</span><span class="sxs-lookup"><span data-stu-id="3928b-1492">Method OnSelectionChanging</span></span>

```xpp
private void OnSelectionChanging([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanging"></a><span data-ttu-id="3928b-1493">パラメーター - OnSelectionChanging</span><span class="sxs-lookup"><span data-stu-id="3928b-1493">Parameters - OnSelectionChanging</span></span>

<span data-ttu-id="3928b-1494">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1494">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1495">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1495">e</span></span>  

## <a name="method-lookup"></a><span data-ttu-id="3928b-1496">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="3928b-1496">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-mouseleave"></a><span data-ttu-id="3928b-1497">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="3928b-1497">Method mouseLeave</span></span>

<span data-ttu-id="3928b-1498">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1498">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-gotfocus"></a><span data-ttu-id="3928b-1499">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="3928b-1499">Method gotFocus</span></span>

<span data-ttu-id="3928b-1500">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1500">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="3928b-1501">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="3928b-1501">Method displayControl</span></span>

<span data-ttu-id="3928b-1502">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="3928b-1502">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onenter"></a><span data-ttu-id="3928b-1503">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="3928b-1503">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="3928b-1504">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="3928b-1504">Parameters - OnEnter</span></span>

<span data-ttu-id="3928b-1505">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1505">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1506">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1506">e</span></span>  

## <a name="method-ongotfocus"></a><span data-ttu-id="3928b-1507">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="3928b-1507">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="3928b-1508">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="3928b-1508">Parameters - OnGotFocus</span></span>

<span data-ttu-id="3928b-1509">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1509">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1510">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1510">e</span></span>  

## <a name="method-onselectionchanged"></a><span data-ttu-id="3928b-1511">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="3928b-1511">Method OnSelectionChanged</span></span>

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a><span data-ttu-id="3928b-1512">パラメーター - OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="3928b-1512">Parameters - OnSelectionChanged</span></span>

<span data-ttu-id="3928b-1513">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1513">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1514">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1514">e</span></span>  

## <a name="method-onvalidating"></a><span data-ttu-id="3928b-1515">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="3928b-1515">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="3928b-1516">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="3928b-1516">Parameters - OnValidating</span></span>

<span data-ttu-id="3928b-1517">sender</span><span class="sxs-lookup"><span data-stu-id="3928b-1517">sender</span></span>  

<!-- -->

<span data-ttu-id="3928b-1518">e</span><span class="sxs-lookup"><span data-stu-id="3928b-1518">e</span></span>  

