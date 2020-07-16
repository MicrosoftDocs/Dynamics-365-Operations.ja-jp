---
title: FormReferenceGroupControl クラス
description: このトピックでは、FormReferenceGroupControl クラスについて説明します。
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
ms.openlocfilehash: c5d7a7cfed5729411a0eb9fc827f262360b937dc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502627"
---
# <a name="class-formreferencegroupcontrol"></a><span data-ttu-id="329fb-103">クラス FormReferenceGroupControl</span><span class="sxs-lookup"><span data-stu-id="329fb-103">Class FormReferenceGroupControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormReferenceGroupControl extends FormReferenceControl
```

## <a name="remarks"></a><span data-ttu-id="329fb-104">備考</span><span class="sxs-lookup"><span data-stu-id="329fb-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="329fb-105">例</span><span class="sxs-lookup"><span data-stu-id="329fb-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="329fb-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="329fb-106">Methods</span></span>

| <span data-ttu-id="329fb-107">方法</span><span class="sxs-lookup"><span data-stu-id="329fb-107">Method</span></span>                                                                                                              | <span data-ttu-id="329fb-108">説明</span><span class="sxs-lookup"><span data-stu-id="329fb-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329fb-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="329fb-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="329fb-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="329fb-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="329fb-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="329fb-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="329fb-112">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-112">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="329fb-113">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-113">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="329fb-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="329fb-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-115">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="329fb-116">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="329fb-116">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="329fb-117">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-117">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="329fb-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="329fb-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="329fb-120">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-120">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="329fb-121">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-121">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="329fb-122">public Image backgroundImage(\[Image image\], \[int drawMode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-122">public Image backgroundImage(\[Image image\], \[int drawMode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="329fb-123">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-123">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="329fb-124">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-124">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="329fb-125">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="329fb-125">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="329fb-126">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-126">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="329fb-127">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-127">public int bold(\[int value\])</span></span>                                                                                      | <span data-ttu-id="329fb-128">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-128">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="329fb-129">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-129">public int border(\[int value\])</span></span>                                                                                    | <span data-ttu-id="329fb-130">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-130">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="329fb-131">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="329fb-131">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="329fb-132">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-132">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="329fb-133">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="329fb-133">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="329fb-134">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="329fb-134">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="329fb-135">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-135">public int characterSet(\[int value\])</span></span>                                                                              | <span data-ttu-id="329fb-136">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-136">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="329fb-137">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-137">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="329fb-138">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-138">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="329fb-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="329fb-140">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-140">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="329fb-141">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="329fb-141">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="329fb-142">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-142">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="329fb-143">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="329fb-143">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="329fb-144">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="329fb-144">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="329fb-145">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="329fb-145">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="329fb-146">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-146">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="329fb-147">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-147">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="329fb-148">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-148">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-149">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-149">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="329fb-150">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-150">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="329fb-151">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-151">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="329fb-152">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-152">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="329fb-153">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-153">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="329fb-154">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-154">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="329fb-155">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-155">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="329fb-156">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-156">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="329fb-157">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="329fb-157">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="329fb-158">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-158">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="329fb-159">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="329fb-159">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="329fb-160">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-160">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="329fb-161">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="329fb-161">public str dragText()</span></span>                                                                                               | <span data-ttu-id="329fb-162">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-162">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="329fb-163">public boolean enableChilds(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="329fb-163">public boolean enableChilds(\[boolean enable\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="329fb-164">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-164">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="329fb-165">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-165">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="329fb-166">public boolean expand(\[boolean expand\])</span><span class="sxs-lookup"><span data-stu-id="329fb-166">public boolean expand(\[boolean expand\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="329fb-167">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-167">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="329fb-168">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-168">public str font(\[str value\])</span></span>                                                                                      | <span data-ttu-id="329fb-169">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-169">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="329fb-170">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-170">public int fontSize(\[int value\])</span></span>                                                                                  | <span data-ttu-id="329fb-171">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-171">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="329fb-172">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-172">public int foregroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="329fb-173">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-173">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="329fb-174">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="329fb-174">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="329fb-175">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-175">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="329fb-176">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="329fb-176">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="329fb-177">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-177">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="329fb-178">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-178">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="329fb-179">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-179">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="329fb-180">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-180">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="329fb-181">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-181">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="329fb-182">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-182">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="329fb-183">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-183">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="329fb-184">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="329fb-184">public str helpField()</span></span>                                                                                              | <span data-ttu-id="329fb-185">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-185">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="329fb-186">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-186">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="329fb-187">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-187">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="329fb-188">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-188">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="329fb-189">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-189">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="329fb-190">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-190">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="329fb-191">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="329fb-191">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="329fb-192">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-192">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="329fb-193">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="329fb-193">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="329fb-194">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="329fb-194">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="329fb-195">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-195">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="329fb-196">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="329fb-196">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="329fb-197">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-197">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="329fb-198">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="329fb-198">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="329fb-199">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-199">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="329fb-200">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="329fb-200">public boolean isValid()</span></span>                                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="329fb-201">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-201">public boolean italic(\[boolean value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="329fb-202">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-202">public str label(\[str value\])</span></span>                                                                                     | <span data-ttu-id="329fb-203">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-203">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="329fb-204">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-204">public int labelAlignment(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="329fb-205">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-205">public int labelBold(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="329fb-206">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-206">public int labelCharacterSet(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-207">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-207">public str labelFont(\[str value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="329fb-208">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-208">public int labelFontSize(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="329fb-209">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-209">public int labelForegroundColor(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="329fb-210">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-210">public int labelGuide(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="329fb-211">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-211">public int labelHeight(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="329fb-212">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-212">public int labelHeightMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="329fb-213">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-213">public int labelHeightValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="329fb-214">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-214">public boolean labelItalic(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="329fb-215">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-215">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="329fb-216">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-216">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="329fb-217">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-217">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                      |                                                                                                                                                                         |
| <span data-ttu-id="329fb-218">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-218">public int labelPosition(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="329fb-219">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-219">public boolean labelUnderline(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="329fb-220">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-220">public int labelWidth(int value, \[int mode\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="329fb-221">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-221">public int labelWidthMode(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="329fb-222">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-222">public int labelWidthValue(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="329fb-223">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="329fb-223">public boolean leave()</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="329fb-224">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-224">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="329fb-225">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-225">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="329fb-226">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-226">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="329fb-227">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-227">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="329fb-228">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-228">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="329fb-229">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-229">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="329fb-230">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-230">public boolean mandatory(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-231">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-231">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="329fb-232">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="329fb-232">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="329fb-233">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="329fb-233">public boolean modified()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="329fb-234">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-234">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="329fb-235">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-235">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="329fb-236">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-236">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="329fb-237">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-237">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="329fb-238">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-238">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="329fb-239">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-239">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="329fb-240">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-240">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="329fb-241">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-241">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="329fb-242">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="329fb-242">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="329fb-243">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-243">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="329fb-244">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-244">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="329fb-245">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-245">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="329fb-246">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="329fb-246">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="329fb-247">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="329fb-247">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="329fb-248">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-248">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="329fb-249">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-249">public str previewPartRef(\[str value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="329fb-250">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-250">public int promptrect(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="329fb-251">public FieldId referenceField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-251">public FieldId referenceField(\[FieldId value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="329fb-252">public str replacementFieldGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-252">public str replacementFieldGroup(\[str value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="329fb-253">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-253">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="329fb-254">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-254">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="329fb-255">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="329fb-255">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="329fb-256">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-256">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="329fb-257">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-257">public boolean showLabel(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-258">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-258">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="329fb-259">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-259">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="329fb-260">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="329fb-260">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="329fb-261">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-261">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="329fb-262">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="329fb-262">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="329fb-263">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-263">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="329fb-264">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-264">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="329fb-265">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-265">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="329fb-266">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-266">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="329fb-267">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-267">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="329fb-268">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-268">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="329fb-269">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-269">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="329fb-270">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-270">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="329fb-271">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-271">public boolean underline(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-272">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="329fb-272">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="329fb-273">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-273">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="329fb-274">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-274">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="329fb-275">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-275">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="329fb-276">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-276">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="329fb-277">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-277">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="329fb-278">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-278">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="329fb-279">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-279">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="329fb-280">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-280">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="329fb-281">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-281">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="329fb-282">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-282">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="329fb-283">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-283">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="329fb-284">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-284">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="329fb-285">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-285">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="329fb-286">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-286">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="329fb-287">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-287">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="329fb-288">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-288">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="329fb-289">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-289">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="329fb-290">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-290">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="329fb-291">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-291">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="329fb-292">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-292">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="329fb-293">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-293">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="329fb-294">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-294">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="329fb-295">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-295">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="329fb-296">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-296">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="329fb-297">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-297">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="329fb-298">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="329fb-298">public boolean validate()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="329fb-299">public Int64 value(\[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-299">public Int64 value(\[Int64 value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="329fb-300">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-300">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="329fb-301">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-301">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="329fb-302">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-302">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="329fb-303">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-303">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="329fb-304">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-304">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="329fb-305">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-305">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="329fb-306">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-306">public int viewEditMode(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="329fb-307">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-307">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="329fb-308">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-308">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="329fb-309">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="329fb-309">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="329fb-310">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-310">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="329fb-311">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-311">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="329fb-312">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-312">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="329fb-313">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="329fb-313">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="329fb-314">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-314">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="329fb-315">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="329fb-315">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="329fb-316">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-316">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="329fb-317">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="329fb-317">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="329fb-318">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-318">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="329fb-319">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-319">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-320">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="329fb-320">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="329fb-321">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="329fb-321">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-322">public void cut()</span><span class="sxs-lookup"><span data-stu-id="329fb-322">public void cut()</span></span>                                                                                                   | <span data-ttu-id="329fb-323">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="329fb-323">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="329fb-324">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="329fb-324">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="329fb-325">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-325">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="329fb-326">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-326">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="329fb-327">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="329fb-327">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="329fb-328">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-328">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="329fb-329">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="329fb-329">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="329fb-330">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="329fb-330">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="329fb-331">public void enter()</span><span class="sxs-lookup"><span data-stu-id="329fb-331">public void enter()</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="329fb-332">public void paste()</span><span class="sxs-lookup"><span data-stu-id="329fb-332">public void paste()</span></span>                                                                                                 | <span data-ttu-id="329fb-333">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="329fb-333">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="329fb-334">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-334">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                       |                                                                                                                                                                         |
| <span data-ttu-id="329fb-335">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="329fb-335">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="329fb-336">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-336">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="329fb-337">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-337">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="329fb-338">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-338">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="329fb-339">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="329fb-339">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="329fb-340">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="329fb-340">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="329fb-341">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="329fb-341">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="329fb-342">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-342">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="329fb-343">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="329fb-343">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="329fb-344">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-344">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="329fb-345">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="329fb-345">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="329fb-346">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-346">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="329fb-347">public void undo()</span><span class="sxs-lookup"><span data-stu-id="329fb-347">public void undo()</span></span>                                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="329fb-348">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="329fb-348">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="329fb-349">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-349">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="329fb-350">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-350">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="329fb-351">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="329fb-351">public void lookup()</span></span>                                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="329fb-352">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="329fb-352">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="329fb-353">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="329fb-353">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="329fb-354">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-354">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                           |                                                                                                                                                                         |
| <span data-ttu-id="329fb-355">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="329fb-355">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="329fb-356">public void copy()</span><span class="sxs-lookup"><span data-stu-id="329fb-356">public void copy()</span></span>                                                                                                  | <span data-ttu-id="329fb-357">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="329fb-357">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="329fb-358">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="329fb-358">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="329fb-359">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-359">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="329fb-360">public void context()</span><span class="sxs-lookup"><span data-stu-id="329fb-360">public void context()</span></span>                                                                                               | <span data-ttu-id="329fb-361">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-361">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="329fb-362">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="329fb-362">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="329fb-363">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-363">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

## <a name="method-addcontrol"></a><span data-ttu-id="329fb-364">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="329fb-364">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="329fb-365">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="329fb-365">Parameters - addControl</span></span>

<span data-ttu-id="329fb-366">controlType</span><span class="sxs-lookup"><span data-stu-id="329fb-366">controlType</span></span>  

<!-- -->

<span data-ttu-id="329fb-367">controlName</span><span class="sxs-lookup"><span data-stu-id="329fb-367">controlName</span></span>  

<!-- -->

<span data-ttu-id="329fb-368">insertAfter</span><span class="sxs-lookup"><span data-stu-id="329fb-368">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="329fb-369">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="329fb-369">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="329fb-370">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="329fb-370">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="329fb-371">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="329fb-371">Parameters - addControlEx</span></span>

<span data-ttu-id="329fb-372">controlClass</span><span class="sxs-lookup"><span data-stu-id="329fb-372">controlClass</span></span>  

<!-- -->

<span data-ttu-id="329fb-373">controlName</span><span class="sxs-lookup"><span data-stu-id="329fb-373">controlName</span></span>  

<!-- -->

<span data-ttu-id="329fb-374">insertAfter</span><span class="sxs-lookup"><span data-stu-id="329fb-374">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="329fb-375">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="329fb-375">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="329fb-376">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="329fb-376">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="329fb-377">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="329fb-377">Parameters - addDataField</span></span>

<span data-ttu-id="329fb-378">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="329fb-378">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="329fb-379">fieldId</span><span class="sxs-lookup"><span data-stu-id="329fb-379">fieldId</span></span>  

<!-- -->

<span data-ttu-id="329fb-380">insertAfter</span><span class="sxs-lookup"><span data-stu-id="329fb-380">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="329fb-381">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="329fb-381">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="329fb-382">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="329fb-382">Return Value - addDataField</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="329fb-383">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="329fb-383">Method alignControl</span></span>

<span data-ttu-id="329fb-384">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-384">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="329fb-385">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="329fb-385">Parameters - alignControl</span></span>

<span data-ttu-id="329fb-386">値</span><span class="sxs-lookup"><span data-stu-id="329fb-386">value</span></span>  
<span data-ttu-id="329fb-387">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-387">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="329fb-388">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="329fb-388">Return Value - alignControl</span></span>

<span data-ttu-id="329fb-389">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="329fb-389">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="329fb-390">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="329fb-390">Remarks - alignControl</span></span>

<span data-ttu-id="329fb-391">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-391">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="329fb-392">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="329fb-392">Method allowEdit</span></span>

<span data-ttu-id="329fb-393">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-393">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="329fb-394">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="329fb-394">Parameters - allowEdit</span></span>

<span data-ttu-id="329fb-395">値</span><span class="sxs-lookup"><span data-stu-id="329fb-395">value</span></span>  
<span data-ttu-id="329fb-396">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="329fb-396">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="329fb-397">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="329fb-397">Return Value - allowEdit</span></span>

<span data-ttu-id="329fb-398">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-398">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="329fb-399">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="329fb-399">Remarks - allowEdit</span></span>

<span data-ttu-id="329fb-400">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="329fb-400">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="329fb-401">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="329fb-401">Method allowSysSetup</span></span>

<span data-ttu-id="329fb-402">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-402">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="329fb-403">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="329fb-403">Return Value - allowSysSetup</span></span>

<span data-ttu-id="329fb-404">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-404">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="329fb-405">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="329fb-405">Method autoDeclaration</span></span>

<span data-ttu-id="329fb-406">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-406">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="329fb-407">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="329fb-407">Parameters - autoDeclaration</span></span>

<span data-ttu-id="329fb-408">値</span><span class="sxs-lookup"><span data-stu-id="329fb-408">value</span></span>  
<span data-ttu-id="329fb-409">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-409">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="329fb-410">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="329fb-410">Return Value - autoDeclaration</span></span>

<span data-ttu-id="329fb-411">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-411">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="329fb-412">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="329fb-412">Remarks - autoDeclaration</span></span>

<span data-ttu-id="329fb-413">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="329fb-413">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="329fb-414">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-414">Method backgroundColor</span></span>

<span data-ttu-id="329fb-415">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-415">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="329fb-416">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-416">Parameters - backgroundColor</span></span>

<span data-ttu-id="329fb-417">値</span><span class="sxs-lookup"><span data-stu-id="329fb-417">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="329fb-418">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-418">Return Value - backgroundColor</span></span>

<span data-ttu-id="329fb-419">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="329fb-419">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="329fb-420">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-420">Remarks - backgroundColor</span></span>

<span data-ttu-id="329fb-421">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="329fb-421">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="329fb-422">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="329fb-422">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="329fb-423">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="329fb-423">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="329fb-424">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="329fb-424">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="329fb-425">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="329fb-425">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="329fb-426">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="329fb-426">The maximum value for a single byte is 255.</span></span>

## <a name="method-backgroundimage"></a><span data-ttu-id="329fb-427">メソッド backgroundImage</span><span class="sxs-lookup"><span data-stu-id="329fb-427">Method backgroundImage</span></span>

```xpp
public Image backgroundImage([Image image], [int drawMode])
```

### <a name="parameters---backgroundimage"></a><span data-ttu-id="329fb-428">パラメーター - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="329fb-428">Parameters - backgroundImage</span></span>

<span data-ttu-id="329fb-429">画像</span><span class="sxs-lookup"><span data-stu-id="329fb-429">image</span></span>  

<!-- -->

<span data-ttu-id="329fb-430">drawMode</span><span class="sxs-lookup"><span data-stu-id="329fb-430">drawMode</span></span>  

### <a name="return-value---backgroundimage"></a><span data-ttu-id="329fb-431">戻り値 - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="329fb-431">Return Value - backgroundImage</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="329fb-432">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="329fb-432">Method backStyle</span></span>

<span data-ttu-id="329fb-433">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-433">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="329fb-434">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="329fb-434">Parameters - backStyle</span></span>

<span data-ttu-id="329fb-435">値</span><span class="sxs-lookup"><span data-stu-id="329fb-435">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="329fb-436">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="329fb-436">Return Value - backStyle</span></span>

<span data-ttu-id="329fb-437">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="329fb-437">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="329fb-438">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="329fb-438">Method beginDrag</span></span>

<span data-ttu-id="329fb-439">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-439">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="329fb-440">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="329fb-440">Parameters - beginDrag</span></span>

<span data-ttu-id="329fb-441">x</span><span class="sxs-lookup"><span data-stu-id="329fb-441">x</span></span>  
<span data-ttu-id="329fb-442">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-442">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="329fb-443">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="329fb-443">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="329fb-444">y</span><span class="sxs-lookup"><span data-stu-id="329fb-444">y</span></span>  
<span data-ttu-id="329fb-445">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-445">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="329fb-446">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="329fb-446">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="329fb-447">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="329fb-447">Return Value - beginDrag</span></span>

<span data-ttu-id="329fb-448">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="329fb-448">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="329fb-449">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="329fb-449">Remarks - beginDrag</span></span>

<span data-ttu-id="329fb-450">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="329fb-450">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="329fb-451">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="329fb-451">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="329fb-452">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="329fb-452">Method bold</span></span>

<span data-ttu-id="329fb-453">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-453">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="329fb-454">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="329fb-454">Parameters - bold</span></span>

<span data-ttu-id="329fb-455">値</span><span class="sxs-lookup"><span data-stu-id="329fb-455">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="329fb-456">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="329fb-456">Return Value - bold</span></span>

<span data-ttu-id="329fb-457">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-457">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="329fb-458">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="329fb-458">Remarks - bold</span></span>

<span data-ttu-id="329fb-459">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="329fb-459">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="329fb-460">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="329fb-460">0 Use the default font weight.</span></span>
-   <span data-ttu-id="329fb-461">1 シン。</span><span class="sxs-lookup"><span data-stu-id="329fb-461">1 Thin.</span></span>
-   <span data-ttu-id="329fb-462">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="329fb-462">2 Extra-light.</span></span>
-   <span data-ttu-id="329fb-463">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="329fb-463">3 Light.</span></span>
-   <span data-ttu-id="329fb-464">4 標準。</span><span class="sxs-lookup"><span data-stu-id="329fb-464">4 Normal.</span></span>
-   <span data-ttu-id="329fb-465">5 中。</span><span class="sxs-lookup"><span data-stu-id="329fb-465">5 Medium.</span></span>
-   <span data-ttu-id="329fb-466">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="329fb-466">6 Semibold.</span></span>
-   <span data-ttu-id="329fb-467">7 太字。</span><span class="sxs-lookup"><span data-stu-id="329fb-467">7 Bold.</span></span>
-   <span data-ttu-id="329fb-468">8 極太。</span><span class="sxs-lookup"><span data-stu-id="329fb-468">8 Extra-bold.</span></span>
-   <span data-ttu-id="329fb-469">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="329fb-469">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="329fb-470">メソッド border</span><span class="sxs-lookup"><span data-stu-id="329fb-470">Method border</span></span>

<span data-ttu-id="329fb-471">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-471">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="329fb-472">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="329fb-472">Parameters - border</span></span>

<span data-ttu-id="329fb-473">値</span><span class="sxs-lookup"><span data-stu-id="329fb-473">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="329fb-474">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="329fb-474">Return Value - border</span></span>

<span data-ttu-id="329fb-475">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="329fb-475">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="329fb-476">備考 - border</span><span class="sxs-lookup"><span data-stu-id="329fb-476">Remarks - border</span></span>

<span data-ttu-id="329fb-477">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="329fb-477">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="329fb-478">先頭値</span><span class="sxs-lookup"><span data-stu-id="329fb-478">Value</span></span> | <span data-ttu-id="329fb-479">説明</span><span class="sxs-lookup"><span data-stu-id="329fb-479">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="329fb-480">0</span><span class="sxs-lookup"><span data-stu-id="329fb-480">0</span></span>     | <span data-ttu-id="329fb-481">自動</span><span class="sxs-lookup"><span data-stu-id="329fb-481">Auto</span></span>        |
| <span data-ttu-id="329fb-482">1</span><span class="sxs-lookup"><span data-stu-id="329fb-482">1</span></span>     | <span data-ttu-id="329fb-483">3D</span><span class="sxs-lookup"><span data-stu-id="329fb-483">3D</span></span>          |
| <span data-ttu-id="329fb-484">2</span><span class="sxs-lookup"><span data-stu-id="329fb-484">2</span></span>     | <span data-ttu-id="329fb-485">単一明細行</span><span class="sxs-lookup"><span data-stu-id="329fb-485">Single line</span></span> |
| <span data-ttu-id="329fb-486">3</span><span class="sxs-lookup"><span data-stu-id="329fb-486">3</span></span>     | <span data-ttu-id="329fb-487">均一</span><span class="sxs-lookup"><span data-stu-id="329fb-487">Flat</span></span>        |
| <span data-ttu-id="329fb-488">4</span><span class="sxs-lookup"><span data-stu-id="329fb-488">4</span></span>     | <span data-ttu-id="329fb-489">None</span><span class="sxs-lookup"><span data-stu-id="329fb-489">None</span></span>        |

## <a name="method-calccontrolsize"></a><span data-ttu-id="329fb-490">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="329fb-490">Method calcControlSize</span></span>

<span data-ttu-id="329fb-491">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-491">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="329fb-492">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="329fb-492">Parameters - calcControlSize</span></span>

<span data-ttu-id="329fb-493">chars</span><span class="sxs-lookup"><span data-stu-id="329fb-493">chars</span></span>  
<span data-ttu-id="329fb-494">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="329fb-494">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="329fb-495">明細行</span><span class="sxs-lookup"><span data-stu-id="329fb-495">lines</span></span>  
<span data-ttu-id="329fb-496">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="329fb-496">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="329fb-497">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="329fb-497">Return Value - calcControlSize</span></span>

<span data-ttu-id="329fb-498">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="329fb-498">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="329fb-499">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="329fb-499">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="329fb-500">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="329fb-500">Parameters - canAddDataField</span></span>

<span data-ttu-id="329fb-501">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="329fb-501">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="329fb-502">fieldId</span><span class="sxs-lookup"><span data-stu-id="329fb-502">fieldId</span></span>  

<!-- -->

<span data-ttu-id="329fb-503">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="329fb-503">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="329fb-504">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="329fb-504">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="329fb-505">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="329fb-505">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="329fb-506">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="329fb-506">Parameters - canContain</span></span>

<span data-ttu-id="329fb-507">control</span><span class="sxs-lookup"><span data-stu-id="329fb-507">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="329fb-508">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="329fb-508">Return Value - canContain</span></span>

## <a name="method-characterset"></a><span data-ttu-id="329fb-509">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="329fb-509">Method characterSet</span></span>

<span data-ttu-id="329fb-510">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-510">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="329fb-511">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="329fb-511">Parameters - characterSet</span></span>

<span data-ttu-id="329fb-512">値</span><span class="sxs-lookup"><span data-stu-id="329fb-512">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="329fb-513">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="329fb-513">Return Value - characterSet</span></span>

<span data-ttu-id="329fb-514">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-514">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="329fb-515">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="329fb-515">Remarks - characterSet</span></span>

<span data-ttu-id="329fb-516">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-516">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="329fb-517">先頭値</span><span class="sxs-lookup"><span data-stu-id="329fb-517">Value</span></span> | <span data-ttu-id="329fb-518">説明</span><span class="sxs-lookup"><span data-stu-id="329fb-518">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="329fb-519">0</span><span class="sxs-lookup"><span data-stu-id="329fb-519">0</span></span>     | <span data-ttu-id="329fb-520">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-520">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="329fb-521">1</span><span class="sxs-lookup"><span data-stu-id="329fb-521">1</span></span>     | <span data-ttu-id="329fb-522">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-522">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="329fb-523">2</span><span class="sxs-lookup"><span data-stu-id="329fb-523">2</span></span>     | <span data-ttu-id="329fb-524">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-524">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="329fb-525">77</span><span class="sxs-lookup"><span data-stu-id="329fb-525">77</span></span>    | <span data-ttu-id="329fb-526">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-526">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="329fb-527">128</span><span class="sxs-lookup"><span data-stu-id="329fb-527">128</span></span>   | <span data-ttu-id="329fb-528">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-528">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="329fb-529">129</span><span class="sxs-lookup"><span data-stu-id="329fb-529">129</span></span>   | <span data-ttu-id="329fb-530">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-530">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="329fb-531">134</span><span class="sxs-lookup"><span data-stu-id="329fb-531">134</span></span>   | <span data-ttu-id="329fb-532">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-532">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="329fb-533">136</span><span class="sxs-lookup"><span data-stu-id="329fb-533">136</span></span>   | <span data-ttu-id="329fb-534">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-534">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="329fb-535">161</span><span class="sxs-lookup"><span data-stu-id="329fb-535">161</span></span>   | <span data-ttu-id="329fb-536">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-536">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="329fb-537">162</span><span class="sxs-lookup"><span data-stu-id="329fb-537">162</span></span>   | <span data-ttu-id="329fb-538">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-538">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="329fb-539">163</span><span class="sxs-lookup"><span data-stu-id="329fb-539">163</span></span>   | <span data-ttu-id="329fb-540">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-540">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="329fb-541">186</span><span class="sxs-lookup"><span data-stu-id="329fb-541">186</span></span>   | <span data-ttu-id="329fb-542">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-542">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="329fb-543">204</span><span class="sxs-lookup"><span data-stu-id="329fb-543">204</span></span>   | <span data-ttu-id="329fb-544">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-544">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="329fb-545">238</span><span class="sxs-lookup"><span data-stu-id="329fb-545">238</span></span>   | <span data-ttu-id="329fb-546">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-546">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="329fb-547">255</span><span class="sxs-lookup"><span data-stu-id="329fb-547">255</span></span>   | <span data-ttu-id="329fb-548">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-548">OEM\_CHARSET</span></span>         |

<span data-ttu-id="329fb-549">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="329fb-549">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="329fb-550">金額</span><span class="sxs-lookup"><span data-stu-id="329fb-550">Value</span></span> | <span data-ttu-id="329fb-551">説明</span><span class="sxs-lookup"><span data-stu-id="329fb-551">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="329fb-552">130</span><span class="sxs-lookup"><span data-stu-id="329fb-552">130</span></span>   | <span data-ttu-id="329fb-553">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-553">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="329fb-554">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="329fb-554">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="329fb-555">先頭値</span><span class="sxs-lookup"><span data-stu-id="329fb-555">Value</span></span> | <span data-ttu-id="329fb-556">説明</span><span class="sxs-lookup"><span data-stu-id="329fb-556">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="329fb-557">177</span><span class="sxs-lookup"><span data-stu-id="329fb-557">177</span></span>   | <span data-ttu-id="329fb-558">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-558">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="329fb-559">178</span><span class="sxs-lookup"><span data-stu-id="329fb-559">178</span></span>   | <span data-ttu-id="329fb-560">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-560">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="329fb-561">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="329fb-561">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="329fb-562">先頭値</span><span class="sxs-lookup"><span data-stu-id="329fb-562">Value</span></span> | <span data-ttu-id="329fb-563">説明</span><span class="sxs-lookup"><span data-stu-id="329fb-563">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="329fb-564">222</span><span class="sxs-lookup"><span data-stu-id="329fb-564">222</span></span>   | <span data-ttu-id="329fb-565">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="329fb-565">THAI\_CHARSET</span></span> |

<span data-ttu-id="329fb-566">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-566">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="329fb-567">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-567">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="329fb-568">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="329fb-568">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="329fb-569">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="329fb-569">Method colorScheme</span></span>

<span data-ttu-id="329fb-570">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-570">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="329fb-571">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="329fb-571">Parameters - colorScheme</span></span>

<span data-ttu-id="329fb-572">値</span><span class="sxs-lookup"><span data-stu-id="329fb-572">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="329fb-573">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="329fb-573">Return Value - colorScheme</span></span>

<span data-ttu-id="329fb-574">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="329fb-574">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="329fb-575">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="329fb-575">Remarks - colorScheme</span></span>

<span data-ttu-id="329fb-576">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-576">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="329fb-577">先頭値</span><span class="sxs-lookup"><span data-stu-id="329fb-577">Value</span></span> | <span data-ttu-id="329fb-578">スタイル</span><span class="sxs-lookup"><span data-stu-id="329fb-578">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="329fb-579">0</span><span class="sxs-lookup"><span data-stu-id="329fb-579">0</span></span>     | <span data-ttu-id="329fb-580">既定</span><span class="sxs-lookup"><span data-stu-id="329fb-580">Default</span></span>               |
| <span data-ttu-id="329fb-581">1</span><span class="sxs-lookup"><span data-stu-id="329fb-581">1</span></span>     | <span data-ttu-id="329fb-582">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="329fb-582">The Windows palette</span></span>   |
| <span data-ttu-id="329fb-583">2</span><span class="sxs-lookup"><span data-stu-id="329fb-583">2</span></span>     | <span data-ttu-id="329fb-584">真の配色</span><span class="sxs-lookup"><span data-stu-id="329fb-584">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="329fb-585">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="329fb-585">Method configurationKey</span></span>

<span data-ttu-id="329fb-586">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-586">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="329fb-587">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="329fb-587">Parameters - configurationKey</span></span>

<span data-ttu-id="329fb-588">値</span><span class="sxs-lookup"><span data-stu-id="329fb-588">value</span></span>  
<span data-ttu-id="329fb-589">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-589">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="329fb-590">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="329fb-590">Return Value - configurationKey</span></span>

<span data-ttu-id="329fb-591">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="329fb-591">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="329fb-592">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="329fb-592">Remarks - configurationKey</span></span>

<span data-ttu-id="329fb-593">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-593">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="329fb-594">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="329fb-594">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="329fb-595">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="329fb-595">Method configurationKeyEx</span></span>

<span data-ttu-id="329fb-596">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-596">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="329fb-597">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="329fb-597">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="329fb-598">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="329fb-598">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="329fb-599">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="329fb-599">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="329fb-600">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="329fb-600">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="329fb-601">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="329fb-601">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="329fb-602">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="329fb-602">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="329fb-603">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="329fb-603">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="329fb-604">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="329fb-604">Parameters - contains</span></span>

<span data-ttu-id="329fb-605">control</span><span class="sxs-lookup"><span data-stu-id="329fb-605">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="329fb-606">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="329fb-606">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="329fb-607">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="329fb-607">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="329fb-608">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="329fb-608">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="329fb-609">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="329fb-609">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="329fb-610">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="329fb-610">Parameters - controlNum</span></span>

<span data-ttu-id="329fb-611">controlNo</span><span class="sxs-lookup"><span data-stu-id="329fb-611">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="329fb-612">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="329fb-612">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="329fb-613">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="329fb-613">Method countryRegionCodes</span></span>

<span data-ttu-id="329fb-614">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-614">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="329fb-615">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="329fb-615">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="329fb-616">値</span><span class="sxs-lookup"><span data-stu-id="329fb-616">value</span></span>  
<span data-ttu-id="329fb-617">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-617">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="329fb-618">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="329fb-618">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="329fb-619">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="329fb-619">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="329fb-620">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="329fb-620">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="329fb-621">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="329fb-621">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="329fb-622">値</span><span class="sxs-lookup"><span data-stu-id="329fb-622">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="329fb-623">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="329fb-623">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="329fb-624">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="329fb-624">Method dataRelationPath</span></span>

<span data-ttu-id="329fb-625">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-625">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="329fb-626">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="329fb-626">Parameters - dataRelationPath</span></span>

<span data-ttu-id="329fb-627">値</span><span class="sxs-lookup"><span data-stu-id="329fb-627">value</span></span>  
<span data-ttu-id="329fb-628">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-628">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="329fb-629">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="329fb-629">Return Value - dataRelationPath</span></span>

<span data-ttu-id="329fb-630">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="329fb-630">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="329fb-631">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="329fb-631">Remarks - dataRelationPath</span></span>

<span data-ttu-id="329fb-632">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="329fb-632">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="329fb-633">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="329fb-633">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="329fb-634">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="329fb-634">Method dataSource</span></span>

<span data-ttu-id="329fb-635">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-635">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="329fb-636">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="329fb-636">Parameters - dataSource</span></span>

<span data-ttu-id="329fb-637">値</span><span class="sxs-lookup"><span data-stu-id="329fb-637">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="329fb-638">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="329fb-638">Return Value - dataSource</span></span>

<span data-ttu-id="329fb-639">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="329fb-639">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="329fb-640">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="329fb-640">Method displayTarget</span></span>

<span data-ttu-id="329fb-641">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-641">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="329fb-642">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="329fb-642">Parameters - displayTarget</span></span>

<span data-ttu-id="329fb-643">値</span><span class="sxs-lookup"><span data-stu-id="329fb-643">value</span></span>  
<span data-ttu-id="329fb-644">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-644">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="329fb-645">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="329fb-645">Return Value - displayTarget</span></span>

<span data-ttu-id="329fb-646">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="329fb-646">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="329fb-647">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="329fb-647">Method dragDrop</span></span>

<span data-ttu-id="329fb-648">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-648">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="329fb-649">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="329fb-649">Parameters - dragDrop</span></span>

<span data-ttu-id="329fb-650">値</span><span class="sxs-lookup"><span data-stu-id="329fb-650">value</span></span>  
<span data-ttu-id="329fb-651">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-651">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="329fb-652">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="329fb-652">Return Value - dragDrop</span></span>

<span data-ttu-id="329fb-653">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="329fb-653">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="329fb-654">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="329fb-654">Remarks - dragDrop</span></span>

<span data-ttu-id="329fb-655">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-655">Use the dragLeave, the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="329fb-656">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="329fb-656">Method dragOver</span></span>

<span data-ttu-id="329fb-657">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-657">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="329fb-658">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="329fb-658">Parameters - dragOver</span></span>

<span data-ttu-id="329fb-659">dragSource</span><span class="sxs-lookup"><span data-stu-id="329fb-659">dragSource</span></span>  
<span data-ttu-id="329fb-660">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-660">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-661">dragMode</span><span class="sxs-lookup"><span data-stu-id="329fb-661">dragMode</span></span>  
<span data-ttu-id="329fb-662">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-662">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-663">x</span><span class="sxs-lookup"><span data-stu-id="329fb-663">x</span></span>  
<span data-ttu-id="329fb-664">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-664">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-665">y</span><span class="sxs-lookup"><span data-stu-id="329fb-665">y</span></span>  
<span data-ttu-id="329fb-666">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-666">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="329fb-667">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="329fb-667">Return Value - dragOver</span></span>

<span data-ttu-id="329fb-668">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="329fb-668">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="329fb-669">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="329fb-669">Method dragOverEx</span></span>

<span data-ttu-id="329fb-670">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-670">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="329fb-671">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="329fb-671">Parameters - dragOverEx</span></span>

<span data-ttu-id="329fb-672">dragSource</span><span class="sxs-lookup"><span data-stu-id="329fb-672">dragSource</span></span>  
<span data-ttu-id="329fb-673">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-673">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-674">dragMode</span><span class="sxs-lookup"><span data-stu-id="329fb-674">dragMode</span></span>  
<span data-ttu-id="329fb-675">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-675">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-676">x</span><span class="sxs-lookup"><span data-stu-id="329fb-676">x</span></span>  
<span data-ttu-id="329fb-677">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-677">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-678">y</span><span class="sxs-lookup"><span data-stu-id="329fb-678">y</span></span>  
<span data-ttu-id="329fb-679">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-679">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="329fb-680">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="329fb-680">Return Value - dragOverEx</span></span>

<span data-ttu-id="329fb-681">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="329fb-681">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="329fb-682">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="329fb-682">Method dragText</span></span>

<span data-ttu-id="329fb-683">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-683">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="329fb-684">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="329fb-684">Return Value - dragText</span></span>

<span data-ttu-id="329fb-685">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="329fb-685">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enablechilds"></a><span data-ttu-id="329fb-686">メソッド enableChilds</span><span class="sxs-lookup"><span data-stu-id="329fb-686">Method enableChilds</span></span>

```xpp
public boolean enableChilds([boolean enable])
```

### <a name="parameters---enablechilds"></a><span data-ttu-id="329fb-687">パラメーター - enableChilds</span><span class="sxs-lookup"><span data-stu-id="329fb-687">Parameters - enableChilds</span></span>

<span data-ttu-id="329fb-688">enable</span><span class="sxs-lookup"><span data-stu-id="329fb-688">enable</span></span>  

### <a name="return-value---enablechilds"></a><span data-ttu-id="329fb-689">戻り値 - enableChilds</span><span class="sxs-lookup"><span data-stu-id="329fb-689">Return Value - enableChilds</span></span>

## <a name="method-enabled"></a><span data-ttu-id="329fb-690">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="329fb-690">Method enabled</span></span>

<span data-ttu-id="329fb-691">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-691">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="329fb-692">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="329fb-692">Parameters - enabled</span></span>

<span data-ttu-id="329fb-693">値</span><span class="sxs-lookup"><span data-stu-id="329fb-693">value</span></span>  
<span data-ttu-id="329fb-694">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-694">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="329fb-695">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="329fb-695">Return Value - enabled</span></span>

<span data-ttu-id="329fb-696">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-696">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="329fb-697">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="329fb-697">Remarks - enabled</span></span>

<span data-ttu-id="329fb-698">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="329fb-698">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="329fb-699">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="329fb-699">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="329fb-700">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="329fb-700">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-expand"></a><span data-ttu-id="329fb-701">メソッド expand</span><span class="sxs-lookup"><span data-stu-id="329fb-701">Method expand</span></span>

```xpp
public boolean expand([boolean expand])
```

### <a name="parameters---expand"></a><span data-ttu-id="329fb-702">パラメーター - expand</span><span class="sxs-lookup"><span data-stu-id="329fb-702">Parameters - expand</span></span>

<span data-ttu-id="329fb-703">expand</span><span class="sxs-lookup"><span data-stu-id="329fb-703">expand</span></span>  

### <a name="return-value---expand"></a><span data-ttu-id="329fb-704">戻り値 - expand</span><span class="sxs-lookup"><span data-stu-id="329fb-704">Return Value - expand</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="329fb-705">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="329fb-705">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="329fb-706">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="329fb-706">Parameters - extendedDataType</span></span>

<span data-ttu-id="329fb-707">値</span><span class="sxs-lookup"><span data-stu-id="329fb-707">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="329fb-708">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="329fb-708">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="329fb-709">メソッド font</span><span class="sxs-lookup"><span data-stu-id="329fb-709">Method font</span></span>

<span data-ttu-id="329fb-710">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-710">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="329fb-711">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="329fb-711">Parameters - font</span></span>

<span data-ttu-id="329fb-712">値</span><span class="sxs-lookup"><span data-stu-id="329fb-712">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="329fb-713">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="329fb-713">Return Value - font</span></span>

<span data-ttu-id="329fb-714">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="329fb-714">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="329fb-715">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="329fb-715">Method fontSize</span></span>

<span data-ttu-id="329fb-716">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-716">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="329fb-717">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="329fb-717">Parameters - fontSize</span></span>

<span data-ttu-id="329fb-718">値</span><span class="sxs-lookup"><span data-stu-id="329fb-718">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="329fb-719">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="329fb-719">Return Value - fontSize</span></span>

<span data-ttu-id="329fb-720">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="329fb-720">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="329fb-721">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-721">Method foregroundColor</span></span>

<span data-ttu-id="329fb-722">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-722">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="329fb-723">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-723">Parameters - foregroundColor</span></span>

<span data-ttu-id="329fb-724">値</span><span class="sxs-lookup"><span data-stu-id="329fb-724">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="329fb-725">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-725">Return Value - foregroundColor</span></span>

<span data-ttu-id="329fb-726">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="329fb-726">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="329fb-727">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-727">Remarks - foregroundColor</span></span>

<span data-ttu-id="329fb-728">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="329fb-728">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="329fb-729">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="329fb-729">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="329fb-730">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="329fb-730">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="329fb-731">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="329fb-731">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="329fb-732">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="329fb-732">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="329fb-733">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="329fb-733">The maximum value for a single byte is 255.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="329fb-734">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="329fb-734">Method hasChanged</span></span>

<span data-ttu-id="329fb-735">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-735">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="329fb-736">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="329fb-736">Parameters - hasChanged</span></span>

<span data-ttu-id="329fb-737">val</span><span class="sxs-lookup"><span data-stu-id="329fb-737">val</span></span>  
<span data-ttu-id="329fb-738">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-738">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="329fb-739">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="329fb-739">Return Value - hasChanged</span></span>

<span data-ttu-id="329fb-740">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-740">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="329fb-741">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="329fb-741">Method hasUserSetting</span></span>

<span data-ttu-id="329fb-742">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-742">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="329fb-743">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="329fb-743">Return Value - hasUserSetting</span></span>

<span data-ttu-id="329fb-744">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-744">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="329fb-745">メソッド height</span><span class="sxs-lookup"><span data-stu-id="329fb-745">Method height</span></span>

<span data-ttu-id="329fb-746">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-746">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="329fb-747">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="329fb-747">Parameters - height</span></span>

<span data-ttu-id="329fb-748">値</span><span class="sxs-lookup"><span data-stu-id="329fb-748">value</span></span>  
<span data-ttu-id="329fb-749">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-749">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="329fb-750">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-750">mode</span></span>  
<span data-ttu-id="329fb-751">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-751">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="329fb-752">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="329fb-752">Return Value - height</span></span>

<span data-ttu-id="329fb-753">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="329fb-753">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="329fb-754">備考 - height</span><span class="sxs-lookup"><span data-stu-id="329fb-754">Remarks - height</span></span>

<span data-ttu-id="329fb-755">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-755">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="329fb-756">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="329fb-756">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="329fb-757">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-757">Mode</span></span>            | <span data-ttu-id="329fb-758">高さの計算</span><span class="sxs-lookup"><span data-stu-id="329fb-758">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="329fb-759">-1 正確</span><span class="sxs-lookup"><span data-stu-id="329fb-759">-1 Exact</span></span>        | <span data-ttu-id="329fb-760">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-760">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="329fb-761">0 自動</span><span class="sxs-lookup"><span data-stu-id="329fb-761">0 Auto</span></span>          | <span data-ttu-id="329fb-762">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-762">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="329fb-763">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="329fb-763">1 Column height</span></span> | <span data-ttu-id="329fb-764">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="329fb-764">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="329fb-765">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="329fb-765">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="329fb-766">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="329fb-766">Method heightMode</span></span>

<span data-ttu-id="329fb-767">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-767">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="329fb-768">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="329fb-768">Parameters - heightMode</span></span>

<span data-ttu-id="329fb-769">値</span><span class="sxs-lookup"><span data-stu-id="329fb-769">value</span></span>  
<span data-ttu-id="329fb-770">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-770">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="329fb-771">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="329fb-771">Return Value - heightMode</span></span>

<span data-ttu-id="329fb-772">計算モード。</span><span class="sxs-lookup"><span data-stu-id="329fb-772">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="329fb-773">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="329fb-773">Remarks - heightMode</span></span>

<span data-ttu-id="329fb-774">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="329fb-774">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="329fb-775">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-775">Mode</span></span>          | <span data-ttu-id="329fb-776">高さの計算</span><span class="sxs-lookup"><span data-stu-id="329fb-776">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="329fb-777">正確</span><span class="sxs-lookup"><span data-stu-id="329fb-777">Exact</span></span>         | <span data-ttu-id="329fb-778">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-778">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="329fb-779">自動</span><span class="sxs-lookup"><span data-stu-id="329fb-779">Auto</span></span>          | <span data-ttu-id="329fb-780">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-780">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="329fb-781">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="329fb-781">Column height</span></span> | <span data-ttu-id="329fb-782">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="329fb-782">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="329fb-783">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="329fb-783">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="329fb-784">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="329fb-784">Method heightValue</span></span>

<span data-ttu-id="329fb-785">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-785">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="329fb-786">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="329fb-786">Parameters - heightValue</span></span>

<span data-ttu-id="329fb-787">値</span><span class="sxs-lookup"><span data-stu-id="329fb-787">value</span></span>  
<span data-ttu-id="329fb-788">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-788">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="329fb-789">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="329fb-789">Return Value - heightValue</span></span>

<span data-ttu-id="329fb-790">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="329fb-790">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="329fb-791">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="329fb-791">Remarks - heightValue</span></span>

<span data-ttu-id="329fb-792">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="329fb-792">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="329fb-793">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="329fb-793">Method helpField</span></span>

<span data-ttu-id="329fb-794">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-794">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="329fb-795">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="329fb-795">Return Value - helpField</span></span>

<span data-ttu-id="329fb-796">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="329fb-796">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="329fb-797">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="329fb-797">Remarks - helpField</span></span>

<span data-ttu-id="329fb-798">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="329fb-798">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="329fb-799">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="329fb-799">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="329fb-800">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="329fb-800">Method helpText</span></span>

<span data-ttu-id="329fb-801">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-801">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="329fb-802">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="329fb-802">Parameters - helpText</span></span>

<span data-ttu-id="329fb-803">値</span><span class="sxs-lookup"><span data-stu-id="329fb-803">value</span></span>  
<span data-ttu-id="329fb-804">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="329fb-804">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="329fb-805">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="329fb-805">Return Value - helpText</span></span>

<span data-ttu-id="329fb-806">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="329fb-806">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="329fb-807">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="329fb-807">Remarks - helpText</span></span>

<span data-ttu-id="329fb-808">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-808">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="329fb-809">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="329fb-809">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="329fb-810">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="329fb-810">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="329fb-811">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="329fb-811">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="329fb-812">値</span><span class="sxs-lookup"><span data-stu-id="329fb-812">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="329fb-813">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="329fb-813">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="329fb-814">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="329fb-814">Method hierarchyParent</span></span>

<span data-ttu-id="329fb-815">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-815">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="329fb-816">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="329fb-816">Parameters - hierarchyParent</span></span>

<span data-ttu-id="329fb-817">値</span><span class="sxs-lookup"><span data-stu-id="329fb-817">value</span></span>  
<span data-ttu-id="329fb-818">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="329fb-818">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="329fb-819">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="329fb-819">Return Value - hierarchyParent</span></span>

<span data-ttu-id="329fb-820">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="329fb-820">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="329fb-821">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="329fb-821">Method hWnd</span></span>

<span data-ttu-id="329fb-822">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-822">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="329fb-823">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="329fb-823">Return Value - hWnd</span></span>

<span data-ttu-id="329fb-824">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="329fb-824">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="329fb-825">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="329fb-825">Remarks - hWnd</span></span>

<span data-ttu-id="329fb-826">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="329fb-826">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="329fb-827">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="329fb-827">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="329fb-828">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="329fb-828">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="329fb-829">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="329fb-829">Method isDisplayed</span></span>

<span data-ttu-id="329fb-830">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-830">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="329fb-831">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="329fb-831">Return Value - isDisplayed</span></span>

<span data-ttu-id="329fb-832">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="329fb-832">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="329fb-833">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="329fb-833">Remarks - isDisplayed</span></span>

<span data-ttu-id="329fb-834">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="329fb-834">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="329fb-835">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="329fb-835">Method isRestricted</span></span>

<span data-ttu-id="329fb-836">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-836">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="329fb-837">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="329fb-837">Return Value - isRestricted</span></span>

<span data-ttu-id="329fb-838">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="329fb-838">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="329fb-839">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="329fb-839">Method isUserSetupEnabled</span></span>

<span data-ttu-id="329fb-840">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-840">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="329fb-841">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="329fb-841">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="329fb-842">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="329fb-842">neededSetupRights</span></span>  
<span data-ttu-id="329fb-843">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="329fb-843">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="329fb-844">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="329fb-844">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="329fb-845">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-845">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="329fb-846">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="329fb-846">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="329fb-847">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="329fb-847">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329fb-848">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="329fb-848">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="329fb-849">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="329fb-849">No changes can be made to the control.</span></span> <span data-ttu-id="329fb-850">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-850">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="329fb-851">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="329fb-851">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="329fb-852">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="329fb-852">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="329fb-853">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="329fb-853">The user cannot move the control.</span></span>   |
| <span data-ttu-id="329fb-854">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="329fb-854">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="329fb-855">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="329fb-855">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="329fb-856">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="329fb-856">The user can also move the control.</span></span> |

<span data-ttu-id="329fb-857">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="329fb-857">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="329fb-858">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="329fb-858">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="329fb-859">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="329fb-859">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="329fb-860">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="329fb-860">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="329fb-861">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="329fb-861">Parameters - italic</span></span>

<span data-ttu-id="329fb-862">値</span><span class="sxs-lookup"><span data-stu-id="329fb-862">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="329fb-863">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="329fb-863">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="329fb-864">メソッド label</span><span class="sxs-lookup"><span data-stu-id="329fb-864">Method label</span></span>

<span data-ttu-id="329fb-865">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-865">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="329fb-866">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="329fb-866">Parameters - label</span></span>

<span data-ttu-id="329fb-867">値</span><span class="sxs-lookup"><span data-stu-id="329fb-867">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="329fb-868">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="329fb-868">Return Value - label</span></span>

<span data-ttu-id="329fb-869">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="329fb-869">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="329fb-870">備考 - label</span><span class="sxs-lookup"><span data-stu-id="329fb-870">Remarks - label</span></span>

<span data-ttu-id="329fb-871">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-871">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="329fb-872">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="329fb-872">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="329fb-873">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="329fb-873">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="329fb-874">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="329fb-874">Parameters - labelAlignment</span></span>

<span data-ttu-id="329fb-875">値</span><span class="sxs-lookup"><span data-stu-id="329fb-875">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="329fb-876">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="329fb-876">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="329fb-877">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="329fb-877">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="329fb-878">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="329fb-878">Parameters - labelBold</span></span>

<span data-ttu-id="329fb-879">値</span><span class="sxs-lookup"><span data-stu-id="329fb-879">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="329fb-880">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="329fb-880">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="329fb-881">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="329fb-881">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="329fb-882">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="329fb-882">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="329fb-883">値</span><span class="sxs-lookup"><span data-stu-id="329fb-883">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="329fb-884">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="329fb-884">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="329fb-885">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="329fb-885">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="329fb-886">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="329fb-886">Parameters - labelFont</span></span>

<span data-ttu-id="329fb-887">値</span><span class="sxs-lookup"><span data-stu-id="329fb-887">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="329fb-888">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="329fb-888">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="329fb-889">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="329fb-889">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="329fb-890">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="329fb-890">Parameters - labelFontSize</span></span>

<span data-ttu-id="329fb-891">値</span><span class="sxs-lookup"><span data-stu-id="329fb-891">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="329fb-892">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="329fb-892">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="329fb-893">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-893">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="329fb-894">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-894">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="329fb-895">値</span><span class="sxs-lookup"><span data-stu-id="329fb-895">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="329fb-896">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="329fb-896">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="329fb-897">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="329fb-897">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="329fb-898">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="329fb-898">Parameters - labelGuide</span></span>

<span data-ttu-id="329fb-899">値</span><span class="sxs-lookup"><span data-stu-id="329fb-899">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="329fb-900">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="329fb-900">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="329fb-901">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="329fb-901">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="329fb-902">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="329fb-902">Parameters - labelHeight</span></span>

<span data-ttu-id="329fb-903">値</span><span class="sxs-lookup"><span data-stu-id="329fb-903">value</span></span>  

<!-- -->

<span data-ttu-id="329fb-904">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-904">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="329fb-905">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="329fb-905">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="329fb-906">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="329fb-906">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="329fb-907">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="329fb-907">Parameters - labelHeightMode</span></span>

<span data-ttu-id="329fb-908">値</span><span class="sxs-lookup"><span data-stu-id="329fb-908">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="329fb-909">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="329fb-909">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="329fb-910">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="329fb-910">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="329fb-911">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="329fb-911">Parameters - labelHeightValue</span></span>

<span data-ttu-id="329fb-912">値</span><span class="sxs-lookup"><span data-stu-id="329fb-912">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="329fb-913">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="329fb-913">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="329fb-914">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="329fb-914">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="329fb-915">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="329fb-915">Parameters - labelItalic</span></span>

<span data-ttu-id="329fb-916">値</span><span class="sxs-lookup"><span data-stu-id="329fb-916">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="329fb-917">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="329fb-917">Return Value - labelItalic</span></span>

## <a name="method-labelmousedblclick"></a><span data-ttu-id="329fb-918">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="329fb-918">Method labelMouseDblClick</span></span>

```xpp
public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedblclick"></a><span data-ttu-id="329fb-919">パラメーター - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="329fb-919">Parameters - labelMouseDblClick</span></span>

<span data-ttu-id="329fb-920">x</span><span class="sxs-lookup"><span data-stu-id="329fb-920">x</span></span>  

<!-- -->

<span data-ttu-id="329fb-921">y</span><span class="sxs-lookup"><span data-stu-id="329fb-921">y</span></span>  

<!-- -->

<span data-ttu-id="329fb-922">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-922">button</span></span>  

<!-- -->

<span data-ttu-id="329fb-923">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-923">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="329fb-924">Shift</span><span class="sxs-lookup"><span data-stu-id="329fb-924">Shift</span></span>  

### <a name="return-value---labelmousedblclick"></a><span data-ttu-id="329fb-925">戻り値 - labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="329fb-925">Return Value - labelMouseDblClick</span></span>

## <a name="method-labelmousedown"></a><span data-ttu-id="329fb-926">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="329fb-926">Method labelMouseDown</span></span>

```xpp
public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmousedown"></a><span data-ttu-id="329fb-927">パラメーター - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="329fb-927">Parameters - labelMouseDown</span></span>

<span data-ttu-id="329fb-928">x</span><span class="sxs-lookup"><span data-stu-id="329fb-928">x</span></span>  

<!-- -->

<span data-ttu-id="329fb-929">y</span><span class="sxs-lookup"><span data-stu-id="329fb-929">y</span></span>  

<!-- -->

<span data-ttu-id="329fb-930">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-930">button</span></span>  

<!-- -->

<span data-ttu-id="329fb-931">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-931">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="329fb-932">Shift</span><span class="sxs-lookup"><span data-stu-id="329fb-932">Shift</span></span>  

### <a name="return-value---labelmousedown"></a><span data-ttu-id="329fb-933">戻り値 - labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="329fb-933">Return Value - labelMouseDown</span></span>

## <a name="method-labelmouseup"></a><span data-ttu-id="329fb-934">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="329fb-934">Method labelMouseUp</span></span>

```xpp
public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---labelmouseup"></a><span data-ttu-id="329fb-935">パラメーター - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="329fb-935">Parameters - labelMouseUp</span></span>

<span data-ttu-id="329fb-936">x</span><span class="sxs-lookup"><span data-stu-id="329fb-936">x</span></span>  

<!-- -->

<span data-ttu-id="329fb-937">y</span><span class="sxs-lookup"><span data-stu-id="329fb-937">y</span></span>  

<!-- -->

<span data-ttu-id="329fb-938">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-938">button</span></span>  

<!-- -->

<span data-ttu-id="329fb-939">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-939">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="329fb-940">Shift</span><span class="sxs-lookup"><span data-stu-id="329fb-940">Shift</span></span>  

### <a name="return-value---labelmouseup"></a><span data-ttu-id="329fb-941">戻り値 - labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="329fb-941">Return Value - labelMouseUp</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="329fb-942">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="329fb-942">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="329fb-943">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="329fb-943">Parameters - labelPosition</span></span>

<span data-ttu-id="329fb-944">値</span><span class="sxs-lookup"><span data-stu-id="329fb-944">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="329fb-945">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="329fb-945">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="329fb-946">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="329fb-946">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="329fb-947">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="329fb-947">Parameters - labelUnderline</span></span>

<span data-ttu-id="329fb-948">値</span><span class="sxs-lookup"><span data-stu-id="329fb-948">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="329fb-949">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="329fb-949">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="329fb-950">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="329fb-950">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="329fb-951">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="329fb-951">Parameters - labelWidth</span></span>

<span data-ttu-id="329fb-952">値</span><span class="sxs-lookup"><span data-stu-id="329fb-952">value</span></span>  

<!-- -->

<span data-ttu-id="329fb-953">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-953">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="329fb-954">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="329fb-954">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="329fb-955">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="329fb-955">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="329fb-956">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="329fb-956">Parameters - labelWidthMode</span></span>

<span data-ttu-id="329fb-957">値</span><span class="sxs-lookup"><span data-stu-id="329fb-957">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="329fb-958">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="329fb-958">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="329fb-959">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="329fb-959">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="329fb-960">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="329fb-960">Parameters - labelWidthValue</span></span>

<span data-ttu-id="329fb-961">値</span><span class="sxs-lookup"><span data-stu-id="329fb-961">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="329fb-962">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="329fb-962">Return Value - labelWidthValue</span></span>

## <a name="method-leave"></a><span data-ttu-id="329fb-963">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="329fb-963">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="329fb-964">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="329fb-964">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="329fb-965">メソッド left</span><span class="sxs-lookup"><span data-stu-id="329fb-965">Method left</span></span>

<span data-ttu-id="329fb-966">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-966">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="329fb-967">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="329fb-967">Parameters - left</span></span>

<span data-ttu-id="329fb-968">値</span><span class="sxs-lookup"><span data-stu-id="329fb-968">value</span></span>  
<span data-ttu-id="329fb-969">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-969">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="329fb-970">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-970">mode</span></span>  
<span data-ttu-id="329fb-971">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-971">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="329fb-972">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="329fb-972">Return Value - left</span></span>

<span data-ttu-id="329fb-973">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="329fb-973">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="329fb-974">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="329fb-974">Method leftMode</span></span>

<span data-ttu-id="329fb-975">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-975">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="329fb-976">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="329fb-976">Parameters - leftMode</span></span>

<span data-ttu-id="329fb-977">値</span><span class="sxs-lookup"><span data-stu-id="329fb-977">value</span></span>  
<span data-ttu-id="329fb-978">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-978">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="329fb-979">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="329fb-979">Return Value - leftMode</span></span>

<span data-ttu-id="329fb-980">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="329fb-980">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="329fb-981">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="329fb-981">Method leftValue</span></span>

<span data-ttu-id="329fb-982">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-982">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="329fb-983">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="329fb-983">Parameters - leftValue</span></span>

<span data-ttu-id="329fb-984">値</span><span class="sxs-lookup"><span data-stu-id="329fb-984">value</span></span>  
<span data-ttu-id="329fb-985">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-985">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="329fb-986">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="329fb-986">Return Value - leftValue</span></span>

<span data-ttu-id="329fb-987">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="329fb-987">The horizontal position of the control in the form.</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="329fb-988">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="329fb-988">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="329fb-989">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="329fb-989">Parameters - mandatory</span></span>

<span data-ttu-id="329fb-990">値</span><span class="sxs-lookup"><span data-stu-id="329fb-990">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="329fb-991">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="329fb-991">Return Value - mandatory</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="329fb-992">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="329fb-992">Method markAsUserAdd</span></span>

<span data-ttu-id="329fb-993">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="329fb-993">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="329fb-994">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="329fb-994">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="329fb-995">値</span><span class="sxs-lookup"><span data-stu-id="329fb-995">value</span></span>  
<span data-ttu-id="329fb-996">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-996">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="329fb-997">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="329fb-997">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="329fb-998">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-998">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="329fb-999">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="329fb-999">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="329fb-1000">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="329fb-1000">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="329fb-1001">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="329fb-1001">Method mouseDblClick</span></span>

<span data-ttu-id="329fb-1002">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1002">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="329fb-1003">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="329fb-1003">Parameters - mouseDblClick</span></span>

<span data-ttu-id="329fb-1004">x</span><span class="sxs-lookup"><span data-stu-id="329fb-1004">x</span></span>  
<span data-ttu-id="329fb-1005">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1005">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1006">y</span><span class="sxs-lookup"><span data-stu-id="329fb-1006">y</span></span>  
<span data-ttu-id="329fb-1007">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1007">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1008">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-1008">button</span></span>  
<span data-ttu-id="329fb-1009">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1009">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1010">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-1010">Ctrl</span></span>  
<span data-ttu-id="329fb-1011">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1011">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1012">シフト</span><span class="sxs-lookup"><span data-stu-id="329fb-1012">Shift</span></span>  
<span data-ttu-id="329fb-1013">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1013">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="329fb-1014">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="329fb-1014">Return Value - mouseDblClick</span></span>

<span data-ttu-id="329fb-1015">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1015">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="329fb-1016">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="329fb-1016">Remarks - mouseDblClick</span></span>

<span data-ttu-id="329fb-1017">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1017">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="329fb-1018">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="329fb-1018">Method mouseDown</span></span>

<span data-ttu-id="329fb-1019">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1019">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="329fb-1020">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="329fb-1020">Parameters - mouseDown</span></span>

<span data-ttu-id="329fb-1021">x</span><span class="sxs-lookup"><span data-stu-id="329fb-1021">x</span></span>  
<span data-ttu-id="329fb-1022">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1022">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1023">y</span><span class="sxs-lookup"><span data-stu-id="329fb-1023">y</span></span>  
<span data-ttu-id="329fb-1024">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1024">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1025">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-1025">button</span></span>  
<span data-ttu-id="329fb-1026">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1026">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1027">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-1027">Ctrl</span></span>  
<span data-ttu-id="329fb-1028">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1028">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1029">シフト</span><span class="sxs-lookup"><span data-stu-id="329fb-1029">Shift</span></span>  
<span data-ttu-id="329fb-1030">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1030">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="329fb-1031">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="329fb-1031">Return Value - mouseDown</span></span>

<span data-ttu-id="329fb-1032">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1032">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="329fb-1033">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="329fb-1033">Remarks - mouseDown</span></span>

<span data-ttu-id="329fb-1034">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1034">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="329fb-1035">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1035">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="329fb-1036">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="329fb-1036">Method mouseMove</span></span>

<span data-ttu-id="329fb-1037">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1037">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="329fb-1038">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="329fb-1038">Parameters - mouseMove</span></span>

<span data-ttu-id="329fb-1039">x</span><span class="sxs-lookup"><span data-stu-id="329fb-1039">x</span></span>  
<span data-ttu-id="329fb-1040">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1040">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1041">y</span><span class="sxs-lookup"><span data-stu-id="329fb-1041">y</span></span>  
<span data-ttu-id="329fb-1042">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1042">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1043">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-1043">button</span></span>  
<span data-ttu-id="329fb-1044">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1044">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1045">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-1045">Ctrl</span></span>  
<span data-ttu-id="329fb-1046">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1046">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1047">シフト</span><span class="sxs-lookup"><span data-stu-id="329fb-1047">Shift</span></span>  
<span data-ttu-id="329fb-1048">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1048">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="329fb-1049">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="329fb-1049">Return Value - mouseMove</span></span>

<span data-ttu-id="329fb-1050">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1050">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="329fb-1051">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="329fb-1051">Remarks - mouseMove</span></span>

<span data-ttu-id="329fb-1052">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1052">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="329fb-1053">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="329fb-1053">Method mouseUp</span></span>

<span data-ttu-id="329fb-1054">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1054">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="329fb-1055">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="329fb-1055">Parameters - mouseUp</span></span>

<span data-ttu-id="329fb-1056">x</span><span class="sxs-lookup"><span data-stu-id="329fb-1056">x</span></span>  
<span data-ttu-id="329fb-1057">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1057">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1058">y</span><span class="sxs-lookup"><span data-stu-id="329fb-1058">y</span></span>  
<span data-ttu-id="329fb-1059">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1059">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1060">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-1060">button</span></span>  
<span data-ttu-id="329fb-1061">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1061">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1062">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-1062">Ctrl</span></span>  
<span data-ttu-id="329fb-1063">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1063">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1064">シフト</span><span class="sxs-lookup"><span data-stu-id="329fb-1064">Shift</span></span>  
<span data-ttu-id="329fb-1065">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1065">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="329fb-1066">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="329fb-1066">Return Value - mouseUp</span></span>

<span data-ttu-id="329fb-1067">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1067">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="329fb-1068">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="329fb-1068">Remarks - mouseUp</span></span>

<span data-ttu-id="329fb-1069">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1069">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="329fb-1070">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1070">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="329fb-1071">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="329fb-1071">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="329fb-1072">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="329fb-1072">Parameters - moveControl</span></span>

<span data-ttu-id="329fb-1073">controlId</span><span class="sxs-lookup"><span data-stu-id="329fb-1073">controlId</span></span>  

<!-- -->

<span data-ttu-id="329fb-1074">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="329fb-1074">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="329fb-1075">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="329fb-1075">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="329fb-1076">メソッド名</span><span class="sxs-lookup"><span data-stu-id="329fb-1076">Method name</span></span>

<span data-ttu-id="329fb-1077">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1077">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="329fb-1078">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="329fb-1078">Parameters - name</span></span>

<span data-ttu-id="329fb-1079">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1079">value</span></span>  
<span data-ttu-id="329fb-1080">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="329fb-1080">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="329fb-1081">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="329fb-1081">Return Value - name</span></span>

<span data-ttu-id="329fb-1082">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="329fb-1082">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="329fb-1083">備考 - name</span><span class="sxs-lookup"><span data-stu-id="329fb-1083">Remarks - name</span></span>

<span data-ttu-id="329fb-1084">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="329fb-1084">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="329fb-1085">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="329fb-1085">It must start with a letter.</span></span>
-   <span data-ttu-id="329fb-1086">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="329fb-1086">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="329fb-1087">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1087">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="329fb-1088">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="329fb-1088">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="329fb-1089">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="329fb-1089">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="329fb-1090">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="329fb-1090">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="329fb-1091">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="329fb-1091">Parameters - neededPermission</span></span>

<span data-ttu-id="329fb-1092">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1092">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="329fb-1093">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="329fb-1093">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="329fb-1094">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="329fb-1094">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="329fb-1095">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="329fb-1095">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="329fb-1096">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="329fb-1096">Method parentControl</span></span>

<span data-ttu-id="329fb-1097">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1097">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="329fb-1098">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="329fb-1098">Return Value - parentControl</span></span>

<span data-ttu-id="329fb-1099">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="329fb-1099">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="329fb-1100">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="329fb-1100">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="329fb-1101">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="329fb-1101">Parameters - previewPartRef</span></span>

<span data-ttu-id="329fb-1102">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1102">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="329fb-1103">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="329fb-1103">Return Value - previewPartRef</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="329fb-1104">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="329fb-1104">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="329fb-1105">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="329fb-1105">Parameters - promptrect</span></span>

<span data-ttu-id="329fb-1106">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1106">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="329fb-1107">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="329fb-1107">Return Value - promptrect</span></span>

## <a name="method-referencefield"></a><span data-ttu-id="329fb-1108">メソッド referenceField</span><span class="sxs-lookup"><span data-stu-id="329fb-1108">Method referenceField</span></span>

```xpp
public FieldId referenceField([FieldId value])
```

### <a name="parameters---referencefield"></a><span data-ttu-id="329fb-1109">パラメーター - referenceField</span><span class="sxs-lookup"><span data-stu-id="329fb-1109">Parameters - referenceField</span></span>

<span data-ttu-id="329fb-1110">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1110">value</span></span>  

### <a name="return-value---referencefield"></a><span data-ttu-id="329fb-1111">戻り値 - referenceField</span><span class="sxs-lookup"><span data-stu-id="329fb-1111">Return Value - referenceField</span></span>

## <a name="method-replacementfieldgroup"></a><span data-ttu-id="329fb-1112">メソッド replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="329fb-1112">Method replacementFieldGroup</span></span>

```xpp
public str replacementFieldGroup([str value])
```

### <a name="parameters---replacementfieldgroup"></a><span data-ttu-id="329fb-1113">パラメーター - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="329fb-1113">Parameters - replacementFieldGroup</span></span>

<span data-ttu-id="329fb-1114">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1114">value</span></span>  

### <a name="return-value---replacementfieldgroup"></a><span data-ttu-id="329fb-1115">戻り値 - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="329fb-1115">Return Value - replacementFieldGroup</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="329fb-1116">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="329fb-1116">Method securityKey</span></span>

<span data-ttu-id="329fb-1117">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1117">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="329fb-1118">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="329fb-1118">Parameters - securityKey</span></span>

<span data-ttu-id="329fb-1119">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1119">value</span></span>  
<span data-ttu-id="329fb-1120">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1120">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="329fb-1121">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="329fb-1121">Return Value - securityKey</span></span>

<span data-ttu-id="329fb-1122">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1122">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="329fb-1123">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="329fb-1123">Method showContextMenu</span></span>

<span data-ttu-id="329fb-1124">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1124">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="329fb-1125">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="329fb-1125">Parameters - showContextMenu</span></span>

<span data-ttu-id="329fb-1126">menuHandle</span><span class="sxs-lookup"><span data-stu-id="329fb-1126">menuHandle</span></span>  
<span data-ttu-id="329fb-1127">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="329fb-1127">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="329fb-1128">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="329fb-1128">Return Value - showContextMenu</span></span>

<span data-ttu-id="329fb-1129">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1129">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="329fb-1130">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="329fb-1130">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="329fb-1131">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="329fb-1131">Parameters - showLabel</span></span>

<span data-ttu-id="329fb-1132">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1132">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="329fb-1133">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="329fb-1133">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="329fb-1134">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="329fb-1134">Method skip</span></span>

<span data-ttu-id="329fb-1135">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1135">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="329fb-1136">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="329fb-1136">Parameters - skip</span></span>

<span data-ttu-id="329fb-1137">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1137">value</span></span>  
<span data-ttu-id="329fb-1138">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1138">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="329fb-1139">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="329fb-1139">Return Value - skip</span></span>

<span data-ttu-id="329fb-1140">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="329fb-1140">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="329fb-1141">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="329fb-1141">Remarks - skip</span></span>

<span data-ttu-id="329fb-1142">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1142">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="329fb-1143">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="329fb-1143">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="329fb-1144">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="329fb-1144">Parameters - sort</span></span>

<span data-ttu-id="329fb-1145">sortDirection</span><span class="sxs-lookup"><span data-stu-id="329fb-1145">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="329fb-1146">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="329fb-1146">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="329fb-1147">メソッド style</span><span class="sxs-lookup"><span data-stu-id="329fb-1147">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="329fb-1148">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="329fb-1148">Parameters - style</span></span>

<span data-ttu-id="329fb-1149">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1149">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="329fb-1150">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="329fb-1150">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="329fb-1151">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="329fb-1151">Method toolTip</span></span>

<span data-ttu-id="329fb-1152">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1152">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="329fb-1153">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="329fb-1153">Return Value - toolTip</span></span>

<span data-ttu-id="329fb-1154">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="329fb-1154">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="329fb-1155">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="329fb-1155">Remarks - toolTip</span></span>

<span data-ttu-id="329fb-1156">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1156">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="329fb-1157">メソッド top</span><span class="sxs-lookup"><span data-stu-id="329fb-1157">Method top</span></span>

<span data-ttu-id="329fb-1158">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1158">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="329fb-1159">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="329fb-1159">Parameters - top</span></span>

<span data-ttu-id="329fb-1160">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1160">value</span></span>  
<span data-ttu-id="329fb-1161">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1161">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="329fb-1162">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-1162">mode</span></span>  
<span data-ttu-id="329fb-1163">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1163">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="329fb-1164">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="329fb-1164">Return Value - top</span></span>

<span data-ttu-id="329fb-1165">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="329fb-1165">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="329fb-1166">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1166">Method topMode</span></span>

<span data-ttu-id="329fb-1167">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1167">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="329fb-1168">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1168">Parameters - topMode</span></span>

<span data-ttu-id="329fb-1169">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1169">value</span></span>  
<span data-ttu-id="329fb-1170">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1170">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="329fb-1171">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1171">Return Value - topMode</span></span>

<span data-ttu-id="329fb-1172">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="329fb-1172">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="329fb-1173">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1173">Method topValue</span></span>

<span data-ttu-id="329fb-1174">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1174">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="329fb-1175">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1175">Parameters - topValue</span></span>

<span data-ttu-id="329fb-1176">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1176">value</span></span>  
<span data-ttu-id="329fb-1177">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1177">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="329fb-1178">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1178">Return Value - topValue</span></span>

<span data-ttu-id="329fb-1179">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="329fb-1179">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="329fb-1180">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="329fb-1180">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="329fb-1181">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="329fb-1181">Parameters - type</span></span>

<span data-ttu-id="329fb-1182">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1182">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="329fb-1183">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="329fb-1183">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="329fb-1184">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="329fb-1184">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="329fb-1185">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="329fb-1185">Parameters - underline</span></span>

<span data-ttu-id="329fb-1186">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1186">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="329fb-1187">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="329fb-1187">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="329fb-1188">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="329fb-1188">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="329fb-1189">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="329fb-1189">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="329fb-1190">データ</span><span class="sxs-lookup"><span data-stu-id="329fb-1190">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="329fb-1191">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="329fb-1191">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="329fb-1192">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="329fb-1192">Method userData</span></span>

<span data-ttu-id="329fb-1193">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1193">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="329fb-1194">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="329fb-1194">Parameters - userData</span></span>

<span data-ttu-id="329fb-1195">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1195">value</span></span>  
<span data-ttu-id="329fb-1196">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1196">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="329fb-1197">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="329fb-1197">Return Value - userData</span></span>

<span data-ttu-id="329fb-1198">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="329fb-1198">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="329fb-1199">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="329fb-1199">Method userDataItem</span></span>

<span data-ttu-id="329fb-1200">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1200">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="329fb-1201">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="329fb-1201">Parameters - userDataItem</span></span>

<span data-ttu-id="329fb-1202">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1202">value</span></span>  
<span data-ttu-id="329fb-1203">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1203">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="329fb-1204">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="329fb-1204">Return Value - userDataItem</span></span>

<span data-ttu-id="329fb-1205">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="329fb-1205">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="329fb-1206">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="329fb-1206">Method userDataItems</span></span>

<span data-ttu-id="329fb-1207">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1207">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="329fb-1208">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="329fb-1208">Parameters - userDataItems</span></span>

<span data-ttu-id="329fb-1209">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1209">value</span></span>  
<span data-ttu-id="329fb-1210">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1210">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="329fb-1211">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="329fb-1211">Return Value - userDataItems</span></span>

<span data-ttu-id="329fb-1212">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="329fb-1212">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="329fb-1213">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="329fb-1213">Method userDisable</span></span>

<span data-ttu-id="329fb-1214">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1214">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="329fb-1215">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="329fb-1215">Parameters - userDisable</span></span>

<span data-ttu-id="329fb-1216">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1216">value</span></span>  
<span data-ttu-id="329fb-1217">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1217">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="329fb-1218">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="329fb-1218">Return Value - userDisable</span></span>

<span data-ttu-id="329fb-1219">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1219">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="329fb-1220">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="329fb-1220">Method userHeight</span></span>

<span data-ttu-id="329fb-1221">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1221">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="329fb-1222">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="329fb-1222">Parameters - userHeight</span></span>

<span data-ttu-id="329fb-1223">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1223">value</span></span>  
<span data-ttu-id="329fb-1224">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1224">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="329fb-1225">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="329fb-1225">Return Value - userHeight</span></span>

<span data-ttu-id="329fb-1226">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="329fb-1226">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="329fb-1227">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="329fb-1227">Method userHide</span></span>

<span data-ttu-id="329fb-1228">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1228">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="329fb-1229">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="329fb-1229">Parameters - userHide</span></span>

<span data-ttu-id="329fb-1230">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1230">value</span></span>  
<span data-ttu-id="329fb-1231">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1231">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="329fb-1232">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="329fb-1232">Return Value - userHide</span></span>

<span data-ttu-id="329fb-1233">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1233">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="329fb-1234">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="329fb-1234">Remarks - userHide</span></span>

<span data-ttu-id="329fb-1235">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1235">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="329fb-1236">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1236">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="329fb-1237">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1237">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="329fb-1238">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="329fb-1238">Method userOrgContainer</span></span>

<span data-ttu-id="329fb-1239">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1239">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="329fb-1240">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="329fb-1240">Parameters - userOrgContainer</span></span>

<span data-ttu-id="329fb-1241">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1241">value</span></span>  
<span data-ttu-id="329fb-1242">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1242">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="329fb-1243">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="329fb-1243">Return Value - userOrgContainer</span></span>

<span data-ttu-id="329fb-1244">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="329fb-1244">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="329fb-1245">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="329fb-1245">Method userOrgSibling</span></span>

<span data-ttu-id="329fb-1246">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1246">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="329fb-1247">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="329fb-1247">Parameters - userOrgSibling</span></span>

<span data-ttu-id="329fb-1248">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1248">value</span></span>  
<span data-ttu-id="329fb-1249">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1249">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="329fb-1250">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="329fb-1250">Return Value - userOrgSibling</span></span>

<span data-ttu-id="329fb-1251">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="329fb-1251">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="329fb-1252">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="329fb-1252">Method userPromptText</span></span>

<span data-ttu-id="329fb-1253">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1253">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="329fb-1254">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="329fb-1254">Parameters - userPromptText</span></span>

<span data-ttu-id="329fb-1255">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1255">value</span></span>  
<span data-ttu-id="329fb-1256">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1256">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="329fb-1257">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="329fb-1257">Return Value - userPromptText</span></span>

<span data-ttu-id="329fb-1258">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="329fb-1258">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="329fb-1259">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="329fb-1259">Method userSecurityLevel</span></span>

<span data-ttu-id="329fb-1260">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1260">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="329fb-1261">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="329fb-1261">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="329fb-1262">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1262">value</span></span>  
<span data-ttu-id="329fb-1263">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1263">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="329fb-1264">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="329fb-1264">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="329fb-1265">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="329fb-1265">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="329fb-1266">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="329fb-1266">Method userSkip</span></span>

<span data-ttu-id="329fb-1267">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1267">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="329fb-1268">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="329fb-1268">Parameters - userSkip</span></span>

<span data-ttu-id="329fb-1269">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1269">value</span></span>  
<span data-ttu-id="329fb-1270">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1270">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="329fb-1271">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1271">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="329fb-1272">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="329fb-1272">Return Value - userSkip</span></span>

<span data-ttu-id="329fb-1273">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="329fb-1273">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="329fb-1274">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="329fb-1274">Method userWidth</span></span>

<span data-ttu-id="329fb-1275">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1275">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="329fb-1276">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="329fb-1276">Parameters - userWidth</span></span>

<span data-ttu-id="329fb-1277">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1277">value</span></span>  
<span data-ttu-id="329fb-1278">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1278">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="329fb-1279">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="329fb-1279">Return Value - userWidth</span></span>

<span data-ttu-id="329fb-1280">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1280">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="329fb-1281">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="329fb-1281">Remarks - userWidth</span></span>

<span data-ttu-id="329fb-1282">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1282">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="329fb-1283">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="329fb-1283">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="329fb-1284">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1284">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="329fb-1285">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="329fb-1285">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="329fb-1286">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="329fb-1286">Parameters - useUserLayout</span></span>

<span data-ttu-id="329fb-1287">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1287">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="329fb-1288">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="329fb-1288">Return Value - useUserLayout</span></span>

## <a name="method-validate"></a><span data-ttu-id="329fb-1289">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="329fb-1289">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="329fb-1290">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="329fb-1290">Return Value - validate</span></span>

## <a name="method-value"></a><span data-ttu-id="329fb-1291">メソッド value</span><span class="sxs-lookup"><span data-stu-id="329fb-1291">Method value</span></span>

```xpp
public Int64 value([Int64 value])
```

### <a name="parameters---value"></a><span data-ttu-id="329fb-1292">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="329fb-1292">Parameters - value</span></span>

<span data-ttu-id="329fb-1293">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1293">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="329fb-1294">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="329fb-1294">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="329fb-1295">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="329fb-1295">Method verticalSpacing</span></span>

<span data-ttu-id="329fb-1296">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1296">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="329fb-1297">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="329fb-1297">Parameters - verticalSpacing</span></span>

<span data-ttu-id="329fb-1298">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1298">value</span></span>  
<span data-ttu-id="329fb-1299">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1299">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="329fb-1300">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-1300">mode</span></span>  
<span data-ttu-id="329fb-1301">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1301">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="329fb-1302">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="329fb-1302">Return Value - verticalSpacing</span></span>

<span data-ttu-id="329fb-1303">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="329fb-1303">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="329fb-1304">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1304">Method verticalSpacingMode</span></span>

<span data-ttu-id="329fb-1305">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1305">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="329fb-1306">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1306">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="329fb-1307">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-1307">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="329fb-1308">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1308">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="329fb-1309">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="329fb-1309">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="329fb-1310">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1310">Method verticalSpacingValue</span></span>

<span data-ttu-id="329fb-1311">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1311">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="329fb-1312">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1312">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="329fb-1313">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1313">value</span></span>  
<span data-ttu-id="329fb-1314">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1314">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="329fb-1315">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1315">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="329fb-1316">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="329fb-1316">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="329fb-1317">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1317">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="329fb-1318">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1318">Parameters - viewEditMode</span></span>

<span data-ttu-id="329fb-1319">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1319">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="329fb-1320">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1320">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="329fb-1321">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="329fb-1321">Method visible</span></span>

<span data-ttu-id="329fb-1322">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1322">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="329fb-1323">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="329fb-1323">Parameters - visible</span></span>

<span data-ttu-id="329fb-1324">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1324">value</span></span>  
<span data-ttu-id="329fb-1325">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1325">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="329fb-1326">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="329fb-1326">Return Value - visible</span></span>

<span data-ttu-id="329fb-1327">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="329fb-1327">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="329fb-1328">メソッド width</span><span class="sxs-lookup"><span data-stu-id="329fb-1328">Method width</span></span>

<span data-ttu-id="329fb-1329">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1329">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="329fb-1330">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="329fb-1330">Parameters - width</span></span>

<span data-ttu-id="329fb-1331">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1331">value</span></span>  
<span data-ttu-id="329fb-1332">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1332">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="329fb-1333">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-1333">mode</span></span>  
<span data-ttu-id="329fb-1334">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1334">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="329fb-1335">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="329fb-1335">Return Value - width</span></span>

<span data-ttu-id="329fb-1336">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="329fb-1336">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="329fb-1337">備考 - width</span><span class="sxs-lookup"><span data-stu-id="329fb-1337">Remarks - width</span></span>

<span data-ttu-id="329fb-1338">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1338">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="329fb-1339">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1339">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="329fb-1340">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-1340">Mode</span></span>           | <span data-ttu-id="329fb-1341">幅計算</span><span class="sxs-lookup"><span data-stu-id="329fb-1341">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="329fb-1342">-1 正確</span><span class="sxs-lookup"><span data-stu-id="329fb-1342">-1 Exact</span></span>       | <span data-ttu-id="329fb-1343">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1343">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="329fb-1344">0 自動</span><span class="sxs-lookup"><span data-stu-id="329fb-1344">0 Auto</span></span>         | <span data-ttu-id="329fb-1345">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1345">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="329fb-1346">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="329fb-1346">1 Column width</span></span> | <span data-ttu-id="329fb-1347">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="329fb-1347">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="329fb-1348">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1348">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="329fb-1349">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1349">Method widthMode</span></span>

<span data-ttu-id="329fb-1350">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1350">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="329fb-1351">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1351">Parameters - widthMode</span></span>

<span data-ttu-id="329fb-1352">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1352">value</span></span>  
<span data-ttu-id="329fb-1353">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="329fb-1353">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="329fb-1354">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1354">Return Value - widthMode</span></span>

<span data-ttu-id="329fb-1355">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1355">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="329fb-1356">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1356">Remarks - widthMode</span></span>

<span data-ttu-id="329fb-1357">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1357">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="329fb-1358">モード</span><span class="sxs-lookup"><span data-stu-id="329fb-1358">Mode</span></span>         | <span data-ttu-id="329fb-1359">幅計算</span><span class="sxs-lookup"><span data-stu-id="329fb-1359">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="329fb-1360">正確</span><span class="sxs-lookup"><span data-stu-id="329fb-1360">Exact</span></span>        | <span data-ttu-id="329fb-1361">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1361">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="329fb-1362">自動</span><span class="sxs-lookup"><span data-stu-id="329fb-1362">Auto</span></span>         | <span data-ttu-id="329fb-1363">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1363">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="329fb-1364">列の幅</span><span class="sxs-lookup"><span data-stu-id="329fb-1364">Column width</span></span> | <span data-ttu-id="329fb-1365">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="329fb-1365">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="329fb-1366">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="329fb-1366">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="329fb-1367">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1367">Method widthValue</span></span>

<span data-ttu-id="329fb-1368">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1368">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="329fb-1369">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1369">Parameters - widthValue</span></span>

<span data-ttu-id="329fb-1370">値</span><span class="sxs-lookup"><span data-stu-id="329fb-1370">value</span></span>  
<span data-ttu-id="329fb-1371">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1371">An Integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="329fb-1372">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1372">Return Value - widthValue</span></span>

<span data-ttu-id="329fb-1373">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="329fb-1373">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="329fb-1374">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="329fb-1374">Remarks - widthValue</span></span>

<span data-ttu-id="329fb-1375">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1375">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="329fb-1376">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="329fb-1376">Method lostFocus</span></span>

<span data-ttu-id="329fb-1377">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1377">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="329fb-1378">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="329fb-1378">Method displayControl</span></span>

<span data-ttu-id="329fb-1379">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1379">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onmodified"></a><span data-ttu-id="329fb-1380">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="329fb-1380">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="329fb-1381">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="329fb-1381">Parameters - OnModified</span></span>

<span data-ttu-id="329fb-1382">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1382">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1383">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1383">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="329fb-1384">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="329fb-1384">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="329fb-1385">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="329fb-1385">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="329fb-1386">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="329fb-1386">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="329fb-1387">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="329fb-1387">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="329fb-1388">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="329fb-1388">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="329fb-1389">overrideObject</span><span class="sxs-lookup"><span data-stu-id="329fb-1389">overrideObject</span></span>  

## <a name="method-cut"></a><span data-ttu-id="329fb-1390">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="329fb-1390">Method cut</span></span>

<span data-ttu-id="329fb-1391">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="329fb-1391">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-mouseenter"></a><span data-ttu-id="329fb-1392">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="329fb-1392">Method mouseEnter</span></span>

<span data-ttu-id="329fb-1393">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1393">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="329fb-1394">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="329fb-1394">Parameters - mouseEnter</span></span>

<span data-ttu-id="329fb-1395">x</span><span class="sxs-lookup"><span data-stu-id="329fb-1395">x</span></span>  
<span data-ttu-id="329fb-1396">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1396">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1397">y</span><span class="sxs-lookup"><span data-stu-id="329fb-1397">y</span></span>  
<span data-ttu-id="329fb-1398">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1398">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1399">ボタン</span><span class="sxs-lookup"><span data-stu-id="329fb-1399">button</span></span>  
<span data-ttu-id="329fb-1400">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1400">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1401">Ctrl</span><span class="sxs-lookup"><span data-stu-id="329fb-1401">Ctrl</span></span>  
<span data-ttu-id="329fb-1402">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1402">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="329fb-1403">シフト</span><span class="sxs-lookup"><span data-stu-id="329fb-1403">Shift</span></span>  
<span data-ttu-id="329fb-1404">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1404">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="329fb-1405">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="329fb-1405">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="329fb-1406">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="329fb-1406">Parameters - OnEnter</span></span>

<span data-ttu-id="329fb-1407">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1407">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1408">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1408">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="329fb-1409">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="329fb-1409">Method dragLeave</span></span>

<span data-ttu-id="329fb-1410">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1410">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-filter"></a><span data-ttu-id="329fb-1411">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="329fb-1411">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="329fb-1412">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="329fb-1412">Parameters - filter</span></span>

<span data-ttu-id="329fb-1413">filterStr</span><span class="sxs-lookup"><span data-stu-id="329fb-1413">filterStr</span></span>  

## <a name="method-arrange"></a><span data-ttu-id="329fb-1414">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="329fb-1414">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-enter"></a><span data-ttu-id="329fb-1415">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="329fb-1415">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-paste"></a><span data-ttu-id="329fb-1416">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="329fb-1416">Method paste</span></span>

<span data-ttu-id="329fb-1417">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1417">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-onvalidating"></a><span data-ttu-id="329fb-1418">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="329fb-1418">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="329fb-1419">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="329fb-1419">Parameters - OnValidating</span></span>

<span data-ttu-id="329fb-1420">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1420">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1421">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1421">e</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="329fb-1422">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="329fb-1422">Method setFocus</span></span>

<span data-ttu-id="329fb-1423">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1423">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="329fb-1424">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="329fb-1424">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="329fb-1425">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="329fb-1425">Parameters - OnGotFocus</span></span>

<span data-ttu-id="329fb-1426">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1426">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1427">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1427">e</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="329fb-1428">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="329fb-1428">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="329fb-1429">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="329fb-1429">Parameters - OnLeaving</span></span>

<span data-ttu-id="329fb-1430">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1430">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1431">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1431">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="329fb-1432">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="329fb-1432">Method inputSearch</span></span>

<span data-ttu-id="329fb-1433">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1433">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="329fb-1434">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="329fb-1434">Parameters - inputSearch</span></span>

<span data-ttu-id="329fb-1435">searchStr</span><span class="sxs-lookup"><span data-stu-id="329fb-1435">searchStr</span></span>  
<span data-ttu-id="329fb-1436">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="329fb-1436">The string value to use to filter data; optional.</span></span>

## <a name="method-drop"></a><span data-ttu-id="329fb-1437">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="329fb-1437">Method drop</span></span>

<span data-ttu-id="329fb-1438">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1438">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="329fb-1439">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="329fb-1439">Parameters - drop</span></span>

<span data-ttu-id="329fb-1440">dragSource</span><span class="sxs-lookup"><span data-stu-id="329fb-1440">dragSource</span></span>  
<span data-ttu-id="329fb-1441">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1441">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-1442">dragMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1442">dragMode</span></span>  
<span data-ttu-id="329fb-1443">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1443">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-1444">x</span><span class="sxs-lookup"><span data-stu-id="329fb-1444">x</span></span>  
<span data-ttu-id="329fb-1445">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1445">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-1446">y</span><span class="sxs-lookup"><span data-stu-id="329fb-1446">y</span></span>  
<span data-ttu-id="329fb-1447">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1447">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="329fb-1448">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="329fb-1448">Method mouseLeave</span></span>

<span data-ttu-id="329fb-1449">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1449">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="329fb-1450">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="329fb-1450">Method prefColumnSize</span></span>

<span data-ttu-id="329fb-1451">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1451">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="329fb-1452">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="329fb-1452">Parameters - prefColumnSize</span></span>

<span data-ttu-id="329fb-1453">width</span><span class="sxs-lookup"><span data-stu-id="329fb-1453">width</span></span>  
<span data-ttu-id="329fb-1454">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="329fb-1454">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="329fb-1455">height</span><span class="sxs-lookup"><span data-stu-id="329fb-1455">height</span></span>  
<span data-ttu-id="329fb-1456">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="329fb-1456">The preferred height of the control.</span></span>

## <a name="method-undo"></a><span data-ttu-id="329fb-1457">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="329fb-1457">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-gotfocus"></a><span data-ttu-id="329fb-1458">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="329fb-1458">Method gotFocus</span></span>

<span data-ttu-id="329fb-1459">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1459">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="329fb-1460">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="329fb-1460">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="329fb-1461">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="329fb-1461">Parameters - OnLostFocus</span></span>

<span data-ttu-id="329fb-1462">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1462">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1463">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1463">e</span></span>  

## <a name="method-lookup"></a><span data-ttu-id="329fb-1464">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="329fb-1464">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="329fb-1465">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="329fb-1465">Method resetUserSetting</span></span>

<span data-ttu-id="329fb-1466">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="329fb-1466">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-onlookup"></a><span data-ttu-id="329fb-1467">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="329fb-1467">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="329fb-1468">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="329fb-1468">Parameters - OnLookup</span></span>

<span data-ttu-id="329fb-1469">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1469">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1470">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1470">e</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="329fb-1471">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="329fb-1471">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="329fb-1472">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="329fb-1472">Parameters - OnValidated</span></span>

<span data-ttu-id="329fb-1473">sender</span><span class="sxs-lookup"><span data-stu-id="329fb-1473">sender</span></span>  

<!-- -->

<span data-ttu-id="329fb-1474">e</span><span class="sxs-lookup"><span data-stu-id="329fb-1474">e</span></span>  

## <a name="method-copy"></a><span data-ttu-id="329fb-1475">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="329fb-1475">Method copy</span></span>

<span data-ttu-id="329fb-1476">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="329fb-1476">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-dropex"></a><span data-ttu-id="329fb-1477">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="329fb-1477">Method dropEx</span></span>

<span data-ttu-id="329fb-1478">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1478">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="329fb-1479">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="329fb-1479">Parameters - dropEx</span></span>

<span data-ttu-id="329fb-1480">dragSource</span><span class="sxs-lookup"><span data-stu-id="329fb-1480">dragSource</span></span>  
<span data-ttu-id="329fb-1481">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1481">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-1482">dragMode</span><span class="sxs-lookup"><span data-stu-id="329fb-1482">dragMode</span></span>  
<span data-ttu-id="329fb-1483">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1483">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-1484">x</span><span class="sxs-lookup"><span data-stu-id="329fb-1484">x</span></span>  
<span data-ttu-id="329fb-1485">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1485">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="329fb-1486">y</span><span class="sxs-lookup"><span data-stu-id="329fb-1486">y</span></span>  
<span data-ttu-id="329fb-1487">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="329fb-1487">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-context"></a><span data-ttu-id="329fb-1488">メソッド context</span><span class="sxs-lookup"><span data-stu-id="329fb-1488">Method context</span></span>

<span data-ttu-id="329fb-1489">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1489">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-enddrag"></a><span data-ttu-id="329fb-1490">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="329fb-1490">Method endDrag</span></span>

<span data-ttu-id="329fb-1491">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="329fb-1491">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="329fb-1492">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="329fb-1492">Remarks - endDrag</span></span>

<span data-ttu-id="329fb-1493">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="329fb-1493">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="329fb-1494">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="329fb-1494">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

