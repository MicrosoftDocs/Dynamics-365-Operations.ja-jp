---
title: FormRadioControl クラス
description: このトピックでは、FormRadioControl クラスについて説明します。
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
ms.openlocfilehash: 2defcf15540ff20d74f8bd1b8541ba38ef6bbe38
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502917"
---
# <a name="class-formradiocontrol"></a><span data-ttu-id="d33a7-103">クラス FormRadioControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-103">Class FormRadioControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormRadioControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="d33a7-104">備考</span><span class="sxs-lookup"><span data-stu-id="d33a7-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d33a7-105">例</span><span class="sxs-lookup"><span data-stu-id="d33a7-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d33a7-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d33a7-106">Methods</span></span>

| <span data-ttu-id="d33a7-107">方法</span><span class="sxs-lookup"><span data-stu-id="d33a7-107">Method</span></span>                                                                                                      | <span data-ttu-id="d33a7-108">説明</span><span class="sxs-lookup"><span data-stu-id="d33a7-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d33a7-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="d33a7-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-110">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="d33a7-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="d33a7-112">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-112">Determines whether the user can modify the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="d33a7-113">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="d33a7-113">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="d33a7-114">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-114">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="d33a7-115">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-115">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-116">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-116">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="d33a7-117">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-117">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="d33a7-118">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-118">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="d33a7-119">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-119">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="d33a7-120">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-120">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="d33a7-121">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-121">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="d33a7-122">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d33a7-122">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="d33a7-123">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-123">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="d33a7-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-124">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="d33a7-125">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-125">Gets or sets the font weight that is used to display text in the control.</span></span>                                                                                               |
| <span data-ttu-id="d33a7-126">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-126">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-127">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-127">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-128">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-128">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="d33a7-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="d33a7-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="d33a7-132">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-132">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="d33a7-133">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-133">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="d33a7-134">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-134">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="d33a7-135">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-135">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="d33a7-136">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-136">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="d33a7-137">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-137">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="d33a7-138">public int columns(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-138">public int columns(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="d33a7-140">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-140">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="d33a7-141">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="d33a7-141">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="d33a7-142">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-142">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="d33a7-143">public int count()</span><span class="sxs-lookup"><span data-stu-id="d33a7-143">public int count()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-144">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-144">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="d33a7-145">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-145">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="d33a7-146">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-146">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-147">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-147">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-148">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-148">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-149">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-149">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="d33a7-150">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-150">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="d33a7-151">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-151">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="d33a7-152">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-152">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="d33a7-153">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-153">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-154">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-154">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-155">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-155">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-156">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-156">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="d33a7-157">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-157">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="d33a7-158">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-158">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="d33a7-159">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-159">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="d33a7-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d33a7-160">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="d33a7-161">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-161">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="d33a7-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d33a7-162">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="d33a7-163">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-163">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="d33a7-164">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="d33a7-164">public str dragText()</span></span>                                                                                       | <span data-ttu-id="d33a7-165">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-165">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="d33a7-166">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-166">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="d33a7-167">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-167">Determines whether the object is enabled or disabled.</span></span>                                                                                                                   |
| <span data-ttu-id="d33a7-168">public EnumId enumType(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-168">public EnumId enumType(\[EnumId value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-169">public EnumId enumTypeValue()</span><span class="sxs-lookup"><span data-stu-id="d33a7-169">public EnumId enumTypeValue()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-170">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-170">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-171">public int find(str string)</span><span class="sxs-lookup"><span data-stu-id="d33a7-171">public int find(str string)</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-172">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-172">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="d33a7-173">コントロールに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-173">Gets or sets the name of the font that is used for the control.</span></span>                                                                                                         |
| <span data-ttu-id="d33a7-174">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-174">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="d33a7-175">コントロール内のテキストに使用されるフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-175">Gets or sets the font size that is used for the control.</span></span>                                                                                                                |
| <span data-ttu-id="d33a7-176">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-176">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="d33a7-177">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-177">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="d33a7-178">public int framePosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-178">public int framePosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-179">public int frameType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-179">public int frameType(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-180">public str getText(int index)</span><span class="sxs-lookup"><span data-stu-id="d33a7-180">public str getText(int index)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-181">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-181">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="d33a7-182">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-182">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="d33a7-183">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="d33a7-183">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="d33a7-184">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-184">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="d33a7-185">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-185">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="d33a7-186">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-186">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="d33a7-187">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-187">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="d33a7-188">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-188">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="d33a7-189">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-189">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="d33a7-190">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-190">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="d33a7-191">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="d33a7-191">public str helpField()</span></span>                                                                                      | <span data-ttu-id="d33a7-192">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-192">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="d33a7-193">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-193">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="d33a7-194">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-194">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>                                                         |
| <span data-ttu-id="d33a7-195">public boolean hideFirstEntry(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-195">public boolean hideFirstEntry(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-196">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-196">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="d33a7-197">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-197">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="d33a7-198">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="d33a7-198">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="d33a7-199">コントロールに関連付けられているウィンドウのハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-199">Returns the handle to the window that is associated with the control.</span></span>                                                                                                   |
| <span data-ttu-id="d33a7-200">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="d33a7-200">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="d33a7-201">コントロールがコンテナーかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-201">Gets a value that indicates whether the control is a container.</span></span>                                                                                                         |
| <span data-ttu-id="d33a7-202">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="d33a7-202">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="d33a7-203">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-203">Returns a value that indicates whether the control is displayed.</span></span>                                                                                                        |
| <span data-ttu-id="d33a7-204">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="d33a7-204">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="d33a7-205">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-205">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="d33a7-206">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="d33a7-206">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="d33a7-207">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-207">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="d33a7-208">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="d33a7-208">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-209">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-209">public boolean italic(\[boolean value\])</span></span>                                                                    | <span data-ttu-id="d33a7-210">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-210">Sets or returns a value that indicates whether the text in the control is italic.</span></span>                                                                                       |
| <span data-ttu-id="d33a7-211">public int item(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-211">public int item(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-212">public int items(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-212">public int items(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-213">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="d33a7-213">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-214">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-214">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="d33a7-215">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-215">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="d33a7-216">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-216">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-217">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-217">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-218">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-218">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-219">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-219">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="d33a7-220">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-220">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="d33a7-221">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-221">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="d33a7-222">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-222">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="d33a7-223">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-223">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="d33a7-224">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-224">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="d33a7-225">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="d33a7-225">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-226">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d33a7-226">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="d33a7-227">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-227">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="d33a7-228">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d33a7-228">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="d33a7-229">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-229">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="d33a7-230">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d33a7-230">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="d33a7-231">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-231">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="d33a7-232">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d33a7-232">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="d33a7-233">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-233">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="d33a7-234">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-234">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="d33a7-235">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-235">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="d33a7-236">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-236">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-237">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="d33a7-237">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-238">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="d33a7-238">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="d33a7-239">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-239">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="d33a7-240">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-240">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-241">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-241">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-242">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-242">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-243">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-243">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-244">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-244">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="d33a7-245">コントロールに関連付けられているセキュリティ キーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-245">Sets or returns the security key that is associated with the control.</span></span>                                                                                                   |
| <span data-ttu-id="d33a7-246">public int selection(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-246">public int selection(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-247">public int selectionChange()</span><span class="sxs-lookup"><span data-stu-id="d33a7-247">public int selectionChange()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-248">public int selectText(str string)</span><span class="sxs-lookup"><span data-stu-id="d33a7-248">public int selectText(str string)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-249">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="d33a7-249">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="d33a7-250">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-250">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="d33a7-251">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-251">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="d33a7-252">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-252">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="d33a7-253">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-253">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-254">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-254">public str text(\[str value\])</span></span>                                                                              | <span data-ttu-id="d33a7-255">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-255">Sets or returns the text for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="d33a7-256">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="d33a7-256">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="d33a7-257">コントロールのツールヒント テキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-257">Sets or returns the tooltip text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="d33a7-258">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-258">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="d33a7-259">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-259">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="d33a7-260">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-260">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-261">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-261">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-262">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-262">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-263">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-263">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="d33a7-264">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-264">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="d33a7-265">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-265">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="d33a7-266">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-266">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="d33a7-267">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-267">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-268">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-268">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="d33a7-269">コントロール内のテキストの下線プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-269">Sets or returns the value of the underline property for the text in the control.</span></span>                                                                                        |
| <span data-ttu-id="d33a7-270">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="d33a7-270">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-271">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-271">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="d33a7-272">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-272">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="d33a7-273">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-273">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="d33a7-274">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-274">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="d33a7-275">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-275">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="d33a7-276">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-276">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="d33a7-277">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-277">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="d33a7-278">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-278">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="d33a7-279">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-279">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="d33a7-280">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-280">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="d33a7-281">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-281">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="d33a7-282">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-282">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="d33a7-283">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-283">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="d33a7-284">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-284">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="d33a7-285">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-285">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="d33a7-286">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-286">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="d33a7-287">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-287">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="d33a7-288">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-288">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="d33a7-289">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-289">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="d33a7-290">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-290">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="d33a7-291">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-291">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="d33a7-292">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-292">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="d33a7-293">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-293">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="d33a7-294">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-294">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="d33a7-295">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="d33a7-295">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-296">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-296">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="d33a7-297">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-297">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="d33a7-298">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-298">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="d33a7-299">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-299">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="d33a7-300">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-300">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="d33a7-301">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-301">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="d33a7-302">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-302">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-303">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-303">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="d33a7-304">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-304">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="d33a7-305">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-305">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="d33a7-306">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-306">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="d33a7-307">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-307">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="d33a7-308">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-308">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="d33a7-309">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-309">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="d33a7-310">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-310">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="d33a7-311">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-311">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-312">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-312">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-313">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="d33a7-313">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="d33a7-314">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-314">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="d33a7-315">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="d33a7-315">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="d33a7-316">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-316">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="d33a7-317">public void insert(str string, int index)</span><span class="sxs-lookup"><span data-stu-id="d33a7-317">public void insert(str string, int index)</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-318">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-318">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                         |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-319">public void delete(str string)</span><span class="sxs-lookup"><span data-stu-id="d33a7-319">public void delete(str string)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-320">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="d33a7-320">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="d33a7-321">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-321">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="d33a7-322">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-322">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-323">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="d33a7-323">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-324">public void endUpdate()</span><span class="sxs-lookup"><span data-stu-id="d33a7-324">public void endUpdate()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-325">public void cut()</span><span class="sxs-lookup"><span data-stu-id="d33a7-325">public void cut()</span></span>                                                                                           | <span data-ttu-id="d33a7-326">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-326">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="d33a7-327">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="d33a7-327">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="d33a7-328">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-328">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="d33a7-329">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d33a7-329">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="d33a7-330">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-330">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="d33a7-331">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="d33a7-331">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="d33a7-332">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-332">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="d33a7-333">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-333">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-334">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-334">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-335">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="d33a7-335">public void displayControl()</span></span>                                                                                | <span data-ttu-id="d33a7-336">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-336">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="d33a7-337">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-337">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-338">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="d33a7-338">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="d33a7-339">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-339">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="d33a7-340">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="d33a7-340">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="d33a7-341">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-341">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="d33a7-342">public void add(str string)</span><span class="sxs-lookup"><span data-stu-id="d33a7-342">public void add(str string)</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-343">public void context()</span><span class="sxs-lookup"><span data-stu-id="d33a7-343">public void context()</span></span>                                                                                       | <span data-ttu-id="d33a7-344">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-344">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="d33a7-345">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-345">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-346">public void beginUpdate()</span><span class="sxs-lookup"><span data-stu-id="d33a7-346">public void beginUpdate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-347">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-347">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-348">public void enter()</span><span class="sxs-lookup"><span data-stu-id="d33a7-348">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-349">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="d33a7-349">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="d33a7-350">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-350">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="d33a7-351">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-351">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-352">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="d33a7-352">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="d33a7-353">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-353">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="d33a7-354">public void clear()</span><span class="sxs-lookup"><span data-stu-id="d33a7-354">public void clear()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-355">public void paste()</span><span class="sxs-lookup"><span data-stu-id="d33a7-355">public void paste()</span></span>                                                                                         | <span data-ttu-id="d33a7-356">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-356">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="d33a7-357">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="d33a7-357">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-358">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-358">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-359">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="d33a7-359">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="d33a7-360">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-360">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="d33a7-361">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="d33a7-361">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-362">public void undo()</span><span class="sxs-lookup"><span data-stu-id="d33a7-362">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="d33a7-363">public void copy()</span><span class="sxs-lookup"><span data-stu-id="d33a7-363">public void copy()</span></span>                                                                                          | <span data-ttu-id="d33a7-364">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-364">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="d33a7-365">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="d33a7-365">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="d33a7-366">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-366">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="d33a7-367">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-367">Method alignControl</span></span>

<span data-ttu-id="d33a7-368">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-368">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="d33a7-369">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-369">Parameters - alignControl</span></span>

<span data-ttu-id="d33a7-370">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-370">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="d33a7-371">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-371">Return Value - alignControl</span></span>

<span data-ttu-id="d33a7-372">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-372">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="d33a7-373">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-373">Remarks - alignControl</span></span>

<span data-ttu-id="d33a7-374">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-374">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="d33a7-375">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="d33a7-375">Method allowEdit</span></span>

<span data-ttu-id="d33a7-376">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-376">Determines whether the user can modify the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="d33a7-377">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d33a7-377">Parameters - allowEdit</span></span>

<span data-ttu-id="d33a7-378">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-378">value</span></span>  
<span data-ttu-id="d33a7-379">コントロールの allowEdit プロパティに割り当てるブール値: オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-379">The Boolean value to assign as the allowEdit property of the control; optional.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="d33a7-380">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d33a7-380">Return Value - allowEdit</span></span>

<span data-ttu-id="d33a7-381">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-381">true if the control can be modified; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="d33a7-382">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="d33a7-382">Remarks - allowEdit</span></span>

<span data-ttu-id="d33a7-383">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-383">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="d33a7-384">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="d33a7-384">Method allowSysSetup</span></span>

<span data-ttu-id="d33a7-385">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-385">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="d33a7-386">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="d33a7-386">Return Value - allowSysSetup</span></span>

<span data-ttu-id="d33a7-387">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-387">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="d33a7-388">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="d33a7-388">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="d33a7-389">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="d33a7-389">Parameters - arrayIndex</span></span>

<span data-ttu-id="d33a7-390">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-390">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="d33a7-391">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="d33a7-391">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="d33a7-392">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d33a7-392">Method autoDeclaration</span></span>

<span data-ttu-id="d33a7-393">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-393">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="d33a7-394">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d33a7-394">Parameters - autoDeclaration</span></span>

<span data-ttu-id="d33a7-395">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-395">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="d33a7-396">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d33a7-396">Return Value - autoDeclaration</span></span>

<span data-ttu-id="d33a7-397">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-397">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="d33a7-398">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="d33a7-398">Remarks - autoDeclaration</span></span>

<span data-ttu-id="d33a7-399">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-399">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="d33a7-400">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-400">Method backgroundColor</span></span>

<span data-ttu-id="d33a7-401">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-401">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="d33a7-402">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-402">Parameters - backgroundColor</span></span>

<span data-ttu-id="d33a7-403">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-403">value</span></span>  
<span data-ttu-id="d33a7-404">コントロールの背景色に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-404">The value to assign for the background color of the control; optional.</span></span>

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="d33a7-405">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-405">Return Value - backgroundColor</span></span>

<span data-ttu-id="d33a7-406">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="d33a7-406">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="d33a7-407">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-407">Remarks - backgroundColor</span></span>

<span data-ttu-id="d33a7-408">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-408">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="d33a7-409">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-409">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="d33a7-410">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-410">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="d33a7-411">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-411">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="d33a7-412">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-412">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="d33a7-413">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-413">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="d33a7-414">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="d33a7-414">Method backStyle</span></span>

<span data-ttu-id="d33a7-415">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-415">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="d33a7-416">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="d33a7-416">Parameters - backStyle</span></span>

<span data-ttu-id="d33a7-417">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-417">value</span></span>  
<span data-ttu-id="d33a7-418">コントロールの背景スタイルに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-418">The value to assign for the background style of the control; optional.</span></span>

### <a name="return-value---backstyle"></a><span data-ttu-id="d33a7-419">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="d33a7-419">Return Value - backStyle</span></span>

<span data-ttu-id="d33a7-420">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-420">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="d33a7-421">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="d33a7-421">Method beginDrag</span></span>

<span data-ttu-id="d33a7-422">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-422">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="d33a7-423">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="d33a7-423">Parameters - beginDrag</span></span>

<span data-ttu-id="d33a7-424">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-424">x</span></span>  
<span data-ttu-id="d33a7-425">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-425">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="d33a7-426">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-426">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="d33a7-427">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-427">y</span></span>  
<span data-ttu-id="d33a7-428">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-428">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="d33a7-429">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-429">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="d33a7-430">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="d33a7-430">Return Value - beginDrag</span></span>

<span data-ttu-id="d33a7-431">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-431">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="d33a7-432">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="d33a7-432">Remarks - beginDrag</span></span>

<span data-ttu-id="d33a7-433">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-433">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="d33a7-434">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-434">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="d33a7-435">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="d33a7-435">Method bold</span></span>

<span data-ttu-id="d33a7-436">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-436">Gets or sets the font weight that is used to display text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="d33a7-437">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="d33a7-437">Parameters - bold</span></span>

<span data-ttu-id="d33a7-438">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-438">value</span></span>  
<span data-ttu-id="d33a7-439">コントロールのボールド設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-439">The value to assign to the bold setting of the control; optional.</span></span>

### <a name="return-value---bold"></a><span data-ttu-id="d33a7-440">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="d33a7-440">Return Value - bold</span></span>

<span data-ttu-id="d33a7-441">0 (ゼロ) から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-441">An integer value between 0 (zero) and 9, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="d33a7-442">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="d33a7-442">Remarks - bold</span></span>

<span data-ttu-id="d33a7-443">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-443">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="d33a7-444">0 � 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-444">0 � Use the default font weight.</span></span>
-   <span data-ttu-id="d33a7-445">1 � シン。</span><span class="sxs-lookup"><span data-stu-id="d33a7-445">1 � Thin.</span></span>
-   <span data-ttu-id="d33a7-446">2 � エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="d33a7-446">2 � Extra-light.</span></span>
-   <span data-ttu-id="d33a7-447">3 � ライト。</span><span class="sxs-lookup"><span data-stu-id="d33a7-447">3 � Light.</span></span>
-   <span data-ttu-id="d33a7-448">4 � 標準。</span><span class="sxs-lookup"><span data-stu-id="d33a7-448">4 � Normal.</span></span>
-   <span data-ttu-id="d33a7-449">5 � 中。</span><span class="sxs-lookup"><span data-stu-id="d33a7-449">5 � Medium.</span></span>
-   <span data-ttu-id="d33a7-450">6 � セミボールド。</span><span class="sxs-lookup"><span data-stu-id="d33a7-450">6 � Semibold.</span></span>
-   <span data-ttu-id="d33a7-451">7 � 太字。</span><span class="sxs-lookup"><span data-stu-id="d33a7-451">7 � Bold.</span></span>
-   <span data-ttu-id="d33a7-452">8 � 極太。</span><span class="sxs-lookup"><span data-stu-id="d33a7-452">8 � Extra-bold.</span></span>
-   <span data-ttu-id="d33a7-453">9 � ヘビー。</span><span class="sxs-lookup"><span data-stu-id="d33a7-453">9 � Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="d33a7-454">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-454">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="d33a7-455">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-455">Parameters - bottomMargin</span></span>

<span data-ttu-id="d33a7-456">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-456">value</span></span>  

<!-- -->

<span data-ttu-id="d33a7-457">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-457">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="d33a7-458">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-458">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="d33a7-459">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-459">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="d33a7-460">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-460">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="d33a7-461">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-461">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="d33a7-462">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-462">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="d33a7-463">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-463">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="d33a7-464">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-464">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="d33a7-465">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-465">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="d33a7-466">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-466">Return Value - bottomMarginValue</span></span>

## <a name="method-cachedatamethod"></a><span data-ttu-id="d33a7-467">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-467">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="d33a7-468">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-468">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="d33a7-469">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-469">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="d33a7-470">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-470">Return Value - cacheDataMethod</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="d33a7-471">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-471">Method calcControlSize</span></span>

<span data-ttu-id="d33a7-472">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-472">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="d33a7-473">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-473">Parameters - calcControlSize</span></span>

<span data-ttu-id="d33a7-474">chars</span><span class="sxs-lookup"><span data-stu-id="d33a7-474">chars</span></span>  
<span data-ttu-id="d33a7-475">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="d33a7-475">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="d33a7-476">明細行</span><span class="sxs-lookup"><span data-stu-id="d33a7-476">lines</span></span>  
<span data-ttu-id="d33a7-477">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="d33a7-477">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="d33a7-478">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-478">Return Value - calcControlSize</span></span>

<span data-ttu-id="d33a7-479">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="d33a7-479">The container that holds the width and height.</span></span>

## <a name="method-caption"></a><span data-ttu-id="d33a7-480">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="d33a7-480">Method caption</span></span>

<span data-ttu-id="d33a7-481">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-481">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="d33a7-482">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="d33a7-482">Parameters - caption</span></span>

<span data-ttu-id="d33a7-483">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-483">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="d33a7-484">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="d33a7-484">Return Value - caption</span></span>

<span data-ttu-id="d33a7-485">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="d33a7-485">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="d33a7-486">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="d33a7-486">Method characterSet</span></span>

<span data-ttu-id="d33a7-487">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-487">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="d33a7-488">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="d33a7-488">Parameters - characterSet</span></span>

<span data-ttu-id="d33a7-489">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-489">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="d33a7-490">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="d33a7-490">Return Value - characterSet</span></span>

<span data-ttu-id="d33a7-491">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-491">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="d33a7-492">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="d33a7-492">Remarks - characterSet</span></span>

<span data-ttu-id="d33a7-493">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-493">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="d33a7-494">先頭値</span><span class="sxs-lookup"><span data-stu-id="d33a7-494">Value</span></span> | <span data-ttu-id="d33a7-495">説明</span><span class="sxs-lookup"><span data-stu-id="d33a7-495">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="d33a7-496">0</span><span class="sxs-lookup"><span data-stu-id="d33a7-496">0</span></span>     | <span data-ttu-id="d33a7-497">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-497">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="d33a7-498">1</span><span class="sxs-lookup"><span data-stu-id="d33a7-498">1</span></span>     | <span data-ttu-id="d33a7-499">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-499">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="d33a7-500">2</span><span class="sxs-lookup"><span data-stu-id="d33a7-500">2</span></span>     | <span data-ttu-id="d33a7-501">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-501">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="d33a7-502">77</span><span class="sxs-lookup"><span data-stu-id="d33a7-502">77</span></span>    | <span data-ttu-id="d33a7-503">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-503">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="d33a7-504">128</span><span class="sxs-lookup"><span data-stu-id="d33a7-504">128</span></span>   | <span data-ttu-id="d33a7-505">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-505">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="d33a7-506">129</span><span class="sxs-lookup"><span data-stu-id="d33a7-506">129</span></span>   | <span data-ttu-id="d33a7-507">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-507">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="d33a7-508">134</span><span class="sxs-lookup"><span data-stu-id="d33a7-508">134</span></span>   | <span data-ttu-id="d33a7-509">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-509">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="d33a7-510">136</span><span class="sxs-lookup"><span data-stu-id="d33a7-510">136</span></span>   | <span data-ttu-id="d33a7-511">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-511">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="d33a7-512">161</span><span class="sxs-lookup"><span data-stu-id="d33a7-512">161</span></span>   | <span data-ttu-id="d33a7-513">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-513">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="d33a7-514">162</span><span class="sxs-lookup"><span data-stu-id="d33a7-514">162</span></span>   | <span data-ttu-id="d33a7-515">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-515">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="d33a7-516">163</span><span class="sxs-lookup"><span data-stu-id="d33a7-516">163</span></span>   | <span data-ttu-id="d33a7-517">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-517">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="d33a7-518">186</span><span class="sxs-lookup"><span data-stu-id="d33a7-518">186</span></span>   | <span data-ttu-id="d33a7-519">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-519">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="d33a7-520">204</span><span class="sxs-lookup"><span data-stu-id="d33a7-520">204</span></span>   | <span data-ttu-id="d33a7-521">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-521">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="d33a7-522">238</span><span class="sxs-lookup"><span data-stu-id="d33a7-522">238</span></span>   | <span data-ttu-id="d33a7-523">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-523">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="d33a7-524">255</span><span class="sxs-lookup"><span data-stu-id="d33a7-524">255</span></span>   | <span data-ttu-id="d33a7-525">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-525">OEM\_CHARSET</span></span>         |

<span data-ttu-id="d33a7-526">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-526">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="d33a7-527">金額</span><span class="sxs-lookup"><span data-stu-id="d33a7-527">Value</span></span> | <span data-ttu-id="d33a7-528">説明</span><span class="sxs-lookup"><span data-stu-id="d33a7-528">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="d33a7-529">130</span><span class="sxs-lookup"><span data-stu-id="d33a7-529">130</span></span>   | <span data-ttu-id="d33a7-530">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-530">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="d33a7-531">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-531">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="d33a7-532">先頭値</span><span class="sxs-lookup"><span data-stu-id="d33a7-532">Value</span></span> | <span data-ttu-id="d33a7-533">説明</span><span class="sxs-lookup"><span data-stu-id="d33a7-533">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="d33a7-534">177</span><span class="sxs-lookup"><span data-stu-id="d33a7-534">177</span></span>   | <span data-ttu-id="d33a7-535">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-535">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="d33a7-536">178</span><span class="sxs-lookup"><span data-stu-id="d33a7-536">178</span></span>   | <span data-ttu-id="d33a7-537">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-537">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="d33a7-538">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-538">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="d33a7-539">先頭値</span><span class="sxs-lookup"><span data-stu-id="d33a7-539">Value</span></span> | <span data-ttu-id="d33a7-540">説明</span><span class="sxs-lookup"><span data-stu-id="d33a7-540">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="d33a7-541">222</span><span class="sxs-lookup"><span data-stu-id="d33a7-541">222</span></span>   | <span data-ttu-id="d33a7-542">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="d33a7-542">THAI\_CHARSET</span></span> |

<span data-ttu-id="d33a7-543">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-543">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="d33a7-544">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-544">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="d33a7-545">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d33a7-545">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="d33a7-546">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="d33a7-546">Method colorScheme</span></span>

<span data-ttu-id="d33a7-547">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-547">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="d33a7-548">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="d33a7-548">Parameters - colorScheme</span></span>

<span data-ttu-id="d33a7-549">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-549">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="d33a7-550">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="d33a7-550">Return Value - colorScheme</span></span>

<span data-ttu-id="d33a7-551">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="d33a7-551">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="d33a7-552">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="d33a7-552">Remarks - colorScheme</span></span>

<span data-ttu-id="d33a7-553">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-553">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="d33a7-554">先頭値</span><span class="sxs-lookup"><span data-stu-id="d33a7-554">Value</span></span> | <span data-ttu-id="d33a7-555">スタイル</span><span class="sxs-lookup"><span data-stu-id="d33a7-555">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="d33a7-556">0</span><span class="sxs-lookup"><span data-stu-id="d33a7-556">0</span></span>     | <span data-ttu-id="d33a7-557">既定</span><span class="sxs-lookup"><span data-stu-id="d33a7-557">Default</span></span>               |
| <span data-ttu-id="d33a7-558">1</span><span class="sxs-lookup"><span data-stu-id="d33a7-558">1</span></span>     | <span data-ttu-id="d33a7-559">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="d33a7-559">The Windows palette</span></span>   |
| <span data-ttu-id="d33a7-560">2</span><span class="sxs-lookup"><span data-stu-id="d33a7-560">2</span></span>     | <span data-ttu-id="d33a7-561">真の配色</span><span class="sxs-lookup"><span data-stu-id="d33a7-561">The true-color scheme</span></span> |

## <a name="method-columns"></a><span data-ttu-id="d33a7-562">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="d33a7-562">Method columns</span></span>

```xpp
public int columns([int value])
```

### <a name="parameters---columns"></a><span data-ttu-id="d33a7-563">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="d33a7-563">Parameters - columns</span></span>

<span data-ttu-id="d33a7-564">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-564">value</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="d33a7-565">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="d33a7-565">Return Value - columns</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="d33a7-566">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="d33a7-566">Method configurationKey</span></span>

<span data-ttu-id="d33a7-567">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-567">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="d33a7-568">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d33a7-568">Parameters - configurationKey</span></span>

<span data-ttu-id="d33a7-569">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-569">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="d33a7-570">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d33a7-570">Return Value - configurationKey</span></span>

<span data-ttu-id="d33a7-571">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="d33a7-571">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="d33a7-572">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="d33a7-572">Remarks - configurationKey</span></span>

<span data-ttu-id="d33a7-573">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-573">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="d33a7-574">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-574">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="d33a7-575">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-575">Method configurationKeyEx</span></span>

<span data-ttu-id="d33a7-576">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-576">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="d33a7-577">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-577">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="d33a7-578">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="d33a7-578">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="d33a7-579">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-579">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="d33a7-580">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-580">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="d33a7-581">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-581">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="d33a7-582">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-582">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-count"></a><span data-ttu-id="d33a7-583">メソッド count</span><span class="sxs-lookup"><span data-stu-id="d33a7-583">Method count</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="d33a7-584">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="d33a7-584">Return Value - count</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="d33a7-585">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="d33a7-585">Method countryRegionCodes</span></span>

<span data-ttu-id="d33a7-586">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-586">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="d33a7-587">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="d33a7-587">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="d33a7-588">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-588">value</span></span>  
<span data-ttu-id="d33a7-589">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-589">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="d33a7-590">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="d33a7-590">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="d33a7-591">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="d33a7-591">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="d33a7-592">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="d33a7-592">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="d33a7-593">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="d33a7-593">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="d33a7-594">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-594">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="d33a7-595">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="d33a7-595">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="d33a7-596">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="d33a7-596">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="d33a7-597">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="d33a7-597">Parameters - dataField</span></span>

<span data-ttu-id="d33a7-598">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-598">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="d33a7-599">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="d33a7-599">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="d33a7-600">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-600">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="d33a7-601">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-601">Parameters - dataMethod</span></span>

<span data-ttu-id="d33a7-602">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-602">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="d33a7-603">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-603">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="d33a7-604">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d33a7-604">Method dataRelationPath</span></span>

<span data-ttu-id="d33a7-605">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-605">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="d33a7-606">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d33a7-606">Parameters - dataRelationPath</span></span>

<span data-ttu-id="d33a7-607">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-607">value</span></span>  
<span data-ttu-id="d33a7-608">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-608">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="d33a7-609">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d33a7-609">Return Value - dataRelationPath</span></span>

<span data-ttu-id="d33a7-610">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="d33a7-610">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="d33a7-611">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="d33a7-611">Remarks - dataRelationPath</span></span>

<span data-ttu-id="d33a7-612">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-612">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="d33a7-613">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="d33a7-613">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="d33a7-614">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="d33a7-614">Method dataSource</span></span>

<span data-ttu-id="d33a7-615">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-615">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="d33a7-616">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="d33a7-616">Parameters - dataSource</span></span>

<span data-ttu-id="d33a7-617">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-617">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="d33a7-618">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="d33a7-618">Return Value - dataSource</span></span>

<span data-ttu-id="d33a7-619">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="d33a7-619">The identifier of the data source that will be used.</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="d33a7-620">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="d33a7-620">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="d33a7-621">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="d33a7-621">Parameters - displayLength</span></span>

<span data-ttu-id="d33a7-622">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-622">value</span></span>  

<!-- -->

<span data-ttu-id="d33a7-623">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-623">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="d33a7-624">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="d33a7-624">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="d33a7-625">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-625">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="d33a7-626">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-626">Parameters - displayLengthMode</span></span>

<span data-ttu-id="d33a7-627">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-627">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="d33a7-628">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-628">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="d33a7-629">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-629">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="d33a7-630">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-630">Parameters - displayLengthValue</span></span>

<span data-ttu-id="d33a7-631">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-631">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="d33a7-632">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-632">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="d33a7-633">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="d33a7-633">Method displayTarget</span></span>

<span data-ttu-id="d33a7-634">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-634">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="d33a7-635">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="d33a7-635">Parameters - displayTarget</span></span>

<span data-ttu-id="d33a7-636">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-636">value</span></span>  
<span data-ttu-id="d33a7-637">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-637">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="d33a7-638">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="d33a7-638">Return Value - displayTarget</span></span>

<span data-ttu-id="d33a7-639">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-639">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="d33a7-640">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="d33a7-640">Method dragDrop</span></span>

<span data-ttu-id="d33a7-641">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-641">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="d33a7-642">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="d33a7-642">Parameters - dragDrop</span></span>

<span data-ttu-id="d33a7-643">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-643">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="d33a7-644">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="d33a7-644">Return Value - dragDrop</span></span>

<span data-ttu-id="d33a7-645">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-645">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="d33a7-646">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="d33a7-646">Method dragOver</span></span>

<span data-ttu-id="d33a7-647">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-647">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="d33a7-648">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="d33a7-648">Parameters - dragOver</span></span>

<span data-ttu-id="d33a7-649">dragSource</span><span class="sxs-lookup"><span data-stu-id="d33a7-649">dragSource</span></span>  
<span data-ttu-id="d33a7-650">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-650">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-651">dragMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-651">dragMode</span></span>  
<span data-ttu-id="d33a7-652">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-652">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-653">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-653">x</span></span>  
<span data-ttu-id="d33a7-654">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-654">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-655">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-655">y</span></span>  
<span data-ttu-id="d33a7-656">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-656">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="d33a7-657">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="d33a7-657">Return Value - dragOver</span></span>

<span data-ttu-id="d33a7-658">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-658">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="d33a7-659">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-659">Method dragOverEx</span></span>

<span data-ttu-id="d33a7-660">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-660">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="d33a7-661">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-661">Parameters - dragOverEx</span></span>

<span data-ttu-id="d33a7-662">dragSource</span><span class="sxs-lookup"><span data-stu-id="d33a7-662">dragSource</span></span>  
<span data-ttu-id="d33a7-663">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-663">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-664">dragMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-664">dragMode</span></span>  
<span data-ttu-id="d33a7-665">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-665">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-666">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-666">x</span></span>  
<span data-ttu-id="d33a7-667">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-667">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-668">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-668">y</span></span>  
<span data-ttu-id="d33a7-669">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-669">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="d33a7-670">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-670">Return Value - dragOverEx</span></span>

<span data-ttu-id="d33a7-671">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-671">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="d33a7-672">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="d33a7-672">Method dragText</span></span>

<span data-ttu-id="d33a7-673">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-673">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="d33a7-674">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="d33a7-674">Return Value - dragText</span></span>

<span data-ttu-id="d33a7-675">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="d33a7-675">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="d33a7-676">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-676">Method enabled</span></span>

<span data-ttu-id="d33a7-677">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-677">Determines whether the object is enabled or disabled.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="d33a7-678">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-678">Parameters - enabled</span></span>

<span data-ttu-id="d33a7-679">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-679">value</span></span>  
<span data-ttu-id="d33a7-680">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-680">A Boolean value that determines whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="d33a7-681">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-681">Return Value - enabled</span></span>

<span data-ttu-id="d33a7-682">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-682">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="d33a7-683">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-683">Remarks - enabled</span></span>

<span data-ttu-id="d33a7-684">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-684">The enabled property lets you enable or disable controls at run time.</span></span> <span data-ttu-id="d33a7-685">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-685">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="d33a7-686">また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-686">You can also disable a control that is used only for display purposes, such as an error message that provides read-only information.</span></span>

## <a name="method-enumtype"></a><span data-ttu-id="d33a7-687">メソッド enumType</span><span class="sxs-lookup"><span data-stu-id="d33a7-687">Method enumType</span></span>

```xpp
public EnumId enumType([EnumId value])
```

### <a name="parameters---enumtype"></a><span data-ttu-id="d33a7-688">パラメーター - enumType</span><span class="sxs-lookup"><span data-stu-id="d33a7-688">Parameters - enumType</span></span>

<span data-ttu-id="d33a7-689">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-689">value</span></span>  

### <a name="return-value---enumtype"></a><span data-ttu-id="d33a7-690">戻り値 - enumType</span><span class="sxs-lookup"><span data-stu-id="d33a7-690">Return Value - enumType</span></span>

## <a name="method-enumtypevalue"></a><span data-ttu-id="d33a7-691">メソッド enumTypeValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-691">Method enumTypeValue</span></span>

```xpp
public EnumId enumTypeValue()
```

### <a name="return-value---enumtypevalue"></a><span data-ttu-id="d33a7-692">戻り値 - enumTypeValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-692">Return Value - enumTypeValue</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="d33a7-693">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="d33a7-693">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="d33a7-694">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="d33a7-694">Parameters - extendedDataType</span></span>

<span data-ttu-id="d33a7-695">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-695">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="d33a7-696">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="d33a7-696">Return Value - extendedDataType</span></span>

## <a name="method-find"></a><span data-ttu-id="d33a7-697">メソッド find</span><span class="sxs-lookup"><span data-stu-id="d33a7-697">Method find</span></span>

```xpp
public int find(str string)
```

### <a name="parameters---find"></a><span data-ttu-id="d33a7-698">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="d33a7-698">Parameters - find</span></span>

<span data-ttu-id="d33a7-699">文字列</span><span class="sxs-lookup"><span data-stu-id="d33a7-699">string</span></span>  

### <a name="return-value---find"></a><span data-ttu-id="d33a7-700">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="d33a7-700">Return Value - find</span></span>

## <a name="method-font"></a><span data-ttu-id="d33a7-701">メソッド font</span><span class="sxs-lookup"><span data-stu-id="d33a7-701">Method font</span></span>

<span data-ttu-id="d33a7-702">コントロールに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-702">Gets or sets the name of the font that is used for the control.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="d33a7-703">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="d33a7-703">Parameters - font</span></span>

<span data-ttu-id="d33a7-704">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-704">value</span></span>  
<span data-ttu-id="d33a7-705">コントロールのフォントとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-705">The value to assign as the font for the control; optional.</span></span>

### <a name="return-value---font"></a><span data-ttu-id="d33a7-706">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="d33a7-706">Return Value - font</span></span>

<span data-ttu-id="d33a7-707">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="d33a7-707">The name of the font, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="d33a7-708">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-708">Method fontSize</span></span>

<span data-ttu-id="d33a7-709">コントロール内のテキストに使用されるフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-709">Gets or sets the font size that is used for the control.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="d33a7-710">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-710">Parameters - fontSize</span></span>

<span data-ttu-id="d33a7-711">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-711">value</span></span>  
<span data-ttu-id="d33a7-712">コントロールのフォント サイズとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-712">The value to assign as the font size for the control; optional.</span></span>

### <a name="return-value---fontsize"></a><span data-ttu-id="d33a7-713">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-713">Return Value - fontSize</span></span>

<span data-ttu-id="d33a7-714">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="d33a7-714">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="d33a7-715">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-715">Method foregroundColor</span></span>

<span data-ttu-id="d33a7-716">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-716">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="d33a7-717">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-717">Parameters - foregroundColor</span></span>

<span data-ttu-id="d33a7-718">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-718">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="d33a7-719">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-719">Return Value - foregroundColor</span></span>

<span data-ttu-id="d33a7-720">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="d33a7-720">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="d33a7-721">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d33a7-721">Remarks - foregroundColor</span></span>

<span data-ttu-id="d33a7-722">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-722">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="d33a7-723">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-723">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="d33a7-724">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-724">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="d33a7-725">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="d33a7-725">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="d33a7-726">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-726">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="d33a7-727">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-727">The maximum value for a single byte is 255.</span></span>

## <a name="method-frameposition"></a><span data-ttu-id="d33a7-728">メソッド framePosition</span><span class="sxs-lookup"><span data-stu-id="d33a7-728">Method framePosition</span></span>

```xpp
public int framePosition([int value])
```

### <a name="parameters---frameposition"></a><span data-ttu-id="d33a7-729">パラメーター - framePosition</span><span class="sxs-lookup"><span data-stu-id="d33a7-729">Parameters - framePosition</span></span>

<span data-ttu-id="d33a7-730">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-730">value</span></span>  

### <a name="return-value---frameposition"></a><span data-ttu-id="d33a7-731">戻り値 - framePosition</span><span class="sxs-lookup"><span data-stu-id="d33a7-731">Return Value - framePosition</span></span>

## <a name="method-frametype"></a><span data-ttu-id="d33a7-732">メソッド frameType</span><span class="sxs-lookup"><span data-stu-id="d33a7-732">Method frameType</span></span>

```xpp
public int frameType([int value])
```

### <a name="parameters---frametype"></a><span data-ttu-id="d33a7-733">パラメーター - frameType</span><span class="sxs-lookup"><span data-stu-id="d33a7-733">Parameters - frameType</span></span>

<span data-ttu-id="d33a7-734">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-734">value</span></span>  

### <a name="return-value---frametype"></a><span data-ttu-id="d33a7-735">戻り値 - frameType</span><span class="sxs-lookup"><span data-stu-id="d33a7-735">Return Value - frameType</span></span>

## <a name="method-gettext"></a><span data-ttu-id="d33a7-736">メソッド getText</span><span class="sxs-lookup"><span data-stu-id="d33a7-736">Method getText</span></span>

```xpp
public str getText(int index)
```

### <a name="parameters---gettext"></a><span data-ttu-id="d33a7-737">パラメーター - getText</span><span class="sxs-lookup"><span data-stu-id="d33a7-737">Parameters - getText</span></span>

<span data-ttu-id="d33a7-738">指数</span><span class="sxs-lookup"><span data-stu-id="d33a7-738">index</span></span>  

### <a name="return-value---gettext"></a><span data-ttu-id="d33a7-739">戻り値 - getText</span><span class="sxs-lookup"><span data-stu-id="d33a7-739">Return Value - getText</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="d33a7-740">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="d33a7-740">Method hasChanged</span></span>

<span data-ttu-id="d33a7-741">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-741">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="d33a7-742">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="d33a7-742">Parameters - hasChanged</span></span>

<span data-ttu-id="d33a7-743">val</span><span class="sxs-lookup"><span data-stu-id="d33a7-743">val</span></span>  
<span data-ttu-id="d33a7-744">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-744">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="d33a7-745">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="d33a7-745">Return Value - hasChanged</span></span>

<span data-ttu-id="d33a7-746">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-746">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="d33a7-747">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="d33a7-747">Method hasUserSetting</span></span>

<span data-ttu-id="d33a7-748">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-748">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="d33a7-749">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="d33a7-749">Return Value - hasUserSetting</span></span>

<span data-ttu-id="d33a7-750">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-750">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="d33a7-751">メソッド height</span><span class="sxs-lookup"><span data-stu-id="d33a7-751">Method height</span></span>

<span data-ttu-id="d33a7-752">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-752">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="d33a7-753">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="d33a7-753">Parameters - height</span></span>

<span data-ttu-id="d33a7-754">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-754">value</span></span>  

<!-- -->

<span data-ttu-id="d33a7-755">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-755">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="d33a7-756">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="d33a7-756">Return Value - height</span></span>

<span data-ttu-id="d33a7-757">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="d33a7-757">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="d33a7-758">備考 - height</span><span class="sxs-lookup"><span data-stu-id="d33a7-758">Remarks - height</span></span>

<span data-ttu-id="d33a7-759">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-759">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="d33a7-760">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-760">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="d33a7-761">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-761">Mode</span></span>            | <span data-ttu-id="d33a7-762">高さの計算</span><span class="sxs-lookup"><span data-stu-id="d33a7-762">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d33a7-763">-1 正確</span><span class="sxs-lookup"><span data-stu-id="d33a7-763">-1 Exact</span></span>        | <span data-ttu-id="d33a7-764">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-764">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d33a7-765">0 自動</span><span class="sxs-lookup"><span data-stu-id="d33a7-765">0 Auto</span></span>          | <span data-ttu-id="d33a7-766">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-766">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d33a7-767">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="d33a7-767">1 Column height</span></span> | <span data-ttu-id="d33a7-768">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-768">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="d33a7-769">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-769">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="d33a7-770">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-770">Method heightMode</span></span>

<span data-ttu-id="d33a7-771">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-771">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="d33a7-772">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-772">Parameters - heightMode</span></span>

<span data-ttu-id="d33a7-773">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-773">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="d33a7-774">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-774">Return Value - heightMode</span></span>

<span data-ttu-id="d33a7-775">計算モード。</span><span class="sxs-lookup"><span data-stu-id="d33a7-775">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="d33a7-776">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-776">Remarks - heightMode</span></span>

<span data-ttu-id="d33a7-777">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-777">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="d33a7-778">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-778">Mode</span></span>          | <span data-ttu-id="d33a7-779">高さの計算</span><span class="sxs-lookup"><span data-stu-id="d33a7-779">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d33a7-780">正確</span><span class="sxs-lookup"><span data-stu-id="d33a7-780">Exact</span></span>         | <span data-ttu-id="d33a7-781">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-781">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d33a7-782">自動</span><span class="sxs-lookup"><span data-stu-id="d33a7-782">Auto</span></span>          | <span data-ttu-id="d33a7-783">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-783">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d33a7-784">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="d33a7-784">Column height</span></span> | <span data-ttu-id="d33a7-785">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-785">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="d33a7-786">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-786">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="d33a7-787">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-787">Method heightValue</span></span>

<span data-ttu-id="d33a7-788">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-788">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="d33a7-789">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-789">Parameters - heightValue</span></span>

<span data-ttu-id="d33a7-790">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-790">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="d33a7-791">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-791">Return Value - heightValue</span></span>

<span data-ttu-id="d33a7-792">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="d33a7-792">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="d33a7-793">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-793">Remarks - heightValue</span></span>

<span data-ttu-id="d33a7-794">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-794">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="d33a7-795">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="d33a7-795">Method helpField</span></span>

<span data-ttu-id="d33a7-796">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-796">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="d33a7-797">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="d33a7-797">Return Value - helpField</span></span>

<span data-ttu-id="d33a7-798">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="d33a7-798">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="d33a7-799">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="d33a7-799">Remarks - helpField</span></span>

<span data-ttu-id="d33a7-800">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-800">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="d33a7-801">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-801">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="d33a7-802">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="d33a7-802">Method helpText</span></span>

<span data-ttu-id="d33a7-803">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-803">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="d33a7-804">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="d33a7-804">Parameters - helpText</span></span>

<span data-ttu-id="d33a7-805">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-805">value</span></span>  
<span data-ttu-id="d33a7-806">コントロールのヘルプ テキストとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-806">The value to assign as the Help text for the control; optional.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="d33a7-807">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="d33a7-807">Return Value - helpText</span></span>

<span data-ttu-id="d33a7-808">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="d33a7-808">The string that should be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="d33a7-809">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="d33a7-809">Remarks - helpText</span></span>

<span data-ttu-id="d33a7-810">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-810">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="d33a7-811">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-811">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hidefirstentry"></a><span data-ttu-id="d33a7-812">メソッド hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="d33a7-812">Method hideFirstEntry</span></span>

```xpp
public boolean hideFirstEntry([boolean value])
```

### <a name="parameters---hidefirstentry"></a><span data-ttu-id="d33a7-813">パラメーター - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="d33a7-813">Parameters - hideFirstEntry</span></span>

<span data-ttu-id="d33a7-814">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-814">value</span></span>  

### <a name="return-value---hidefirstentry"></a><span data-ttu-id="d33a7-815">戻り値 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="d33a7-815">Return Value - hideFirstEntry</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="d33a7-816">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d33a7-816">Method hierarchyParent</span></span>

<span data-ttu-id="d33a7-817">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-817">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="d33a7-818">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d33a7-818">Parameters - hierarchyParent</span></span>

<span data-ttu-id="d33a7-819">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-819">value</span></span>  
<span data-ttu-id="d33a7-820">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-820">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="d33a7-821">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="d33a7-821">Return Value - hierarchyParent</span></span>

<span data-ttu-id="d33a7-822">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-822">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="d33a7-823">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="d33a7-823">Method hWnd</span></span>

<span data-ttu-id="d33a7-824">コントロールに関連付けられているウィンドウのハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-824">Returns the handle to the window that is associated with the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="d33a7-825">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="d33a7-825">Return Value - hWnd</span></span>

<span data-ttu-id="d33a7-826">コントロールに関連付けられているウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d33a7-826">The handle to the window that is associated with the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="d33a7-827">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="d33a7-827">Remarks - hWnd</span></span>

<span data-ttu-id="d33a7-828">ウィンドウのハンドルは、Windows API 関数で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-828">The handle to the window can be used with Windows API functions.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="d33a7-829">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="d33a7-829">Method isContainer</span></span>

<span data-ttu-id="d33a7-830">コントロールがコンテナーかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-830">Gets a value that indicates whether the control is a container.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="d33a7-831">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="d33a7-831">Return Value - isContainer</span></span>

<span data-ttu-id="d33a7-832">コントロールがコンテナーである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-832">true if the control is a container; otherwise, false.</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="d33a7-833">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="d33a7-833">Method isDisplayed</span></span>

<span data-ttu-id="d33a7-834">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-834">Returns a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="d33a7-835">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="d33a7-835">Return Value - isDisplayed</span></span>

<span data-ttu-id="d33a7-836">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-836">true if the control is displayed; otherwise, false.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="d33a7-837">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="d33a7-837">Method isRestricted</span></span>

<span data-ttu-id="d33a7-838">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-838">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="d33a7-839">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="d33a7-839">Return Value - isRestricted</span></span>

<span data-ttu-id="d33a7-840">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-840">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="d33a7-841">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-841">Method isUserSetupEnabled</span></span>

<span data-ttu-id="d33a7-842">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-842">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="d33a7-843">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-843">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="d33a7-844">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="d33a7-844">neededSetupRights</span></span>  
<span data-ttu-id="d33a7-845">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-845">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="d33a7-846">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-846">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="d33a7-847">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-847">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="d33a7-848">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="d33a7-848">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="d33a7-849">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-849">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span> <span data-ttu-id="d33a7-850">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-850">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d33a7-851">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="d33a7-851">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="d33a7-852">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-852">No changes can be made to the control.</span></span> <span data-ttu-id="d33a7-853">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-853">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="d33a7-854">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="d33a7-854">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="d33a7-855">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-855">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="d33a7-856">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-856">The user cannot move the control.</span></span>   |
| <span data-ttu-id="d33a7-857">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="d33a7-857">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="d33a7-858">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-858">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="d33a7-859">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-859">The user can also move the control.</span></span> |

## <a name="method-isvalid"></a><span data-ttu-id="d33a7-860">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="d33a7-860">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="d33a7-861">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="d33a7-861">Return Value - isValid</span></span>

## <a name="method-italic"></a><span data-ttu-id="d33a7-862">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="d33a7-862">Method italic</span></span>

<span data-ttu-id="d33a7-863">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-863">Sets or returns a value that indicates whether the text in the control is italic.</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="d33a7-864">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="d33a7-864">Parameters - italic</span></span>

<span data-ttu-id="d33a7-865">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-865">value</span></span>  
<span data-ttu-id="d33a7-866">コントロールの斜体設定の値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-866">The value for the control's italic setting; optional.</span></span>

### <a name="return-value---italic"></a><span data-ttu-id="d33a7-867">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="d33a7-867">Return Value - italic</span></span>

<span data-ttu-id="d33a7-868">コントロール内のテキストが斜体である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-868">true if the text in the control is italic; otherwise, false.</span></span>

## <a name="method-item"></a><span data-ttu-id="d33a7-869">メソッド item</span><span class="sxs-lookup"><span data-stu-id="d33a7-869">Method item</span></span>

```xpp
public int item([int value])
```

### <a name="parameters---item"></a><span data-ttu-id="d33a7-870">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="d33a7-870">Parameters - item</span></span>

<span data-ttu-id="d33a7-871">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-871">value</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="d33a7-872">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="d33a7-872">Return Value - item</span></span>

## <a name="method-items"></a><span data-ttu-id="d33a7-873">メソッド items</span><span class="sxs-lookup"><span data-stu-id="d33a7-873">Method items</span></span>

```xpp
public int items([int value])
```

### <a name="parameters---items"></a><span data-ttu-id="d33a7-874">パラメーター - items</span><span class="sxs-lookup"><span data-stu-id="d33a7-874">Parameters - items</span></span>

<span data-ttu-id="d33a7-875">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-875">value</span></span>  

### <a name="return-value---items"></a><span data-ttu-id="d33a7-876">戻り値 - items</span><span class="sxs-lookup"><span data-stu-id="d33a7-876">Return Value - items</span></span>

## <a name="method-leave"></a><span data-ttu-id="d33a7-877">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="d33a7-877">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="d33a7-878">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="d33a7-878">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="d33a7-879">メソッド left</span><span class="sxs-lookup"><span data-stu-id="d33a7-879">Method left</span></span>

<span data-ttu-id="d33a7-880">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-880">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="d33a7-881">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="d33a7-881">Parameters - left</span></span>

<span data-ttu-id="d33a7-882">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-882">value</span></span>  
<span data-ttu-id="d33a7-883">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-883">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="d33a7-884">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-884">mode</span></span>  
<span data-ttu-id="d33a7-885">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-885">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="d33a7-886">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="d33a7-886">Return Value - left</span></span>

<span data-ttu-id="d33a7-887">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="d33a7-887">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="d33a7-888">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-888">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="d33a7-889">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-889">Parameters - leftMargin</span></span>

<span data-ttu-id="d33a7-890">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-890">value</span></span>  

<!-- -->

<span data-ttu-id="d33a7-891">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-891">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="d33a7-892">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-892">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="d33a7-893">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-893">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="d33a7-894">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-894">Parameters - leftMarginMode</span></span>

<span data-ttu-id="d33a7-895">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-895">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="d33a7-896">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-896">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="d33a7-897">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-897">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="d33a7-898">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-898">Parameters - leftMarginValue</span></span>

<span data-ttu-id="d33a7-899">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-899">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="d33a7-900">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-900">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="d33a7-901">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-901">Method leftMode</span></span>

<span data-ttu-id="d33a7-902">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-902">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="d33a7-903">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-903">Parameters - leftMode</span></span>

<span data-ttu-id="d33a7-904">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-904">value</span></span>  
<span data-ttu-id="d33a7-905">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-905">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="d33a7-906">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-906">Return Value - leftMode</span></span>

<span data-ttu-id="d33a7-907">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="d33a7-907">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="d33a7-908">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-908">Method leftValue</span></span>

<span data-ttu-id="d33a7-909">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-909">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="d33a7-910">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-910">Parameters - leftValue</span></span>

<span data-ttu-id="d33a7-911">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-911">value</span></span>  
<span data-ttu-id="d33a7-912">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-912">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="d33a7-913">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-913">Return Value - leftValue</span></span>

<span data-ttu-id="d33a7-914">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="d33a7-914">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="d33a7-915">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="d33a7-915">Method markAsUserAdd</span></span>

<span data-ttu-id="d33a7-916">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-916">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="d33a7-917">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="d33a7-917">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="d33a7-918">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-918">value</span></span>  
<span data-ttu-id="d33a7-919">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-919">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="d33a7-920">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="d33a7-920">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="d33a7-921">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-921">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-modified"></a><span data-ttu-id="d33a7-922">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="d33a7-922">Method modified</span></span>

```xpp
public boolean modified()
```

### <a name="return-value---modified"></a><span data-ttu-id="d33a7-923">戻り値 - modified</span><span class="sxs-lookup"><span data-stu-id="d33a7-923">Return Value - modified</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="d33a7-924">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d33a7-924">Method mouseDblClick</span></span>

<span data-ttu-id="d33a7-925">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-925">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="d33a7-926">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d33a7-926">Parameters - mouseDblClick</span></span>

<span data-ttu-id="d33a7-927">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-927">x</span></span>  
<span data-ttu-id="d33a7-928">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-928">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-929">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-929">y</span></span>  
<span data-ttu-id="d33a7-930">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-930">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-931">ボタン</span><span class="sxs-lookup"><span data-stu-id="d33a7-931">button</span></span>  
<span data-ttu-id="d33a7-932">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-932">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-933">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d33a7-933">Ctrl</span></span>  
<span data-ttu-id="d33a7-934">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-934">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-935">シフト</span><span class="sxs-lookup"><span data-stu-id="d33a7-935">Shift</span></span>  
<span data-ttu-id="d33a7-936">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-936">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="d33a7-937">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d33a7-937">Return Value - mouseDblClick</span></span>

<span data-ttu-id="d33a7-938">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-938">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="d33a7-939">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="d33a7-939">Remarks - mouseDblClick</span></span>

<span data-ttu-id="d33a7-940">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-940">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="d33a7-941">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="d33a7-941">Method mouseDown</span></span>

<span data-ttu-id="d33a7-942">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-942">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="d33a7-943">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="d33a7-943">Parameters - mouseDown</span></span>

<span data-ttu-id="d33a7-944">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-944">x</span></span>  
<span data-ttu-id="d33a7-945">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-945">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-946">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-946">y</span></span>  
<span data-ttu-id="d33a7-947">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-947">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-948">ボタン</span><span class="sxs-lookup"><span data-stu-id="d33a7-948">button</span></span>  
<span data-ttu-id="d33a7-949">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-949">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-950">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d33a7-950">Ctrl</span></span>  
<span data-ttu-id="d33a7-951">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-951">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-952">シフト</span><span class="sxs-lookup"><span data-stu-id="d33a7-952">Shift</span></span>  
<span data-ttu-id="d33a7-953">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-953">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="d33a7-954">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="d33a7-954">Return Value - mouseDown</span></span>

<span data-ttu-id="d33a7-955">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-955">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="d33a7-956">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="d33a7-956">Remarks - mouseDown</span></span>

<span data-ttu-id="d33a7-957">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-957">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="d33a7-958">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-958">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="d33a7-959">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="d33a7-959">Method mouseMove</span></span>

<span data-ttu-id="d33a7-960">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-960">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="d33a7-961">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="d33a7-961">Parameters - mouseMove</span></span>

<span data-ttu-id="d33a7-962">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-962">x</span></span>  
<span data-ttu-id="d33a7-963">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-963">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-964">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-964">y</span></span>  
<span data-ttu-id="d33a7-965">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-965">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-966">ボタン</span><span class="sxs-lookup"><span data-stu-id="d33a7-966">button</span></span>  
<span data-ttu-id="d33a7-967">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-967">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-968">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d33a7-968">Ctrl</span></span>  
<span data-ttu-id="d33a7-969">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-969">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-970">シフト</span><span class="sxs-lookup"><span data-stu-id="d33a7-970">Shift</span></span>  
<span data-ttu-id="d33a7-971">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-971">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="d33a7-972">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="d33a7-972">Return Value - mouseMove</span></span>

<span data-ttu-id="d33a7-973">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-973">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="d33a7-974">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="d33a7-974">Remarks - mouseMove</span></span>

<span data-ttu-id="d33a7-975">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-975">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="d33a7-976">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="d33a7-976">Method mouseUp</span></span>

<span data-ttu-id="d33a7-977">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-977">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="d33a7-978">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="d33a7-978">Parameters - mouseUp</span></span>

<span data-ttu-id="d33a7-979">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-979">x</span></span>  
<span data-ttu-id="d33a7-980">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-980">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-981">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-981">y</span></span>  
<span data-ttu-id="d33a7-982">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-982">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-983">ボタン</span><span class="sxs-lookup"><span data-stu-id="d33a7-983">button</span></span>  
<span data-ttu-id="d33a7-984">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-984">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-985">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d33a7-985">Ctrl</span></span>  
<span data-ttu-id="d33a7-986">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-986">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-987">シフト</span><span class="sxs-lookup"><span data-stu-id="d33a7-987">Shift</span></span>  
<span data-ttu-id="d33a7-988">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-988">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="d33a7-989">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="d33a7-989">Return Value - mouseUp</span></span>

<span data-ttu-id="d33a7-990">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-990">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="d33a7-991">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="d33a7-991">Remarks - mouseUp</span></span>

<span data-ttu-id="d33a7-992">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-992">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="d33a7-993">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-993">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="d33a7-994">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d33a7-994">Method name</span></span>

<span data-ttu-id="d33a7-995">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-995">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="d33a7-996">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="d33a7-996">Parameters - name</span></span>

<span data-ttu-id="d33a7-997">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-997">value</span></span>  
<span data-ttu-id="d33a7-998">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="d33a7-998">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="d33a7-999">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="d33a7-999">Return Value - name</span></span>

<span data-ttu-id="d33a7-1000">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1000">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="d33a7-1001">備考 - name</span><span class="sxs-lookup"><span data-stu-id="d33a7-1001">Remarks - name</span></span>

<span data-ttu-id="d33a7-1002">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1002">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="d33a7-1003">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1003">It must start with a letter.</span></span>
-   <span data-ttu-id="d33a7-1004">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1004">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="d33a7-1005">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1005">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="d33a7-1006">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1006">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="d33a7-1007">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1007">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="d33a7-1008">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="d33a7-1008">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="d33a7-1009">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="d33a7-1009">Parameters - neededPermission</span></span>

<span data-ttu-id="d33a7-1010">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1010">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="d33a7-1011">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="d33a7-1011">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="d33a7-1012">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d33a7-1012">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="d33a7-1013">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d33a7-1013">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="d33a7-1014">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-1014">Method parentControl</span></span>

<span data-ttu-id="d33a7-1015">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1015">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="d33a7-1016">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-1016">Return Value - parentControl</span></span>

<span data-ttu-id="d33a7-1017">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1017">The parent control for the control.</span></span>

## <a name="method-previewpartref"></a><span data-ttu-id="d33a7-1018">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="d33a7-1018">Method previewPartRef</span></span>

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a><span data-ttu-id="d33a7-1019">パラメーター - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="d33a7-1019">Parameters - previewPartRef</span></span>

<span data-ttu-id="d33a7-1020">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1020">value</span></span>  

### <a name="return-value---previewpartref"></a><span data-ttu-id="d33a7-1021">戻り値 - previewPartRef</span><span class="sxs-lookup"><span data-stu-id="d33a7-1021">Return Value - previewPartRef</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="d33a7-1022">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-1022">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="d33a7-1023">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-1023">Parameters - rightMargin</span></span>

<span data-ttu-id="d33a7-1024">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1024">value</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1025">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1025">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="d33a7-1026">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-1026">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="d33a7-1027">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1027">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="d33a7-1028">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1028">Parameters - rightMarginMode</span></span>

<span data-ttu-id="d33a7-1029">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1029">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="d33a7-1030">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1030">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="d33a7-1031">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1031">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="d33a7-1032">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1032">Parameters - rightMarginValue</span></span>

<span data-ttu-id="d33a7-1033">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1033">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="d33a7-1034">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1034">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="d33a7-1035">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="d33a7-1035">Method securityKey</span></span>

<span data-ttu-id="d33a7-1036">コントロールに関連付けられているセキュリティ キーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1036">Sets or returns the security key that is associated with the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="d33a7-1037">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="d33a7-1037">Parameters - securityKey</span></span>

<span data-ttu-id="d33a7-1038">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1038">value</span></span>  
<span data-ttu-id="d33a7-1039">コントロールに関連付けられているセキュリティ キー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1039">The security key that is associated with the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="d33a7-1040">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="d33a7-1040">Return Value - securityKey</span></span>

<span data-ttu-id="d33a7-1041">コントロールに関連付けられているセキュリティ キー。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1041">The security key that is associated with the control.</span></span>

## <a name="method-selection"></a><span data-ttu-id="d33a7-1042">メソッド selection</span><span class="sxs-lookup"><span data-stu-id="d33a7-1042">Method selection</span></span>

```xpp
public int selection([int value])
```

### <a name="parameters---selection"></a><span data-ttu-id="d33a7-1043">パラメーター - selection</span><span class="sxs-lookup"><span data-stu-id="d33a7-1043">Parameters - selection</span></span>

<span data-ttu-id="d33a7-1044">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1044">value</span></span>  

### <a name="return-value---selection"></a><span data-ttu-id="d33a7-1045">戻り値 - selection</span><span class="sxs-lookup"><span data-stu-id="d33a7-1045">Return Value - selection</span></span>

## <a name="method-selectionchange"></a><span data-ttu-id="d33a7-1046">メソッド selectionChange</span><span class="sxs-lookup"><span data-stu-id="d33a7-1046">Method selectionChange</span></span>

```xpp
public int selectionChange()
```

### <a name="return-value---selectionchange"></a><span data-ttu-id="d33a7-1047">戻り値 - selectionChange</span><span class="sxs-lookup"><span data-stu-id="d33a7-1047">Return Value - selectionChange</span></span>

## <a name="method-selecttext"></a><span data-ttu-id="d33a7-1048">メソッド selectText</span><span class="sxs-lookup"><span data-stu-id="d33a7-1048">Method selectText</span></span>

```xpp
public int selectText(str string)
```

### <a name="parameters---selecttext"></a><span data-ttu-id="d33a7-1049">パラメーター - selectText</span><span class="sxs-lookup"><span data-stu-id="d33a7-1049">Parameters - selectText</span></span>

<span data-ttu-id="d33a7-1050">文字列</span><span class="sxs-lookup"><span data-stu-id="d33a7-1050">string</span></span>  

### <a name="return-value---selecttext"></a><span data-ttu-id="d33a7-1051">戻り値 - selectText</span><span class="sxs-lookup"><span data-stu-id="d33a7-1051">Return Value - selectText</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="d33a7-1052">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="d33a7-1052">Method showContextMenu</span></span>

<span data-ttu-id="d33a7-1053">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1053">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="d33a7-1054">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="d33a7-1054">Parameters - showContextMenu</span></span>

<span data-ttu-id="d33a7-1055">menuHandle</span><span class="sxs-lookup"><span data-stu-id="d33a7-1055">menuHandle</span></span>  
<span data-ttu-id="d33a7-1056">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1056">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="d33a7-1057">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="d33a7-1057">Return Value - showContextMenu</span></span>

<span data-ttu-id="d33a7-1058">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1058">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="d33a7-1059">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1059">Method skip</span></span>

<span data-ttu-id="d33a7-1060">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1060">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="d33a7-1061">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1061">Parameters - skip</span></span>

<span data-ttu-id="d33a7-1062">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1062">value</span></span>  
<span data-ttu-id="d33a7-1063">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1063">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="d33a7-1064">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1064">Return Value - skip</span></span>

<span data-ttu-id="d33a7-1065">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1065">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="d33a7-1066">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="d33a7-1066">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="d33a7-1067">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="d33a7-1067">Parameters - sort</span></span>

<span data-ttu-id="d33a7-1068">sortDirection</span><span class="sxs-lookup"><span data-stu-id="d33a7-1068">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="d33a7-1069">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="d33a7-1069">Return Value - sort</span></span>

## <a name="method-text"></a><span data-ttu-id="d33a7-1070">メソッド text</span><span class="sxs-lookup"><span data-stu-id="d33a7-1070">Method text</span></span>

<span data-ttu-id="d33a7-1071">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1071">Sets or returns the text for the control.</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="d33a7-1072">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="d33a7-1072">Parameters - text</span></span>

<span data-ttu-id="d33a7-1073">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1073">value</span></span>  
<span data-ttu-id="d33a7-1074">コントロールに割り当てるテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1074">The text to assign to the control; optional.</span></span>

### <a name="return-value---text"></a><span data-ttu-id="d33a7-1075">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="d33a7-1075">Return Value - text</span></span>

<span data-ttu-id="d33a7-1076">コントロールのテキスト。コントロールにテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1076">The text for the control; an empty string if there is no text for the control.</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="d33a7-1077">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1077">Method toolTip</span></span>

<span data-ttu-id="d33a7-1078">コントロールのツールヒント テキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1078">Sets or returns the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="d33a7-1079">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1079">Return Value - toolTip</span></span>

<span data-ttu-id="d33a7-1080">コントロールのツールヒント テキスト。コントロールにツールヒント テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1080">The tooltip text for the control; an empty string if there is no tooltip text for the control.</span></span>

## <a name="method-top"></a><span data-ttu-id="d33a7-1081">メソッド top</span><span class="sxs-lookup"><span data-stu-id="d33a7-1081">Method top</span></span>

<span data-ttu-id="d33a7-1082">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1082">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="d33a7-1083">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="d33a7-1083">Parameters - top</span></span>

<span data-ttu-id="d33a7-1084">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1084">value</span></span>  
<span data-ttu-id="d33a7-1085">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1085">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1086">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1086">mode</span></span>  
<span data-ttu-id="d33a7-1087">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1087">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="d33a7-1088">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="d33a7-1088">Return Value - top</span></span>

<span data-ttu-id="d33a7-1089">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1089">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="d33a7-1090">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-1090">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="d33a7-1091">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-1091">Parameters - topMargin</span></span>

<span data-ttu-id="d33a7-1092">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1092">value</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1093">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1093">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="d33a7-1094">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="d33a7-1094">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="d33a7-1095">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1095">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="d33a7-1096">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1096">Parameters - topMarginMode</span></span>

<span data-ttu-id="d33a7-1097">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1097">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="d33a7-1098">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1098">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="d33a7-1099">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1099">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="d33a7-1100">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1100">Parameters - topMarginValue</span></span>

<span data-ttu-id="d33a7-1101">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1101">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="d33a7-1102">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1102">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="d33a7-1103">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1103">Method topMode</span></span>

<span data-ttu-id="d33a7-1104">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1104">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="d33a7-1105">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1105">Parameters - topMode</span></span>

<span data-ttu-id="d33a7-1106">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1106">value</span></span>  
<span data-ttu-id="d33a7-1107">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1107">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="d33a7-1108">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1108">Return Value - topMode</span></span>

<span data-ttu-id="d33a7-1109">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1109">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="d33a7-1110">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1110">Method topValue</span></span>

<span data-ttu-id="d33a7-1111">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1111">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="d33a7-1112">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1112">Parameters - topValue</span></span>

<span data-ttu-id="d33a7-1113">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1113">value</span></span>  
<span data-ttu-id="d33a7-1114">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1114">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="d33a7-1115">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1115">Return Value - topValue</span></span>

<span data-ttu-id="d33a7-1116">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1116">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="d33a7-1117">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="d33a7-1117">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="d33a7-1118">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="d33a7-1118">Parameters - type</span></span>

<span data-ttu-id="d33a7-1119">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1119">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="d33a7-1120">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="d33a7-1120">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="d33a7-1121">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="d33a7-1121">Method underline</span></span>

<span data-ttu-id="d33a7-1122">コントロール内のテキストの下線プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1122">Sets or returns the value of the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="d33a7-1123">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="d33a7-1123">Parameters - underline</span></span>

<span data-ttu-id="d33a7-1124">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1124">value</span></span>  
<span data-ttu-id="d33a7-1125">コントロールに対する underline プロパティの値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1125">The value of the underline property for the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="d33a7-1126">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="d33a7-1126">Return Value - underline</span></span>

<span data-ttu-id="d33a7-1127">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1127">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="d33a7-1128">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d33a7-1128">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="d33a7-1129">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d33a7-1129">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="d33a7-1130">データ</span><span class="sxs-lookup"><span data-stu-id="d33a7-1130">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="d33a7-1131">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d33a7-1131">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="d33a7-1132">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="d33a7-1132">Method userData</span></span>

<span data-ttu-id="d33a7-1133">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1133">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="d33a7-1134">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="d33a7-1134">Parameters - userData</span></span>

<span data-ttu-id="d33a7-1135">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1135">value</span></span>  
<span data-ttu-id="d33a7-1136">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1136">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="d33a7-1137">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="d33a7-1137">Return Value - userData</span></span>

<span data-ttu-id="d33a7-1138">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1138">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="d33a7-1139">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="d33a7-1139">Method userDataItem</span></span>

<span data-ttu-id="d33a7-1140">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1140">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="d33a7-1141">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="d33a7-1141">Parameters - userDataItem</span></span>

<span data-ttu-id="d33a7-1142">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1142">value</span></span>  
<span data-ttu-id="d33a7-1143">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1143">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="d33a7-1144">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="d33a7-1144">Return Value - userDataItem</span></span>

<span data-ttu-id="d33a7-1145">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1145">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="d33a7-1146">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="d33a7-1146">Method userDataItems</span></span>

<span data-ttu-id="d33a7-1147">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1147">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="d33a7-1148">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="d33a7-1148">Parameters - userDataItems</span></span>

<span data-ttu-id="d33a7-1149">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1149">value</span></span>  
<span data-ttu-id="d33a7-1150">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1150">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="d33a7-1151">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="d33a7-1151">Return Value - userDataItems</span></span>

<span data-ttu-id="d33a7-1152">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1152">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="d33a7-1153">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="d33a7-1153">Method userDisable</span></span>

<span data-ttu-id="d33a7-1154">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1154">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="d33a7-1155">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="d33a7-1155">Parameters - userDisable</span></span>

<span data-ttu-id="d33a7-1156">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1156">value</span></span>  
<span data-ttu-id="d33a7-1157">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1157">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="d33a7-1158">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="d33a7-1158">Return Value - userDisable</span></span>

<span data-ttu-id="d33a7-1159">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1159">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="d33a7-1160">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="d33a7-1160">Method userHeight</span></span>

<span data-ttu-id="d33a7-1161">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1161">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="d33a7-1162">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="d33a7-1162">Parameters - userHeight</span></span>

<span data-ttu-id="d33a7-1163">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1163">value</span></span>  
<span data-ttu-id="d33a7-1164">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1164">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="d33a7-1165">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="d33a7-1165">Return Value - userHeight</span></span>

<span data-ttu-id="d33a7-1166">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1166">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="d33a7-1167">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="d33a7-1167">Method userHide</span></span>

<span data-ttu-id="d33a7-1168">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1168">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="d33a7-1169">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="d33a7-1169">Parameters - userHide</span></span>

<span data-ttu-id="d33a7-1170">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1170">value</span></span>  
<span data-ttu-id="d33a7-1171">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1171">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="d33a7-1172">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="d33a7-1172">Return Value - userHide</span></span>

<span data-ttu-id="d33a7-1173">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1173">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="d33a7-1174">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="d33a7-1174">Remarks - userHide</span></span>

<span data-ttu-id="d33a7-1175">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1175">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="d33a7-1176">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1176">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="d33a7-1177">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1177">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="d33a7-1178">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="d33a7-1178">Method userOrgContainer</span></span>

<span data-ttu-id="d33a7-1179">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1179">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="d33a7-1180">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="d33a7-1180">Parameters - userOrgContainer</span></span>

<span data-ttu-id="d33a7-1181">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1181">value</span></span>  
<span data-ttu-id="d33a7-1182">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1182">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="d33a7-1183">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="d33a7-1183">Return Value - userOrgContainer</span></span>

<span data-ttu-id="d33a7-1184">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1184">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="d33a7-1185">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="d33a7-1185">Method userOrgSibling</span></span>

<span data-ttu-id="d33a7-1186">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1186">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="d33a7-1187">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="d33a7-1187">Parameters - userOrgSibling</span></span>

<span data-ttu-id="d33a7-1188">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1188">value</span></span>  
<span data-ttu-id="d33a7-1189">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1189">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="d33a7-1190">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="d33a7-1190">Return Value - userOrgSibling</span></span>

<span data-ttu-id="d33a7-1191">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1191">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="d33a7-1192">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="d33a7-1192">Method userPromptText</span></span>

<span data-ttu-id="d33a7-1193">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1193">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="d33a7-1194">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="d33a7-1194">Parameters - userPromptText</span></span>

<span data-ttu-id="d33a7-1195">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1195">value</span></span>  
<span data-ttu-id="d33a7-1196">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1196">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="d33a7-1197">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="d33a7-1197">Return Value - userPromptText</span></span>

<span data-ttu-id="d33a7-1198">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1198">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="d33a7-1199">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="d33a7-1199">Method userSecurityLevel</span></span>

<span data-ttu-id="d33a7-1200">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1200">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="d33a7-1201">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="d33a7-1201">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="d33a7-1202">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1202">value</span></span>  
<span data-ttu-id="d33a7-1203">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1203">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="d33a7-1204">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="d33a7-1204">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="d33a7-1205">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1205">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="d33a7-1206">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1206">Method userSkip</span></span>

<span data-ttu-id="d33a7-1207">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1207">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="d33a7-1208">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1208">Parameters - userSkip</span></span>

<span data-ttu-id="d33a7-1209">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1209">value</span></span>  
<span data-ttu-id="d33a7-1210">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1210">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="d33a7-1211">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1211">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="d33a7-1212">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="d33a7-1212">Return Value - userSkip</span></span>

<span data-ttu-id="d33a7-1213">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1213">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="d33a7-1214">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="d33a7-1214">Method userWidth</span></span>

<span data-ttu-id="d33a7-1215">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1215">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="d33a7-1216">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="d33a7-1216">Parameters - userWidth</span></span>

<span data-ttu-id="d33a7-1217">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1217">value</span></span>  
<span data-ttu-id="d33a7-1218">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1218">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="d33a7-1219">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="d33a7-1219">Return Value - userWidth</span></span>

<span data-ttu-id="d33a7-1220">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1220">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="d33a7-1221">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="d33a7-1221">Remarks - userWidth</span></span>

<span data-ttu-id="d33a7-1222">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1222">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="d33a7-1223">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1223">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="d33a7-1224">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1224">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-validate"></a><span data-ttu-id="d33a7-1225">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="d33a7-1225">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="d33a7-1226">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="d33a7-1226">Return Value - validate</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="d33a7-1227">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d33a7-1227">Method verticalSpacing</span></span>

<span data-ttu-id="d33a7-1228">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1228">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="d33a7-1229">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d33a7-1229">Parameters - verticalSpacing</span></span>

<span data-ttu-id="d33a7-1230">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1230">value</span></span>  
<span data-ttu-id="d33a7-1231">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1231">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1232">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1232">mode</span></span>  
<span data-ttu-id="d33a7-1233">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1233">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="d33a7-1234">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="d33a7-1234">Return Value - verticalSpacing</span></span>

<span data-ttu-id="d33a7-1235">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1235">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="d33a7-1236">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1236">Method verticalSpacingMode</span></span>

<span data-ttu-id="d33a7-1237">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1237">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="d33a7-1238">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1238">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="d33a7-1239">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1239">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="d33a7-1240">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1240">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="d33a7-1241">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1241">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="d33a7-1242">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1242">Method verticalSpacingValue</span></span>

<span data-ttu-id="d33a7-1243">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1243">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="d33a7-1244">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1244">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="d33a7-1245">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1245">value</span></span>  
<span data-ttu-id="d33a7-1246">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1246">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="d33a7-1247">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1247">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="d33a7-1248">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1248">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="d33a7-1249">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1249">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="d33a7-1250">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1250">Parameters - viewEditMode</span></span>

<span data-ttu-id="d33a7-1251">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1251">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="d33a7-1252">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1252">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="d33a7-1253">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="d33a7-1253">Method visible</span></span>

<span data-ttu-id="d33a7-1254">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1254">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="d33a7-1255">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="d33a7-1255">Parameters - visible</span></span>

<span data-ttu-id="d33a7-1256">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1256">value</span></span>  
<span data-ttu-id="d33a7-1257">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1257">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="d33a7-1258">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="d33a7-1258">Return Value - visible</span></span>

<span data-ttu-id="d33a7-1259">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1259">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="d33a7-1260">メソッド width</span><span class="sxs-lookup"><span data-stu-id="d33a7-1260">Method width</span></span>

<span data-ttu-id="d33a7-1261">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1261">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="d33a7-1262">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="d33a7-1262">Parameters - width</span></span>

<span data-ttu-id="d33a7-1263">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1263">value</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1264">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1264">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="d33a7-1265">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="d33a7-1265">Return Value - width</span></span>

<span data-ttu-id="d33a7-1266">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1266">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="d33a7-1267">備考 - width</span><span class="sxs-lookup"><span data-stu-id="d33a7-1267">Remarks - width</span></span>

<span data-ttu-id="d33a7-1268">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1268">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="d33a7-1269">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1269">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="d33a7-1270">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1270">Mode</span></span>           | <span data-ttu-id="d33a7-1271">幅計算</span><span class="sxs-lookup"><span data-stu-id="d33a7-1271">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d33a7-1272">-1 正確</span><span class="sxs-lookup"><span data-stu-id="d33a7-1272">-1 Exact</span></span>       | <span data-ttu-id="d33a7-1273">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1273">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d33a7-1274">0 自動</span><span class="sxs-lookup"><span data-stu-id="d33a7-1274">0 Auto</span></span>         | <span data-ttu-id="d33a7-1275">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1275">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d33a7-1276">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="d33a7-1276">1 Column width</span></span> | <span data-ttu-id="d33a7-1277">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1277">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="d33a7-1278">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1278">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="d33a7-1279">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1279">Method widthMode</span></span>

<span data-ttu-id="d33a7-1280">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1280">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="d33a7-1281">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1281">Parameters - widthMode</span></span>

<span data-ttu-id="d33a7-1282">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1282">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="d33a7-1283">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1283">Return Value - widthMode</span></span>

<span data-ttu-id="d33a7-1284">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1284">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="d33a7-1285">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1285">Remarks - widthMode</span></span>

<span data-ttu-id="d33a7-1286">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="d33a7-1286">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="d33a7-1287">モード</span><span class="sxs-lookup"><span data-stu-id="d33a7-1287">Mode</span></span>         | <span data-ttu-id="d33a7-1288">幅計算</span><span class="sxs-lookup"><span data-stu-id="d33a7-1288">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d33a7-1289">正確</span><span class="sxs-lookup"><span data-stu-id="d33a7-1289">Exact</span></span>        | <span data-ttu-id="d33a7-1290">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1290">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="d33a7-1291">自動</span><span class="sxs-lookup"><span data-stu-id="d33a7-1291">Auto</span></span>         | <span data-ttu-id="d33a7-1292">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1292">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="d33a7-1293">列の幅</span><span class="sxs-lookup"><span data-stu-id="d33a7-1293">Column width</span></span> | <span data-ttu-id="d33a7-1294">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1294">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="d33a7-1295">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1295">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="d33a7-1296">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1296">Method widthValue</span></span>

<span data-ttu-id="d33a7-1297">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1297">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="d33a7-1298">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1298">Parameters - widthValue</span></span>

<span data-ttu-id="d33a7-1299">値</span><span class="sxs-lookup"><span data-stu-id="d33a7-1299">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="d33a7-1300">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1300">Return Value - widthValue</span></span>

<span data-ttu-id="d33a7-1301">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1301">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="d33a7-1302">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="d33a7-1302">Remarks - widthValue</span></span>

<span data-ttu-id="d33a7-1303">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1303">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-onleaving"></a><span data-ttu-id="d33a7-1304">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="d33a7-1304">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="d33a7-1305">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="d33a7-1305">Parameters - OnLeaving</span></span>

<span data-ttu-id="d33a7-1306">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1306">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1307">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1307">e</span></span>  

## <a name="method-filter"></a><span data-ttu-id="d33a7-1308">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="d33a7-1308">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="d33a7-1309">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="d33a7-1309">Parameters - filter</span></span>

<span data-ttu-id="d33a7-1310">filterStr</span><span class="sxs-lookup"><span data-stu-id="d33a7-1310">filterStr</span></span>  

## <a name="method-mouseenter"></a><span data-ttu-id="d33a7-1311">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="d33a7-1311">Method mouseEnter</span></span>

<span data-ttu-id="d33a7-1312">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1312">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="d33a7-1313">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="d33a7-1313">Parameters - mouseEnter</span></span>

<span data-ttu-id="d33a7-1314">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-1314">x</span></span>  
<span data-ttu-id="d33a7-1315">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1315">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1316">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-1316">y</span></span>  
<span data-ttu-id="d33a7-1317">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1317">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1318">ボタン</span><span class="sxs-lookup"><span data-stu-id="d33a7-1318">button</span></span>  
<span data-ttu-id="d33a7-1319">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1319">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1320">Ctrl</span><span class="sxs-lookup"><span data-stu-id="d33a7-1320">Ctrl</span></span>  
<span data-ttu-id="d33a7-1321">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1321">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1322">シフト</span><span class="sxs-lookup"><span data-stu-id="d33a7-1322">Shift</span></span>  
<span data-ttu-id="d33a7-1323">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1323">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="d33a7-1324">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="d33a7-1324">Method setFocus</span></span>

<span data-ttu-id="d33a7-1325">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1325">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-insert"></a><span data-ttu-id="d33a7-1326">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="d33a7-1326">Method insert</span></span>

```xpp
public void insert(str string, int index)
```

### <a name="parameters---insert"></a><span data-ttu-id="d33a7-1327">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="d33a7-1327">Parameters - insert</span></span>

<span data-ttu-id="d33a7-1328">文字列</span><span class="sxs-lookup"><span data-stu-id="d33a7-1328">string</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1329">指数</span><span class="sxs-lookup"><span data-stu-id="d33a7-1329">index</span></span>  

## <a name="method-onselectionchanged"></a><span data-ttu-id="d33a7-1330">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="d33a7-1330">Method OnSelectionChanged</span></span>

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a><span data-ttu-id="d33a7-1331">パラメーター - OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="d33a7-1331">Parameters - OnSelectionChanged</span></span>

<span data-ttu-id="d33a7-1332">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1332">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1333">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1333">e</span></span>  

## <a name="method-delete"></a><span data-ttu-id="d33a7-1334">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="d33a7-1334">Method delete</span></span>

```xpp
public void delete(str string)
```

### <a name="parameters---delete"></a><span data-ttu-id="d33a7-1335">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="d33a7-1335">Parameters - delete</span></span>

<span data-ttu-id="d33a7-1336">文字列</span><span class="sxs-lookup"><span data-stu-id="d33a7-1336">string</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="d33a7-1337">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-1337">Method prefColumnSize</span></span>

<span data-ttu-id="d33a7-1338">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1338">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="d33a7-1339">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="d33a7-1339">Parameters - prefColumnSize</span></span>

<span data-ttu-id="d33a7-1340">width</span><span class="sxs-lookup"><span data-stu-id="d33a7-1340">width</span></span>  
<span data-ttu-id="d33a7-1341">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1341">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1342">height</span><span class="sxs-lookup"><span data-stu-id="d33a7-1342">height</span></span>  
<span data-ttu-id="d33a7-1343">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1343">The preferred height of the control.</span></span>

## <a name="method-onlookup"></a><span data-ttu-id="d33a7-1344">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="d33a7-1344">Method OnLookup</span></span>

```xpp
private void OnLookup([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlookup"></a><span data-ttu-id="d33a7-1345">パラメーター - OnLookup</span><span class="sxs-lookup"><span data-stu-id="d33a7-1345">Parameters - OnLookup</span></span>

<span data-ttu-id="d33a7-1346">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1346">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1347">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1347">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="d33a7-1348">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="d33a7-1348">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-endupdate"></a><span data-ttu-id="d33a7-1349">メソッド endUpdate</span><span class="sxs-lookup"><span data-stu-id="d33a7-1349">Method endUpdate</span></span>

```xpp
public void endUpdate()
```

## <a name="method-cut"></a><span data-ttu-id="d33a7-1350">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="d33a7-1350">Method cut</span></span>

<span data-ttu-id="d33a7-1351">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1351">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="d33a7-1352">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="d33a7-1352">Method resetUserSetting</span></span>

<span data-ttu-id="d33a7-1353">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1353">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-dropex"></a><span data-ttu-id="d33a7-1354">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-1354">Method dropEx</span></span>

<span data-ttu-id="d33a7-1355">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1355">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="d33a7-1356">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="d33a7-1356">Parameters - dropEx</span></span>

<span data-ttu-id="d33a7-1357">dragSource</span><span class="sxs-lookup"><span data-stu-id="d33a7-1357">dragSource</span></span>  
<span data-ttu-id="d33a7-1358">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1358">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1359">dragMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1359">dragMode</span></span>  
<span data-ttu-id="d33a7-1360">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1360">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1361">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-1361">x</span></span>  
<span data-ttu-id="d33a7-1362">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1362">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1363">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-1363">y</span></span>  
<span data-ttu-id="d33a7-1364">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1364">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="d33a7-1365">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="d33a7-1365">Method lostFocus</span></span>

<span data-ttu-id="d33a7-1366">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1366">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-onvalidated"></a><span data-ttu-id="d33a7-1367">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="d33a7-1367">Method OnValidated</span></span>

```xpp
private void OnValidated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="d33a7-1368">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="d33a7-1368">Parameters - OnValidated</span></span>

<span data-ttu-id="d33a7-1369">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1369">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1370">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1370">e</span></span>  

## <a name="method-onmodified"></a><span data-ttu-id="d33a7-1371">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="d33a7-1371">Method OnModified</span></span>

```xpp
private void OnModified([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="d33a7-1372">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="d33a7-1372">Parameters - OnModified</span></span>

<span data-ttu-id="d33a7-1373">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1373">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1374">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1374">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="d33a7-1375">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="d33a7-1375">Method displayControl</span></span>

<span data-ttu-id="d33a7-1376">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1376">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="d33a7-1377">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="d33a7-1377">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="d33a7-1378">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="d33a7-1378">Parameters - OnGotFocus</span></span>

<span data-ttu-id="d33a7-1379">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1379">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1380">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1380">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="d33a7-1381">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="d33a7-1381">Method mouseLeave</span></span>

<span data-ttu-id="d33a7-1382">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1382">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-dragleave"></a><span data-ttu-id="d33a7-1383">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="d33a7-1383">Method dragLeave</span></span>

<span data-ttu-id="d33a7-1384">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1384">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-add"></a><span data-ttu-id="d33a7-1385">メソッド add</span><span class="sxs-lookup"><span data-stu-id="d33a7-1385">Method add</span></span>

```xpp
public void add(str string)
```

### <a name="parameters---add"></a><span data-ttu-id="d33a7-1386">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="d33a7-1386">Parameters - add</span></span>

<span data-ttu-id="d33a7-1387">文字列</span><span class="sxs-lookup"><span data-stu-id="d33a7-1387">string</span></span>  

## <a name="method-context"></a><span data-ttu-id="d33a7-1388">メソッド context</span><span class="sxs-lookup"><span data-stu-id="d33a7-1388">Method context</span></span>

<span data-ttu-id="d33a7-1389">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1389">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-onselectionchanging"></a><span data-ttu-id="d33a7-1390">メソッド OnSelectionChanging</span><span class="sxs-lookup"><span data-stu-id="d33a7-1390">Method OnSelectionChanging</span></span>

```xpp
private void OnSelectionChanging([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanging"></a><span data-ttu-id="d33a7-1391">パラメーター - OnSelectionChanging</span><span class="sxs-lookup"><span data-stu-id="d33a7-1391">Parameters - OnSelectionChanging</span></span>

<span data-ttu-id="d33a7-1392">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1392">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1393">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1393">e</span></span>  

## <a name="method-beginupdate"></a><span data-ttu-id="d33a7-1394">メソッド beginUpdate</span><span class="sxs-lookup"><span data-stu-id="d33a7-1394">Method beginUpdate</span></span>

```xpp
public void beginUpdate()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="d33a7-1395">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="d33a7-1395">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="d33a7-1396">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="d33a7-1396">Parameters - OnLostFocus</span></span>

<span data-ttu-id="d33a7-1397">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1397">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1398">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1398">e</span></span>  

## <a name="method-enter"></a><span data-ttu-id="d33a7-1399">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="d33a7-1399">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-inputsearch"></a><span data-ttu-id="d33a7-1400">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="d33a7-1400">Method inputSearch</span></span>

<span data-ttu-id="d33a7-1401">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1401">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="d33a7-1402">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="d33a7-1402">Parameters - inputSearch</span></span>

<span data-ttu-id="d33a7-1403">searchStr</span><span class="sxs-lookup"><span data-stu-id="d33a7-1403">searchStr</span></span>  
<span data-ttu-id="d33a7-1404">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1404">The string value to use to filter data; optional.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="d33a7-1405">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="d33a7-1405">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="d33a7-1406">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="d33a7-1406">Parameters - OnEnter</span></span>

<span data-ttu-id="d33a7-1407">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1407">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1408">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1408">e</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="d33a7-1409">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="d33a7-1409">Method gotFocus</span></span>

<span data-ttu-id="d33a7-1410">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1410">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-clear"></a><span data-ttu-id="d33a7-1411">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="d33a7-1411">Method clear</span></span>

```xpp
public void clear()
```

## <a name="method-paste"></a><span data-ttu-id="d33a7-1412">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="d33a7-1412">Method paste</span></span>

<span data-ttu-id="d33a7-1413">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1413">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-lookup"></a><span data-ttu-id="d33a7-1414">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="d33a7-1414">Method lookup</span></span>

```xpp
public void lookup()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="d33a7-1415">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-1415">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="d33a7-1416">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="d33a7-1416">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="d33a7-1417">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="d33a7-1417">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1418">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="d33a7-1418">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1419">overrideObject</span><span class="sxs-lookup"><span data-stu-id="d33a7-1419">overrideObject</span></span>  

## <a name="method-drop"></a><span data-ttu-id="d33a7-1420">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="d33a7-1420">Method drop</span></span>

<span data-ttu-id="d33a7-1421">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1421">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="d33a7-1422">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="d33a7-1422">Parameters - drop</span></span>

<span data-ttu-id="d33a7-1423">dragSource</span><span class="sxs-lookup"><span data-stu-id="d33a7-1423">dragSource</span></span>  
<span data-ttu-id="d33a7-1424">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1424">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1425">dragMode</span><span class="sxs-lookup"><span data-stu-id="d33a7-1425">dragMode</span></span>  
<span data-ttu-id="d33a7-1426">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1426">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1427">x</span><span class="sxs-lookup"><span data-stu-id="d33a7-1427">x</span></span>  
<span data-ttu-id="d33a7-1428">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1428">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="d33a7-1429">y</span><span class="sxs-lookup"><span data-stu-id="d33a7-1429">y</span></span>  
<span data-ttu-id="d33a7-1430">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1430">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-onvalidating"></a><span data-ttu-id="d33a7-1431">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="d33a7-1431">Method OnValidating</span></span>

```xpp
private void OnValidating([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="d33a7-1432">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="d33a7-1432">Parameters - OnValidating</span></span>

<span data-ttu-id="d33a7-1433">sender</span><span class="sxs-lookup"><span data-stu-id="d33a7-1433">sender</span></span>  

<!-- -->

<span data-ttu-id="d33a7-1434">e</span><span class="sxs-lookup"><span data-stu-id="d33a7-1434">e</span></span>  

## <a name="method-undo"></a><span data-ttu-id="d33a7-1435">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="d33a7-1435">Method undo</span></span>

```xpp
public void undo()
```

## <a name="method-copy"></a><span data-ttu-id="d33a7-1436">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="d33a7-1436">Method copy</span></span>

<span data-ttu-id="d33a7-1437">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1437">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-enddrag"></a><span data-ttu-id="d33a7-1438">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="d33a7-1438">Method endDrag</span></span>

<span data-ttu-id="d33a7-1439">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1439">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="d33a7-1440">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="d33a7-1440">Remarks - endDrag</span></span>

<span data-ttu-id="d33a7-1441">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1441">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="d33a7-1442">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="d33a7-1442">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

